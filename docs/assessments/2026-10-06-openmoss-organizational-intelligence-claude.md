---
source: "Xipeng Qiu, Organizational Intelligence: Governing Agentic AI at the Level of the Organization, OpenMOSS, 2026-06-19"
url: "https://openmoss.ai/blog/en/organizational-intelligence/"
reviewer: "Claude Code (claude-opus-5-5): canonical adjudicator"
reviewer_profile:
  harnesses_used: ["Codex primary", "Codex independent assessment", "Claude Code (claude-opus-5-5) independent cross-family assessment", "Claude Code (claude-opus-5-5) adjudication and verification"]
  roles: "Three independent initial extractions across two model families. The Claude assessor saw only file names from the Codex work. The adjudicating Claude session read the Codex report before comparing, so the adjudication is not blind. Human adjudication recorded below."
  shared_inputs: ["Source URL", "AGENTS.md", "assess skill v1.2.0", "content specs", "lessons and committed ledger", "incumbent KB"]
risk_class: High
confidence: Moderate
sources_used:
  - "Codex report, retained as collateral evidence: docs/assessments/2026-10-06-openmoss-organizational-intelligence.md"
  - "Claude working draft: docs/assessments/drafts/2026-10-06-openmoss-organizational-intelligence/claude-opus.md (local, gitignored)"
hitl_executioner: "Ville Takanen"
assessment_date: 2026-10-06
status: "Assessment approved — implementation pending"
---

# Content Review: Organizational Intelligence

This is the canonical report for this assessment, designated by the human reviewer on 2026-10-06. The earlier Codex report for the same source is retained as collateral evidence at `docs/assessments/2026-10-06-openmoss-organizational-intelligence.md`. This report records a second model family's independent assessment, the verified findings the Codex assessments did not make, and the human decisions taken on them. Where this report is silent, the Codex report's claim ledger (C1–C9), incumbent extraction, and search record remain valid supporting evidence.

## A. Intake and Executive Summary

- **Editorial question:** Does an independent cross-family assessment confirm, bound, or change the approved Codex package?
- **Risk class and rationale:** High. The package creates a taxonomy node and states governance and evaluator boundaries that touch high-centrality nodes.
- **Review route:** third independent assessment and the first from a second model family, followed by comparison against the Codex report and human adjudication.
- **Assessment verdict:** synthesized.
- **Editorial strategy:** expand, with three narrow integrations. The node is retained by human decision; the Claude assessor recommended against it (Section C).
- **Evidence confidence:** Moderate for editorial usefulness. Low for the essay's framework claims, which its author describes as "argued … not demonstrated". Insufficient for causal effectiveness and maturity-level validity. High for the citation defects verified in Section B.
- **Assessment:** The approved package survives cross-family review with four revisions:
  1. Anchor the concept in Wilensky (1967) and Kolbjørnsrud (2024), and note a third, multi-agent sense of the term.
  2. Cite the essay as a self-deposited essay, not a working paper.
  3. Do not import the essay's debt vocabulary.
  4. Add an Adversarial Code Review integration.

  Incumbent citation defects found during re-verification are filed separately as a bug.

## B. Critical Analysis

### Agreement with the Codex report

The two model families reached the same verdict (synthesized) and the same risk class (High). They also agree on six substantive points:

- **Compound Loop:** private traces are not shared instructions, and promotion stays a reviewed act (Codex C3).
- **Agent Optimization Loop:** governance rises with a change's reach. Lessons 4–5 remain operative (Codex C4).
- **Maturity levels:** OI maturity levels are not mapped onto ASDLC autonomy levels (Codex C5).
- **Self-preference:** Panickssery et al. (2024) is the evidence for evaluator self-preference. Separation is bounded, not absolute (Codex C6).
- **Benchmarks and effectiveness:** benchmark figures are not imported. Governance effectiveness is Insufficient (Codex C7, C9).
- **Storey:** the paper is single-authored, and "exponential" overstates it (Codex incumbent re-verification).

Agreement across families is consistency, not correctness (Lesson 8).

### Source metadata (verified)

