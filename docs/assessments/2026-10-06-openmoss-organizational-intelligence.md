---
source: "Xipeng Qiu, Organizational Intelligence: Governing Agentic AI at the Level of the Organization, OpenMOSS, 2026-06-19"
url: "https://openmoss.ai/blog/en/organizational-intelligence/"
reviewer: "Codex primary assessor and canonical adjudicator"
reviewer_profile:
  harnesses_used: ["Codex primary", "Codex independent assessment"]
  roles: "Separate initial extractions; primary also drafts synthesis; human adjudication recorded below. Same inherited model family, not cross-model replication."
  shared_inputs: ["Source URL", "AGENTS.md", "assess skill", "content specs", "lessons and ledger", "incumbent KB"]
risk_class: High
confidence: Moderate
assessment_date: 2026-10-06
hitl_executioner: "Ville Takanen"
status: "Assessment approved — implementation pending"
---

# Content Review: Organizational Intelligence

## A. Intake and Executive Summary

- **Editorial question:** Does this source warrant an organization-level concept in the software-development KB, and which existing guidance needs clarification?
- **Risk:** High: proposed taxonomy node and governance boundaries, including evaluation and persistent learning. Route: two independent initial assessments followed by human adjudication.
- **Assessment verdict:** synthesized.
- **Editorial strategy:** expand, with two narrow integrations.
- **Confidence:** Moderate in editorial usefulness; Insufficient for causal effectiveness or maturity-level validity.
- **Recommendation:** Create a concise Organizational Intelligence concept anchored in established usage, presenting Qiu's contribution as a proposed agentic interpretation. Clarify the Compound Loop's persistence boundary and the Agent Optimization Loop's change boundary. Preserve current authority and evaluator constraints.

This is a terminology and scope gap, not an absent implementation architecture. Lessons 3 and 6 support considering a named concept despite overlap. Earlier organizational-intelligence literature provides a stronger reason for the node than an unsupported claim that this particular essay is seminal or has search demand.

## B. Critical Analysis

### Incumbent extraction

| Article | Current position and consequence for assessment |
|---|---|
| `concepts/agentic-sdlc` | Humans govern a software factory; the core is already socio-technical. Do not recast the KB as model-only. |
| `patterns/agentic-double-diamond` | Discovery, specification, assembly, and runtime feedback already extend beyond coding. No replacement lifecycle needed. |
| `concepts/context-engineering` | Already includes organizational context and platform interfaces. The gap concerns authority and continuity across teams, not introducing organizational context for the first time. |
| `patterns/compound-loop` | Human-gated persistence to scoped, retrievable artifacts already captures durable team learning. |
| `concepts/learning-loop` | Crystallizes discoveries into living specs. Preserve this distinct purpose. |
| `patterns/agent-optimization-loop` | Separates product execution from producer improvement; evaluator updates already have epoch and anchor constraints. |
| `concepts/harness-engineering` | Infrastructure surrounding a model is already first-class. OI must add an organizational subject, not rename this discipline. |
| `patterns/context-gates`, `concepts/provenance` | Existing verification and accountability structures remain useful; neither proves institutional effectiveness. |
| `concepts/levels-of-autonomy` | Classifies operational independence. Its L5 explicitly removes human intervention and structural overrides. |
| `concepts/triple-debt-model` | Cognitive and intent debt already have definitions and a primary source. Avoid duplicating terminology. |

### Challenger extraction

