---
title: "Theory of LLM Constraints"
longTitle: "Theory of LLM Constraints: Why Coding-Side Acceleration Doesn't Deliver"
description: "Applying Goldratt's Theory of Constraints to AI delivery. Coding-side speed shifts bottlenecks downstream; the ASDLC answer is proportional verification from a minimal context-specific scaffold."
tags:
  - Theory
  - Productivity
  - Metrics
  - Bottlenecks
  - Industrialization
status: "Experimental"
publishedDate: 2026-05-18
lastUpdated: 2026-10-01
relatedIds:
  - concepts/agentic-sdlc
  - concepts/feedback-loop-compression
  - concepts/pr-slop
  - concepts/ai-amplification
  - patterns/context-gates
  - practices/adversarial-code-review
references:
  - type: "website"
    title: "Theory of LLM Constraints"
    author: "Mats Ljunggren"
    url: "https://www.linkedin.com/pulse/theory-llm-constraints-mats-ljunggren-qmzde/"
    published: 2026-05-12
    accessed: 2026-05-18
    annotation: "Applies Goldratt's Theory of Constraints to LLM-augmented delivery; synthesizes Faros, Thoughtworks, DORA, and METR telemetry into the bottleneck-shift thesis."
  - type: "website"
    title: "The AI Productivity Paradox Report 2025"
    author: "Faros AI"
    url: "https://www.faros.ai/blog/ai-software-engineering"
    published: 2025-07-23
    accessed: 2026-10-01
    annotation: "Observational telemetry across 10,000+ developers and 1,255 teams using Spearman rank correlation against AI usage. 98% more PRs merged, 91% PR review time increase, 154% larger PRs, 9% more bugs. Correlational; not a causal estimate."
  - type: "website"
    title: "How much faster can coding assistants really make software delivery?"
    author: "Sichu Zhang (Thoughtworks)"
    url: "https://www.thoughtworks.com/en-us/insights/blog/generative-ai/how-faster-coding-assistants-software-delivery"
    published: 2025-02-18
    accessed: 2026-10-01
    annotation: "Client case using estimated task savings across 150 tracked tickets and a cycle-time heuristic: ~30% estimated coding-task improvement yields ~8% estimated cycle-time improvement because development was ~55% of team time. Team estimates, not measured telemetry."
  - type: "website"
    title: "2025 DORA Report: State of AI-Assisted Software Development"
    author: "Google Cloud / DORA"
    url: "https://dora.dev/dora-report-2025/"
    published: 2025-10-01
    accessed: 2026-05-18
    annotation: "First official benchmarks for Deployment Rework Rate, the 5th DORA metric — the quality-leakage signal complementing PR Cycle Time."
  - type: "website"
    title: "Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity"
    author: "METR"
    url: "https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study"
    published: 2025-07-10
    accessed: 2026-05-18
    annotation: "RCT finding experienced open-source developers were 19% slower (CI +2% to +39%) with early-2025 AI tools while perceiving themselves as faster. Measures task completion time, not downstream delivery."
  - type: "website"
    title: "We are Changing our Developer Productivity Experiment Design"
    author: "METR"
    url: "https://metr.org/blog/2026-02-24-uplift-update/"
    published: 2026-02-24
    accessed: 2026-10-01
    annotation: "METR's own update: the early-2025 slowdown is a historical, tool-specific result; selection bias and concurrent-agent measurement problems make the current uplift estimate unreliable, and developers are likely more sped up now than in early 2025."
  - type: "website"
    title: "Coding Is No Longer the Constraint: Scaling Developer Experience to Teams and Agents at Spotify"
    author: "Spotify Engineering (Niklas Gustavsson)"
    url: "https://engineering.atspotify.com/2026/6/code-with-claude-coding-is-no-longer-the-constraint"
    published: 2026-06-03
    accessed: 2026-09-30
    annotation: "First-party operational account from a Code with Claude talk: 76% more PRs, constraint moving to review and prioritization, auto-merge of safe changes. Self-reported figures without methods; delivered at a vendor event with a product pitch."
  - type: "website"
    title: "AI Changed How Spotify Builds. What We Learned (and Fixed) About Quality at Higher Velocity"
    author: "Spotify Engineering (Tyson Singer)"
    url: "https://engineering.atspotify.com/2026/9/ai-changed-how-spotify-builds-what-we-learned-and-fixed-about-quality-at-higher-velocity"
    published: 2026-09-16
    accessed: 2026-09-30
    annotation: "Spotify's quality retrospective: merged changes roughly doubled year over year with no rise in rework rate, while complexity and PR size crept up and automated fleet updates that passed checks failed in production. States the constraint moved to verification capacity."