| Field | Finding | Basis |
|---|---|---|
| Author | Xipeng Qiu, sole author. ORCID 0000-0001-7163-5247 | Zenodo creators; ORCID public API |
| Affiliation | OpenMOSS Team, Shanghai Innovation Institute, Fudan University | Page "About" box |
| Published | 2026-06-19 | HTML `article:published_time`; Zenodo `publication_date` |
| Snapshot | SHA-256 `f9dbfb80c551e4dcc18aaf831315a7c61df504c73fd83998f81d38166a009753`, byte-identical to the Codex snapshot | Independent curl fetches |
| DOI | `10.5281/zenodo.20773858`, resource type Publication | Zenodo REST API |
| What the DOI holds | One file, `organizational-intelligence-openmoss-blog.pdf`. The Claude assessor's `pdfinfo`/`pdftotext` pass found a 54-page headless-browser print of the blog page whose front matter reads "DOI: No DOI yet." | Zenodo API (file listing verified by adjudicator); PDF inspection by assessor |
| Peer review | None. The "About" box says the essay "is based on a working paper", but no separately deposited working paper was found by title or author search. | Source HTML; web search |

Cite the source as a self-deposited essay with a Zenodo DOI. Do not cite it as a working paper or a journal article. DataCite maps the record to `article-journal` only because of Zenodo's generic Publication type; do not copy that into a reference annotation.

### Truth Arbitration and Regression Risk

**The node decision.** The Claude assessor recommended no node, for four reasons:
- The term predates the essay and has competing senses.
- The essay is a self-deposited essay with no measurable uptake.
- Its scope exceeds the SDLC.
- Lesson 6's "seminal" condition is unmet.

The adjudicator's view, accepted by the human reviewer, is that only the third reason weighs against a node, and it is outweighed:
- **Scope:** `docs/vision.md` frames ASDLC as a framework for agentic operating models and the industrialization of knowledge work. Organization-level governance is therefore in scope.
- **Competing senses:** these argue for a definitional page that disambiguates, which is what the approved outline does by putting prior usage first.
- **Weak source:** the lack of uptake and peer review bears on how much the page may rely on Qiu, not on whether the concept exists.

The verified defects below do lower trust in the source, so the page must depend on it less than the original outline implied.

**Regression risks if integrated carelessly:**

1. Citing Zheng et al. (2023) for self-preference would import the essay's overclaim.
2. Importing the essay's "intent debt" would contradict Storey's definition. Nine content articles mention Intent Debt.
3. Citing the DOI as a "working paper" would overstate review status.
4. Adopting "the organization is the right unit for evaluating and governing agentic AI" as an ASDLC thesis would assert a comparative claim the essay does not test.
5. Treating all harness changes as evolution-loop changes would contradict Lesson 4. Lesson 4 permits validated soft-harness tuning; the Codex C4 effect rule decides which changes need governance.

**Open question resolved.** The Claude assessor asked whether harness tuning sits in the reflective or the evolution loop. The Codex C4 effect rule answers it:
- A change that alters permissions, acceptance criteria, or mandatory review is governed change.
- Other validated tuning stays under Lesson 4.

### Claim–Evidence Ledger

IDs use an `X` prefix to avoid confusion with the Codex report's C1–C9.