Qiu proposes an organization-level framework spanning shared state, authority, and learning. It separates operational, reflective, and evolution loops, distinguishes private records from authoritative knowledge, and proposes governance-gated maturity levels. The essay acknowledges that the framework and its governance requirements lack empirical validation. [Source: Introduction, Three nested loops, Maturity Model, Limitations](https://openmoss.ai/blog/en/organizational-intelligence/).

### Metadata and evidence provenance

The HTML appendix names **Xipeng Qiu**, OpenMOSS Team / Shanghai Innovation Institute / Fudan University, and describes the essay as based on a working paper. HTML `article:published_time` is **2026-06-19**. Treat it as a conceptual essay; hosting and a DOI do not establish peer review. The [Zenodo record](https://zenodo.org/records/20773858) verifies the author, June 19 publication date, v1, and DOI `10.5281/zenodo.20773858`; its technical creation date is June 20. Direct DOI resolution initially failed, but direct record access succeeded. The deposit PDF was not compared with the live HTML.

Retrieved HTML snapshot: `/private/tmp/openmoss-oi.html`; SHA-256 `f9dbfb80c551e4dcc18aaf831315a7c61df504c73fd83998f81d38166a009753`. This temporary snapshot is an inspection aid, not a permanent archive. Access date is not publication date or proof of when particular wording was added.

### Claim–Evidence Ledger

Confidence applies to the bounded claim, not the proposal's appeal. For all governance recommendations below: provenance is first-party conceptual argument; selection bias toward supportive agent literature is possible; consistency with incumbent policy is not independent validation; organization-wide reproducibility and cost remain untested.

| ID | Claim and type | Evidence and appraisal, including strongest limitation | Confidence | Operation | Proposed wording and limits |
|---|---|---|---|---|---|
| C1 | OI merits a term definition. Definition/editorial recommendation. | [Kolbjørnsrud, 2024](https://cmr.berkeley.edu/2024/02/66-2-designing-the-intelligent-organization-six-principles-for-human-ai-collaboration/) directly establishes prior human/digital collective usage. Suitable for terminology, not causal estimates. Corpus search found no dedicated OI node. Counterpoint: existing factory language already spans organization design. | High for prior usage; Moderate for node usefulness | split | Define the collective capacity to solve problems and adapt; identify agentic governance as one interpretation. Do not attribute invention of the term to OpenMOSS. |
| C2 | The three loops offer a useful comparison. Conceptual. | Qiu, Three nested loops; incumbent Ralph, Compound, Learning, and Optimization loops. Strong semantic fit, no measured superiority. The operational loop spans multiple actors and is not equivalent to one Ralph execution. | Moderate | corroborate | Use the distinction to ask what changes: a deliverable, reusable knowledge, or future operating rules. Mapping is explanatory, not one-to-one equivalence. |
| C3 | Persistence needs an authority distinction. Recommendation. | Qiu, state formulation and Three nested loops; Compound Loop already gates durable guidance. [CI-Work](https://arxiv.org/abs/2604.21308) supplies a bounded enterprise-information-flow benchmark, not a longitudinal memory trial. Access permission alone does not settle permitted use. | Moderate | bound | “Execution traces record what happened. Candidate lessons propose what future work should do. Persisting a trace does not authorize its promotion into shared instructions.” Retain the existing human gate. |
| C4 | Classify changes by effects, not filename. Editorial recommendation. | Incumbent Optimization Loop and assessment Lessons 4–5. [Self-Harness](https://arxiv.org/abs/2606.09498) supports tested harness proposals; [RQGM](https://arxiv.org/abs/2606.26294) supports epoch-local evaluator changes. Neither demonstrates safe organizational self-redesign. A skill edit can change authority despite being called “learning.” | Moderate | bound | “A proposed lesson that changes permissions, acceptance criteria, or mandatory review belongs to governed policy change, even when stored in a skill or playbook.” Preserve frozen active criteria and independent promotion anchors. |
| C5 | OI levels and autonomy levels measure distinct phenomena. Definition/boundary. | Qiu's bespoke scale measures organizational intelligence maturity; ASDLC's scale measures operational autonomy. Human steering explicitly confirms this distinction. Different L5 meanings are expected, not a conflict or a defect. No conversion is needed. | High | retain | “OI maturity describes organizational capability and governance; autonomy describes an agent's operational independence.” Describe the bespoke OI scale on its own terms, attributing it to Qiu and preserving its proposed status. Distinct constructs do not imply a demonstrated statistical independence. |
| C6 | Separate production and evaluation where consequential. Recommendation. | [Panickssery et al., 2024](https://arxiv.org/abs/2404.13076) tests self-recognition and preference in LLM evaluation. Direct for those biases, indirect for enterprise governance. A different session/model can still share blind spots; its necessity and sufficiency are not established for every action. | Moderate | bound | Keep risk-appropriate external checks and ground-truth evidence; do not claim that two agents establish correctness or that a human must approve every routine read. |
| C7 | Benchmark scores do not validate OI. Empirical boundary. | [TheAgentCompany v1](https://arxiv.org/html/2412.14161v1) verifies 24.0% full completion versus 34.4% partial credit in the original evaluation. [v3](https://arxiv.org/abs/2412.14161) reports 30% autonomous completion. Version, harness, tasks, and metric matter. Simulated task completion is not longitudinal organizational learning. | High for versioned figures; Insufficient for maturity validation | bound | If used, cite the exact version and metric. Prefer omitting these incidental figures from the concept. Do not present them as October 2026 capability ceilings. |
| C8 | Preserve established debt vocabulary. Definition. | [Storey](https://arxiv.org/abs/2603.22106) defines cognitive debt in shared understanding and intent debt in externalized rationale. Qiu's “comprehension debt” is adjacent; intent drift and absent rationale overlap without being identical. No evidence establishes a separate taxonomy node. | Moderate | retain | Use Cognitive Debt and Intent Debt with their incumbent definitions; explain local terminology differences only if needed. |
| C9 | Governance gates improve outcomes. Causal claim. | Qiu explicitly leaves necessity, sufficiency, and operating cost unresolved. No controlled organizational outcome comparison was found in this bounded search. Alternative: review latency and rubber-stamping can offset gains. | Insufficient | reject | Do not assert a measured effectiveness gain, validated maturity threshold, or guaranteed safety. Recommendations require evaluation against incidents, false accepts, reviewer effort, and delivery outcomes. |

### Truth arbitration and regression risks

The source can broaden the KB's organizing vocabulary without superseding its implementation patterns. The proposed concept must distinguish established meaning from this particular synthesis. OI levels are a distinct, bespoke scale for a different measured phenomenon from ASDLC autonomy. Their shared numbering creates no substantive disagreement and is not a reason to omit the OI scale. Evaluate its own construct definition, observable classification criteria, inter-rater reliability, and predictive usefulness. Those measurement properties remain unvalidated in the source.

Verification timing also needs precision: authorization precedes an irreversible action; postcondition checks follow execution or inspect a staged result. Review cannot make an already executed external action “not happen.” A failed check needs recovery or compensation where reversal is unavailable. This is editorial reasoning, not a result demonstrated by the essay.

No direct ASDLC citation was found in the fetched essay. Shared terminology alone establishes neither borrowing nor independent empirical confirmation.

### Incumbent citation re-verification

- Self-Harness authors and original June 8 submission verified; the current record is v3, August 20. The three-stage method supports the narrow proposal-loop account. No new performance number is proposed.
- RQGM authors and June 29 revision verified; first submission was June 24. The incumbent `published: 2026-06-29` is a revision date. Its abstract supports fixed criteria within epochs, not a guarantee of institutional safety. Keep ASDLC's human-governed constraints explicitly editorial.
- Storey's record has one author. The incumbent's “Storey et al.” should be corrected in a separately approved calibration; its “exponential increase” sentence is not established by the abstract and should not be reinforced here. Full-text appraisal is needed before any quantitative replacement.
- The Compound Loop has no external reference array. Its human gate is incumbent design policy, not an experimentally validated universal law.
- The whole bibliography was not re-audited. No new corroborating citation is proposed for the unrelated causal claims in Double Diamond or Context Gates.

### Search and Selection Record

- **Question/date:** Is the proposed concept distinct and are its governance/maturity claims evidenced? 2026-10-06.
- **Sources:** full source HTML and appendix; local content/specs/lessons/ledger; primary arXiv records; publisher-hosted organizational-design article.
- **Queries:** local searches for `organizational intelligence`, memory, promotion, authority, loops, independent verification, and debt; web searches for `"Designing the intelligent organization" "Kolbjørnsrud"` and `site:openmoss.ai "Organizational Intelligence" author`; direct source-citation followups.
- **Included:** conceptual source and prior term definition; primary evidence relevant to verification bias, context privacy, harness evolution, evaluator boundaries, benchmark interpretation, and debt definitions.
- **Excluded:** search-result mirrors when publisher material was available; unrelated papers from the large bibliography; unverified EnterpriseBench numbers; productivity or political-economy predictions not needed for this editorial decision.
- **Access limits:** guessed CMR URL initially failed; corrected publisher URL succeeded. DOI resolver failed initially; direct Zenodo record succeeded. Most supporting papers were checked at abstract/metadata level; TheAgentCompany v1 full HTML was checked. This is a targeted assessment, not a systematic literature review, exhaustive priority search, or full replication audit.

## C. Disagreement and Human Decision

### Disagreement Record

Primary extraction was completed before receiving the independent assessor's conclusions. The independent working draft is `docs/assessments/drafts/2026-10-06-openmoss-organizational-intelligence/independent.md` (local, gitignored). Same-model agreement is not evidence of correctness.

| Reviewer or role | Position | Evidence/rationale | Provisional adjudication |
|---|---|---|---|
| Primary | New concept plus two loop clarifications; initially emphasized level-number disambiguation and an autonomy graph edge. | Prior OI literature, corpus gap, incumbent loop contracts. | Retain core recommendation; revise scale framing after human steering. |
| Independent | Same verdict and integrations; favors harness/compound/optimization edges, with autonomy edge only if substantive. | Technical harness versus institutional embedding is a stronger teaching connection. | Adopt harness edge in place of autonomy edge; retain Agentic SDLC edge for the software-domain application. |
| Human steering | OI levels are independent of ASDLC autonomy: a bespoke scale measuring a different phenomenon. | Explicit user correction, 2026-10-06. | Accepted. Withdraw conflict framing. Include an attributed account of the OI scale on its own terms; assess its measurement validity independently. This is scope steering, not approval of the full assessment or implementation. |

No unresolved disagreement remains about the verdict or the two integrations. The user subsequently approved the original editorial package; the critic extension remains a proposal. Independent review additionally flagged that the incumbent Morris citation does not validate ASDLC's exact L3 mapping; that destination is no longer proposed for amendment and the citation issue remains outside this package.

### Human Decision

- **Reviewer:** Ville Takanen.
- **Decision/override:** approved the original recommendation on 2026-10-06 ("yeah, I agree"). Earlier correction that OI levels measure a distinct phenomenon is incorporated. The subsequent request to assess improvements to loop and critic materials is an extension under review, not blanket implementation approval.
- **Rationale and feedback applied:** the user values the quality and attributability of the loop definitions and asked whether these can improve loop and critic materials. Section D records the approved original package; a separate working addendum assesses the extension.
- **Execution boundary:** assessment finalization is approved. Article and skill implementation remains pending. No content or skill changes are included in this report.

## D. Knowledge Graph Impact and Action Plan

| # | Proposed action | Path | Type |
|---|---|---|---|
| 1 | Define Organizational Intelligence using prior literature; explain agentic interpretation, evidence limits, and maturity/autonomy distinction. | `src/content/concepts/organizational-intelligence.md` | CREATE |
| 2 | Clarify traces versus candidate lessons versus approved instructions, without weakening the existing gate. | `src/content/patterns/compound-loop.md` | INTEGRATE |
| 3 | Clarify that an edit affecting authority/evaluation is governed change regardless of storage format. | `src/content/patterns/agent-optimization-loop.md` | INTEGRATE |
| 4 | Add reciprocal substantive relationships from the new concept to Agentic SDLC, Harness Engineering, Compound Loop, and Agent Optimization Loop. | These four incumbent articles and the new concept | LINK |
| 5 | After human decision, file canonical assessment and append one ledger line with decision, profile, risk, confidence, and execution status. | `docs/assessments/2026-10-06-openmoss-organizational-intelligence.md`, `docs/assessments/ledger.jsonl` | LOG |

This package adds one node and four bidirectional relationships; two incumbents receive substantive clarifications and two receive relationship text. Qiu's existing OI scale can be described within the concept; no separate scale node or renumbering of ASDLC autonomy is proposed. No new memory product architecture or debt node is proposed. Existing target paths and their current `relatedIds` were inspected. New reciprocal edges must be added together during implementation; existing legacy graph defects are not silently absorbed into scope.

## E. Reviewable Content Scope

Concept outline: **Definition** (prior usage first), **Key Characteristics** (shared knowledge, coordinated action, accountability), **Agentic Interpretation** (attributed synthesis), **OI Maturity Levels** (the source's bespoke scale, with one sentence distinguishing its measured phenomenon), **Open Questions** (measurement, cost, and evidence), **ASDLC Usage** (one paragraph linking the four substantive neighbors). References belong in frontmatter; article body starts at H2. Use `status: Experimental` for the initial agentic synthesis, recognizing that this distributes it through the MCP and Field Manual surfaces.

The exact bounded integration wording is in C3–C4. The new page should distinguish organizational properties from promises about particular models. No article is drafted into `src/content/` during this assessment.

## F. Canonical Ledger Entry

Append one record after this approved report: `initial_verdict: synthesized`, `final_verdict: synthesized`, `risk_class: High`, `confidence: Moderate`, two-reviewer profile, the scale-independence correction, human approval, and `execution_status: pending`. Pending refers to content implementation, not the completed assessment. The later critic extension is not represented as approved.

## G. Reusable Learning and Verification

Candidate lesson: assess the effect of an instruction change, not whether its file is called memory, skill, or policy. Existing lessons already address most of this; no lessons-file update is proposed now.

`pnpm check` passed: 117 Astro files, zero errors/warnings, two existing deprecated-Server hints; 28 specs validated. The content check reports 149 documented legacy relationship defects. No published content changed. Reviewer drafts remain local and gitignored; this canonical assessment is tracked documentation.