---

## Definition

The **Theory of LLM Constraints** is the application of Eliyahu Goldratt's *Theory of Constraints* (TOC) to AI-assisted software delivery. Its central claim: because LLMs collapse the marginal cost of code generation, the system bottleneck structurally shifts from the **coding station** to **review, integration, and validation**. Local optimization at the coding station produces little end-to-end throughput improvement on its own.

The thesis is consistent with heterogeneous evidence that measures different outcomes in different settings. A Thoughtworks client case *estimates* that ~30% coding-task acceleration yields ~8% cycle-time improvement, because development was about half of team time. Faros telemetry across 10,000+ developers reports a *correlation* between AI adoption and 98% more PRs merged, a 91% increase in PR review time, and PRs 154% larger on average. METR's early-2025 randomized trial measured experienced open-source developers 19% slower on *task completion time* with the tools of that period, while reporting they felt faster; METR has since stated that its current uplift estimate is unreliable and that developers are likely faster now. None of these is a measurement of a moved queue, but together they motivate measuring the whole delivery process rather than the coding station. The constraint moved. Most teams did not.

## The Diagnostic: Where the Constraint Moves

In a traditional SDLC, coding is one constraint among several. When LLMs accelerate it, three things happen at once:

- **Inventory build-up at review.** PR queues lengthen. Faros: 98% more PRs, 154% larger on average (correlational).
- **Quality leakage.** Faros: 9% more bugs per developer (correlational). DORA 2025 publishes the first official benchmarks for *Deployment Rework Rate* — the ratio of deployments that are unplanned responses to a production incident.
- **Perceived velocity diverges from measured velocity.** METR's early-2025 RCT found experienced developers 19% *slower* on task time with the tools of that period while reporting they felt faster. The dashboard and the timesheet disagree, even if the gap has since narrowed.

A first-party case from Spotify (2026) illustrates the shift at scale. After near-universal adoption of AI coding tools, Spotify reports 76% more pull requests, with merged changes roughly doubling year over year. Its response is the Subordinate step in practice: auto-merge what is safe, focus human review where it matters, and rethink planning and prioritization. Its own retrospective reports no rise in rework rate so far, alongside warning signals of creeping complexity and PR size and automated fleet updates that passed checks but failed in production. In Spotify's words: "AI increased the capacity to produce change. The next constraint became our ability to verify it." These are self-reported figures from an organization with years of prior investment in standardization and an internal developer portal; they illustrate the diagnosis, not a transferable effect size.

The constraint is no longer "how fast can the human type." It is "how fast can the system verify intent."

## Two System-Level Diagnostics

| Signal | What it measures | What it surfaces |
|---|---|---|
| **PR Cycle Time** | Elapsed time through the pull-request workflow (review / integration) | Where inventory accumulates |
| **Deployment Rework Rate** (DORA 5th metric) | Share of deployments that are unplanned responses to a production incident | Where the constraint is being bypassed rather than respected |

Tracking only the first invites the Faster Horse: throughput goes up while rework hides the cost. Tracking both keeps the dialectic honest.

## The Dialectic: Classical TOC vs. ASDLC

Goldratt's Five Focusing Steps prescribe: **identify the constraint, exploit it, subordinate everything else, elevate it, repeat when it moves.** Applied naively to PR queue saturation, "elevate" means *add reviewer capacity, parallelize review, accelerate human approval*.

This is the [Faster Horse Fallacy](/concepts/agentic-sdlc). It optimizes the broken station rather than redesigning the line. The ASDLC accepts Goldratt's *diagnostic* and rejects his *classical cure*:

| Step | Classical TOC remediation | ASDLC structural remediation |
|---|---|---|
| Identify | Coding is no longer the constraint; review is. | Same. |
| Exploit | Squeeze every drop from existing reviewers. | Reduce review surface via [Micro-Commits](/practices/micro-commits) and [Specs](/patterns/the-spec). |
| Subordinate | Cap upstream PR generation to match review capacity. | Cap *unverified* generation; let verified generation run. |
| **Elevate** | **Add reviewers, parallelize review, AI-assist review.** | **Replace peer review with inspection stations** — [Adversarial Code Review](/practices/adversarial-code-review), [Context Gates](/patterns/context-gates), [Constitutional Review](/practices/constitutional-review-implementation). |
| Repeat | When review is no longer the constraint, find the next one. | Same — production observability via [Feedback Loop Compression](/concepts/feedback-loop-compression). |

The substitution at *Elevate* is the entire point. Adding reviewers is linear; structural verification is multiplicative. This is the same position [PR Slop](/concepts/pr-slop) takes from a different angle: "PR slop cannot be solved by reviewing harder."

## Minimal Scaffolding: Proportional Gates

A common prescriptive response to the constraint shift is **Scaffolding-First Development**: pre-building the validation surface (tests, NFRs, CI/CD) before generating feature code. This invokes Deming's "build quality in, don't inspect it in" at agent speed.

The ASDLC adopts a refined stance: **Minimal Scaffolding-First**.

For any given context (e.g., a TypeScript web application), there is a sensible, minimal scaffold that should always be used from the outset. This baseline includes essential constraints like compilation checks, type-checking, and basic syntactical linting.

However, beyond this minimal baseline, we must **avoid overtly adding scaffolding**. The ASDLC is opinionated on having the *minimal, and only the minimal*, scaffold to start. Additional gates should not be added as a ritual playbook; they must **earn their place by protecting against a specific, identified risk**.

A gate that does not sit on the constraint or protect against a named risk represents overproduction of validation inventory (unsubordinated capacity).

- **Minimal Baseline (Start here):** Context-specific, low-cost guards (e.g., type-checkers, basic compiler checks).
- **Proportional Additions (Earn their place):** Additional gates (e.g., visual regression tests, performance-budget checkers, custom security policies) are built only when a concrete failure mode is identified.

- A linter is a no-brainer: the cost is near-zero and the failure modes it catches (syntax errors, dead code, style drift) are broadly identified across all code.
- A type-checker is a no-brainer in a typed language for the same reason.
- A unit test suite for a payment-handling module earns its place the moment the module exists, because the risk surface is concrete and named.
- A design-system drift check earns its place once the design system is load-bearing and the divergence risk is concrete and named — not as default infrastructure.
- A performance-regression gate earns its place once the system has a named performance contract and an identified path to breaching it.

This is not anti-discipline. It is the recognition that **a gate that does not sit on the constraint costs more than it saves**, and that the constraint moves. Building gates is itself a form of work; the work is subject to the same proportionality TOC and Lean prescribe for any other process step. The discipline is in the analysis that identifies the risk, not in the ritual of building every gate the playbook names.

## ASDLC Usage

This concept gives the ASDLC's bottleneck-shift thesis a theoretical name (Goldratt's TOC) and a body of heterogeneous evidence relevant to the constraint hypothesis (Faros / Thoughtworks / DORA 2025 / METR / Spotify), each carrying its own design and limits. It positions the ASDLC's verification architecture as *the structural answer* to the constraint shift, distinguishing it from two regressive defaults the industry will otherwise reach for:

1. **Classical TOC elevation** — adding reviewer capacity. Optimizes the broken station.
2. **Strong Scaffolding-First** — pre-built canonical gates. Overproduces verification inventory.

The ASDLC answer is proportional structural verification starting from a context-specific minimal scaffold, introducing additional gates only as they earn their place.

See also: [Feedback Loop Compression](/concepts/feedback-loop-compression) (the OODA-framed view of the same shift), [PR Slop](/concepts/pr-slop) (the quality-leakage manifestation), [AI Amplification](/concepts/ai-amplification) (why bad processes amplify under AI), [Context Gates](/patterns/context-gates) (how proportional gates are layered in practice).