| Claim ID | Claim | Type | Supporting or conflicting evidence | Appraisal | Confidence | Editorial operation | Proposed wording and limits |
|---|---|---|---|---|---|---|---|
| X1 | "Organizational intelligence" is an established term with several senses; the essay offers one agentic interpretation. | definition | Harold L. Wilensky, *Organizational Intelligence: Knowledge and Policy in Government and Industry* (Basic Books, 1967); [Kolbjørnsrud, 2024](https://cmr.berkeley.edu/2024/02/66-2-designing-the-intelligent-organization-six-principles-for-human-ai-collaboration/); [Agensh](https://arxiv.org/abs/2609.26781) (arXiv, 2026-09-22) uses the term for scaling a self-organized multi-agent harness (verified). | Direct for usage. Strongest limitation: no evidence that any one sense dominates in agentic engineering. | High for prior usage; Moderate for node usefulness | split | Definition first, crediting Wilensky as origin; then the human/digital collective sense; then Qiu's governance interpretation, attributed. One sentence noting the multi-agent harness sense. |
| X2 | The essay is a peer-reviewed or working-paper publication. | descriptive | Zenodo deposit is a print of the blog page; no separate working paper found. | Direct. Limitation: a working paper could exist unpublished. | High that the DOI holds the blog print | reject | Reference annotation: "Self-deposited essay with a Zenodo DOI; conceptual framework, not peer-reviewed or empirically tested." |
| X3 | Governance should rise with a loop's reach: operational, reflective (memory, skills, playbooks under existing rules), evolution (policies, gates, evaluation criteria, harness pipelines). | recommendation | Essay, "Three nested loops". Consistent with Lessons 4–5, `agent-optimization-loop`, `compound-loop`. [Self-Harness](https://arxiv.org/abs/2606.09498) shows validated harness proposals without per-change human authorization in benchmark settings. | Conceptual. The essay states necessity, sufficiency, and reviewer cost are open. | Moderate as consistent framing; Low for necessity | corroborate, bound | Attribute as one framing; keep Codex C4's effect rule and Lesson 4 as the operative ASDLC rules. Not established practice. |
| X4 | Private working state may update automatically; promotion into authoritative shared knowledge is a separate, reviewed act. | recommendation | Essay, state formulation. Reconciles Ralph Loop's automatic `progress.txt` with Compound Loop's gated writeback. | Design heuristic. Limitation: no evidence promotion review catches enough bad lessons to justify its cost; private state can leak if agents read each other's scratch. | Moderate as heuristic; Low as demonstrated effect | corroborate, refine | "Task-local working state (progress files, scratch notes) may update automatically because it is discarded or rotated with the task. Promotion of a candidate learning into shared, authoritative context is a separate, reviewed act." Combine with Codex C3. |
| X5 | Same-model evaluators favor their own outputs. | descriptive (cited) | [Panickssery et al., 2024](https://arxiv.org/abs/2404.13076) supports it on summarization with 2023–24 models. The essay also cites [Zheng et al., 2023](https://arxiv.org/abs/2306.05685), which states: "Due to limited data and small differences, our study cannot determine whether the models exhibit a self-enhancement bias" (v4 PDF, verified). | Method fit good for evaluator bias, indirect for code review. Limitation: one task domain, older models, effect varies by model. | Moderate for self-preference; Low for transfer to code review | corroborate, bound | In `adversarial-code-review`: "LLM evaluators have been shown to prefer their own generations (Panickssery et al., 2024; summarization tasks, 2023–24 models). A fresh session removes shared conversation context, not model-level self-preference; where possible, use a different model family for the Critic." No effect size for code. Do not cite Zheng or the essay for this. |
| X6 | The essay names "intent debt" (a loop drifting from its set-up purpose) and "comprehension debt" (understanding lost as unreviewed outputs ship). | definition | Essay: "We call them intent debt … and comprehension debt", uncited (verified). [Storey](https://arxiv.org/abs/2603.22106) v4 defines intent debt as "the absence or erosion of explicit rationale, goals, and constraints that guide how a system evolves" and cites Alakmeh et al. (2026) for comprehension debt (verified). | Terms predate the essay; its intent-debt sense conflicts with Storey's. Limitation: the essay may not claim coinage, but "We call them" without citation will mislead. | High | reject import | Use incumbent Cognitive Debt and Intent Debt only. The OI concept does not define either term. |
| X7 | The essay's L0–L5 scale grades organizational maturity, with minimum governance controls per level. | definition | Essay, Maturity Model; L4–L5 are "research targets". Human steering (Codex report): a distinct construct from ASDLC autonomy. | No validation of construct, classification criteria, or predictive use. | Low for scale validity | retain as attributed proposal | Describe the scale on its own terms inside the concept, with one sentence stating it measures organizational capability, not agent autonomy. No mapping table. |
| X8 | "A verifier that waves through bad work is worse than none." | causal | Essay, verification section. No data. | Plausible false-assurance argument; untested. | Insufficient | reject | Do not repeat. Prefer executable postconditions where available (consistent with `context-gates`). |

### Incumbent citation re-verification

These defects were triggered by Lesson 9 and are independent of this assessment's verdict. They are filed as [AL-104](https://linear.app/asdlc/issue/AL-104) and are not part of this package.

1. **`concepts/harness-engineering`, reference 1.** It cites "The Agent Harness", Martin Fowler, `martinfowler.com/articles/agent-harness.html`, 2024-05-20.
   - The URL returns 404 (verified).
   - The page on martinfowler.com is Birgitta Böckeler, "Harness engineering for coding agent users", dated 02 April 2026, which updates a 17 February 2026 memo (verified).
   - The word "horse" does not appear in it (verified). The body sentence "popularized by Martin Fowler … using the equestrian metaphor" is therefore unsupported.
   - Whether Böckeler states the exact "Agent = Model + Harness" equation was checked by the assessor only.
2. **`concepts/harness-engineering`, Ning et al.** The arXiv title is "Code as Agent Harness" (verified), and the KB adds a subtitle that isn't in it. The abstract organizes "the survey around three connected layers" (verified), while the KB says "Following the framework established …" and so turns a survey's organizing scheme into a production architecture. The article also has two `### 3.` headings (verified).
3. **`concepts/triple-debt-model` and `concepts/provenance`.**
   - "Formulated by Margaret-Anne Storey et al." should be Storey alone.
   - The annotation "Reviewed by Kent Beck, Adam Tornhill, …" misreads the acknowledgments. They thank colleagues "who provided valuable feedback and ideas on reviewing earlier drafts" (verified), which is not peer review.
   - The intent-debt wording predates v4.
   - "Drives an exponential increase" and "minimizes Technical Debt but supercharges …" overstate Storey's hedged "may".
4. **`patterns/adversarial-code-review`.** The self-validation section has no peer-reviewed support. This is addressed in this package by X5, not by the bug.
5. **`patterns/agent-optimization-loop`.** `lastUpdated: 2026-03-18` predates its June 2026 material. Fix it when integrating X3.
6. **`concepts/levels-of-autonomy`.** The assessor reports "per session" where the Huang et al. source says "per transcript". Minor; recorded only.

### Search and Selection Record

- **Required?:** Yes. The assessment involves empirical, definitional, and time-sensitive claims.
- **Question and date:** Does the essay add to, bound, or contradict incumbent claims on loop governance, memory promotion, independent verification, maturity levels, and debt vocabulary, and does it justify a node? 2026-10-06.
- **Sources searched and queries:**
  - Source HTML: raw curl, transcribed.
  - Source metadata: Zenodo REST API and deposit PDF; ORCID public API.
  - arXiv: the API batch over the essay's cited IDs; full PDFs for Zheng et al. 2306.05685v4, Panickssery et al. 2404.13076, and Storey 2603.22106v4; abstracts for TheAgentCompany v1 and v3; Agensh 2609.26781.
  - Other pages: the ACL Anthology page for EnterpriseBench; Anthropic, "When AI builds itself"; martinfowler.com harness pages.
  - Queries: the exact title; "Xipeng Qiu organizational intelligence arXiv 2026 OpenMOSS agents"; "comprehension debt" origin; local greps over `src/content` for organizational intelligence, debt terms, double-loop learning, maker-checker, least privilege, self-preference, harness, memory, and levels.
- **Selection:**
  - **Included:** primary records for source metadata, and primary papers for any claim the KB would import or that reinforces an incumbent claim.
  - **Excluded:** the essay's pre-LLM organization-theory bibliography (nothing imported), practitioner "company brain" sources (labelled non-peer-reviewed by the essay), and paywalled press.
  - **Inaccessible:** the incumbent Fowler URL (404); Alakmeh et al. (2026), which is known only through Storey's reference list.
- **Limitations:**
  - One Claude assessor, and the adjudicator was not blind to the Codex report.
  - 2026 benchmark papers were checked at the abstract level.
  - No search for empirical evaluations of governance tiering.
  - Web search was US-only.

## C. Disagreement and Human Decision

### Disagreement Record

| Reviewer or role | Position | Evidence or rationale | Adjudication response |
|---|---|---|---|
| Codex primary and independent (Codex report) | Create an OI concept; two loop integrations; four reciprocal edges. | Prior OI literature, corpus gap, incumbent loop contracts. | Retained, with the revisions below. |
| Claude assessor | Same verdict and risk; integrate only, no node; add `adversarial-code-review` integration; repair incumbent citations. | Competing senses of the term; self-deposited essay without uptake; scope beyond the SDLC; Lesson 6 unmet. Found the Zheng miscitation, uncited debt terms, blog-print DOI, and harness-engineering and triple-debt-model citation defects. | Node objection narrowed: it becomes constraints on the node, not its removal (Section B). All verified findings adopted. |
| Claude assessor vs. human steering | Assessor called the shared L-numbering a "collision" with ASDLC autonomy levels. | Reader-confusion risk on a high-centrality node. | Narrowed. The human reviewer had already ruled the scales distinct, so there is no conceptual conflict. One disambiguating sentence in the concept addresses reader confusion. |
| Codex critic extension (working draft, not approved) | Proposes refining `patterns/adversarial-code-review` with Panickssery, bounded. | Independent convergence on the same evidence and a compatible bound. | Implement X5 and any approved extension wording as one coherent edit to that article. |

### Human Decision

- **HITL reviewer:** Ville Takanen, 2026-10-06.
- **Decision or override:**
  - Keep the concept node, revised: Wilensky origin, the multi-agent sense noted, the essay cited as a self-deposited essay, and no debt-term import.
  - Add the `adversarial-code-review` integration to the package.
  - File the incumbent citation repairs as a separate bug ([AL-104](https://linear.app/asdlc/issue/AL-104)).
  - Record this assessment as a separate report rather than amending the Codex report.
  - Designate this report as the official canonical report, retain the Codex report as collateral evidence, and update the ledger line.
- **Rationale and feedback applied:** the reviewer accepted the adjudicator's recommendation on the node and on every option except the citation repairs, which were redirected to a bug. The original Codex package approval stands; this report narrows its concept scope and adds one integration.

## D. Knowledge Graph Impact and Action Plan

| # | Action | Path | Type |
|---|---|---|---|
| 1 | Define Organizational Intelligence per Codex action 1, revised by X1, X2, X6, and X7. | `src/content/concepts/organizational-intelligence.md` | CREATE |
| 2 | Codex C3 wording plus the X4 private-state refinement. | `src/content/patterns/compound-loop.md` | INTEGRATE |
| 3 | Codex C4 effect rule plus the attributed X3 framing; fix `lastUpdated`. | `src/content/patterns/agent-optimization-loop.md` | INTEGRATE |
| 4 | Add Panickssery et al. (2024) and the X5 same-model bound; coordinate with the critic extension. | `src/content/patterns/adversarial-code-review.md` | INTEGRATE |
| 5 | Reciprocal edges per Codex action 4; unchanged. | Concept plus `agentic-sdlc`, `harness-engineering`, `compound-loop`, `agent-optimization-loop` | LINK |
| 6 | File incumbent citation repairs 1–3 as a separate bug. | Linear [AL-104](https://linear.app/asdlc/issue/AL-104) | LOG |
| 7 | File this canonical report; retain the Codex report unchanged as collateral evidence; update the ledger line. | `docs/assessments/2026-10-06-openmoss-organizational-intelligence-claude.md`, `docs/assessments/2026-10-06-openmoss-organizational-intelligence.md`, `docs/assessments/ledger.jsonl` | LOG |

Graph delta beyond the Codex package: none. Action 4 edits an existing node without new edges.

## E. Draft Content

Revisions to the Codex concept outline:
- **Definition:** Wilensky (1967) first, then Kolbjørnsrud (2024), then one sentence on the multi-agent harness sense (Agensh, 2026).
- **Agentic Interpretation:** attribute Qiu (2026) as one proposed interpretation.
- **OI Maturity Levels:** describe the scale as an attributed, unvalidated proposal, with L4–L5 marked as the essay's own "research targets".
- **Open Questions:** include the essay's own statement that its governance requirements are "argued … not demonstrated".
- **Excluded:** the essay's debt terms and benchmark figures.

Integration wording is in X3–X5.

## F. Canonical Ledger Entry

The ledger keeps one line for `2026-10-06-openmoss-organizational-intelligence`. The Codex adjudicator had appended it, but it was not yet committed, so it was rewritten in place rather than appended a second time. No committed history changed. The line records:
- the three-reviewer, two-family profile, with this report as canonical and the Codex report as collateral evidence;
- the 2026-10-06 human decisions as pivots;
- `final_verdict: synthesized` and `execution_status: pending`. Pending refers to content implementation.

## G. Reusable Learning

**Lesson 10 (approved by the human reviewer 2026-10-06 and added to `docs/assessments/lessons.md`):** verify the challenger's own citations for every claim the KB would import, not only the incumbent's. Lesson 9 covers incumbent citations at the moment of corroboration. This pass found three problems on the challenger side that the same import step would have carried into the KB:
- a miscited bias (Zheng et al.);
- uncited debt terms that conflict with the KB's definitions;
- a DOI that resolves to a print of the blog itself.
