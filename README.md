# Governed AI for Regulated Industries

Position papers by Aejaz Sheriff Quaraishi on building AI systems that regulators, auditors and courts can examine case by case.

The papers share one design rule: **models propose, deterministic rules decide, and licensed humans sign.** Each applies that rule to a different problem, from health plan coverage decisions to clinical safety to enterprise governance programs, and each says what evidence the system should produce while it runs.

## Papers

| Paper | What it covers | Status |
| --- | --- | --- |
| [Three Frameworks, One Evidence Set](papers/three-frameworks-one-evidence-set.pdf) | Running NIST AI RMF, ISO/IEC 42001 and the EU AI Act off one evidence base. Crosswalk to clauses and articles, a reference architecture separating the system of record from the control plane, an implementation sequence, and a check of common framework claims. Credo AI is the worked example. | Version 2.0, November 2026 |
| Who Decided? Deterministic Safety for AI in Health Plan Utilization Management | An architecture for AI in prior authorization and utilization review where automation can't produce a denial and every determination leaves a sealed, replayable trace. Anchored on California SB 1120, Texas SB 815, CMS rules and recent litigation. | In preparation |
| A Policy Without a Control: Governance as Architecture for Enterprise AI | Governing delegated work instead of only models, a component-by-consequence tiering matrix, policy as code in an AI control plane, and value governance with a baseline before any benefit claim. | In preparation |
| The Human-in-the-Loop Illusion: Architectural Safety Guarantees for Clinical AI | Why human review is a poor primary safety mechanism for detecting rare AI errors, a symmetric failure-mode framework, and the architectural alternatives: safety envelopes, unconditional input and output checks, fail-closed defaults and calibrated abstention. | In preparation |

Papers marked "in preparation" will be added to `papers/` as they're finalized.

## Core ideas

**The Deterministic Safety Principle.** Probabilistic model output never directly drives a coverage determination, a dollar figure or a clinical decision. Exact values come from structured sources, determinations come from explicit and versioned criteria, and adverse outcomes come from accountable people.

**One evidence set.** Governance artifacts are produced once, where the work happens, tagged with the framework provisions they satisfy, and exported in each framework's terms. If a framework deliverable can't be generated from the shared record, the underlying evidence is missing.

**Tier by consequence.** A system's governance tier is set by the kind of AI component it uses and by what happens, and to whom, if it's wrong. A system takes the highest tier of any part it contains, and agents start at tier 2.

**Measure the oversight you rely on.** If a design depends on a person catching errors, the program should show how often that person actually does.

## Repository layout

```
.
├── papers/      Published PDFs
├── figures/     Source files for figures, where shareable
├── CHANGELOG.md Version history for each paper
└── README.md
```

## Related public work

- Sheriff A. [A deterministic safety pipeline for therapeutic AI in elderly assisted living](https://www.medrxiv.org/content/10.64898/2026.02.17.26346507v1). medRxiv preprint, February 2026. Bench evaluation, not a clinical study.
- [AI-Production-Checklist](https://github.com/asq-sheriff/AI-Production-Checklist): production readiness items mapped to NIST AI RMF, ISO/IEC 42001, the EU AI Act and OWASP LLM Top 10.

## Citing

Please cite the paper title, the version and the date shown on its cover, for example:

> Quaraishi, A. S. *Three Frameworks, One Evidence Set: Operationalizing NIST AI RMF, ISO/IEC 42001 and the EU AI Act.* Technical white paper, version 2.0, November 2026.

## Disclosures

These are independent position papers. They don't represent the views of any employer or client, and nothing here is legal advice. Regulatory summaries are current to the date on each paper and should be confirmed with counsel before they're relied on.

The author has no commercial relationship with any vendor named in these papers. Through his own company he has a commercial interest in a product that generates governance configuration and compliance evidence for AI coding agents, and he is the inventor on a pending US patent application covering a deterministic safety architecture for AI systems. Each paper carries its own disclosure where relevant.

## Corrections

Found an error or an out-of-date citation? Please open an issue with the paper, the section and the source that shows the correction. Fixes are recorded in `CHANGELOG.md`.

## Author

Aejaz Sheriff Quaraishi, enterprise and AI architect. [linkedin.com/in/asheriff](https://linkedin.com/in/asheriff)

## License

© 2026 Aejaz Sheriff Quaraishi. All rights reserved.
