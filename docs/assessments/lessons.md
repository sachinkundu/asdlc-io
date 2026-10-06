# Assessor Long-Term Memory (Lessons Learned)

This document records crystallized heuristics and lessons learned from past content assessments, human-in-the-loop (HITL) pivots, and integration retrospectives. The assessor loads this file at the start of every assessment to avoid repeating past mistakes and ensure alignment with the latest scientific writing standards.

## Heuristics & Lessons

### 1. Proportional Gates & Scaffolding
- **Lesson:** Avoid pre-building comprehensive canonical scaffolding/validation rules ahead of concrete demand. Gates must earn their place by protecting against specific, named risks. Linters and type-checkers are low-cost baseline defaults; other checks (visual regression, security policies) should be added only when a concrete failure mode is identified.
- **Reference:** [Theory of LLM Constraints](/concepts/theory-of-llm-constraints) (2026-05-18)

### 2. Scientific Writing Parity
- **Lesson:** Every new concept article must be written in an objective, factual, academic tone. Avoid marketing hype, buzzwords, or anthropomorphic descriptions of agents. Clearly demarcate evidence levels (empirical vs. dialectical/conceptual) and state boundary conditions/limitations.
- **Reference:** Content Articles Spec (2026-05-20)

### 3. SEO & Taxonomy Definitions vs. Implementation Overlap
- **Lesson:** Do not reject a new concept article solely based on conceptual overlap with operational practice nodes (e.g., `workflow-as-code` vs. `harness-engineering`). If the term is a major industry category designator or represents significant SEO value, it warrants a dedicated concept article. Differentiate by letting the concept define *what and why* (taxonomy/discipline) and the practice define *how* (execution steps).
- **Reference:** [Code as Agent Harness](/docs/assessments/2026-05-20-code-as-agent-harness) (2026-05-20)

### 4. Harness Self-Tuning and Autonomy Boundaries (Soft vs. Hard Harness)
- **Lesson:** When documenting agent self-improvement or self-tuning loops, explicitly qualify the boundary of autonomy. The agent's self-modification should be limited to the **Soft Harness** (prompts, instructions, settings) to target model-specific failure patterns. The **Hard Harness** (sandbox runtime, tool implementations, and security gates) must remain frozen and human-governed to prevent behavioral drift and safety regressions, mirroring how design systems remain immutable compared to mutable UI pages.
- **Reference:** [Self-Harness Assessment](/docs/assessments/2026-06-10-self-harness) (2026-06-10)

### 5. Controlled Evaluator Evolution Requires Anchored Epochs
- **Lesson:** When assessing learned evaluators, co-evolving judges, or non-stationary utility functions, do not treat evaluator mutation as safe by default. It is acceptable only when the evaluator is frozen within an epoch, promoted at governed boundaries, checked against an independent ground-truth anchor, and regression-tested against held-out scenarios that the new evaluator did not optimize directly.
- **Reference:** [Red Queen Gödel Machine Assessment](/docs/assessments/2026-06-30-red-queen-godel-machine) (2026-06-30)

### 6. Preserve HITL Taxonomy Overrides
- **Lesson:** Duplicate-check rejections are not absolute when a source introduces a named framework that is likely to become a reusable research or industry reference. A standalone concept may be warranted as a taxonomy anchor if human review explicitly accepts the vocabulary cost and the page remains definitional while incumbent patterns carry the implementation guidance. This override has now recurred twice — agents recommended "synthesize, no new article" and HITL overrode to create the standalone page both times. Treat it as the default expectation for **named, seminal, citable systems from notable sources** (extending Lesson #3 beyond "industry category designator"), and propose the standalone node rather than defaulting against it.
- **Reference:** [ReAct Assessment](/docs/assessments/2026-05-28-react) (2026-05-28), [Red Queen Gödel Machine Assessment](/docs/assessments/2026-06-30-red-queen-godel-machine) (2026-06-30)

### 7. Article Status Is a Distribution Switch
- **Lesson:** Frontmatter `status` is not just editorial metadata — `Live`/`Experimental` gates the MCP index, the `.md` variant endpoints, and MCP eval fixtures. Before proposing a status change (especially `Deprecated`), check the distribution side effects. When the KB's position on a pattern reverses, deprecate the *pattern in prose* while keeping the taxonomy-anchor URL Live: the article retains definitional authority for the term (concept validity) while its guidance discourages usage (usage guidance). Concept validity and usage guidance are separate axes — do not collapse them into a status flag.
- **Reference:** [Persona Prompting Evidence Assessment](/docs/assessments/2026-07-05-persona-prompting-evidence) (2026-07-05)

### 8. Assessor Count Is an Operating Profile, Not Evidence
- **Lesson:** Do not encode a current multi-assessor configuration as a universal epistemic rule. Route independent review by change risk and unresolved uncertainty, and treat model agreement as consistency rather than correctness. Record the reviewer profile for provenance; require evidence or an independent anchor for the underlying claim.
- **Reference:** [Academic Editorial Pipeline Assessment](/docs/assessments/2026-08-25-academic-editorial-pipeline) (2026-08-25)

### 9. Corroboration Triggers Incumbent Citation Re-Verification
- **Lesson:** When a challenger corroborates an incumbent claim, re-verify the incumbent's existing citations (URL, byline, date, method label, metric definition) before adding the new reference. Corroboration is the moment an overstated sentence is most likely to be reinforced rather than examined. The Spotify pass found a drifted Faros URL, a consultancy estimate labelled "empirical telemetry", a METR result stated without its temporal bound, and a categorical "no net throughput improvement" sentence contradicted by its own next sentence — all in nodes the new source would have endorsed.
- **Reference:** [Spotify Coding Constraint Assessment](/docs/assessments/2026-09-30-spotify-coding-constraint) (2026-10-01)

### 10. Verify the Challenger's Own Citations Before Import
- **Lesson:** Lesson 9 re-checks the incumbent's citations. Apply the same check to the challenger for every claim, term, or reference the KB would import.
  - **Cited evidence:** confirm that the cited paper supports the claim as stated, not only that the paper exists.
  - **Terms:** confirm whether the challenger coined each term. If the term already exists, check whether the challenger's definition conflicts with the KB's.
  - **Publication status:** check what a DOI or "working paper" label actually points to.

  A challenger that cites peer-reviewed work in good faith can still carry an overclaim, and the import step repeats it with the KB's authority. The OpenMOSS pass found three such problems:
  - the essay cited Zheng et al. (2023) for a self-preference bias that Zheng et al. state they "cannot determine";
  - it introduced "intent debt" and "comprehension debt" without citation, and its "intent debt" conflicts with Storey's definition used across the KB;
  - its DOI resolves to a print of the blog post, not the working paper it mentions.
- **Reference:** [OpenMOSS Organizational Intelligence Assessment](/docs/assessments/2026-10-06-openmoss-organizational-intelligence-claude) (2026-10-06)
