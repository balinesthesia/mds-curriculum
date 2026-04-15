# Architecture

Design decisions and rationale for the `mds-curriculum` repository.  
Read this before opening a PR or modifying curriculum structure.

---

## Audience

**Anesthesiology residents** at Universitas Udayana and affiliated hospitals.  
Entry requirement: clinical intelligence only. No prior statistics or programming assumed.  
Motivation lever: their own patient data, their own clinical questions.

---

## Design Principles

1. **Concept before tool.** Every module follows: Concept → Clinical context → Tool. Never Tool → Application.
2. **Clinical anchor is load-bearing, not decorative.** Toy datasets are prohibited. Every exercise uses real or realistic clinical data.
3. **Reproducibility as discipline, not afterthought.** Version control, environment management, and literate programming are introduced in Week 1 of Basic and never relaxed.
4. **Prediction vs inference is the central distinction.** This single concept separates the Basic researcher track from the Intermediate builder track and must be taught explicitly.
5. **AI-assisted workflows are taught critically.** AI tools enter at Advanced tier only. Residents learn what LLMs cannot catch before they learn to use them.

---

## Tier Design Rationale

### Why R for Basic

Clinical literature residents read is predominantly R-generated (`tableone`, `survival`, `ggplot2`). Teaching R at Basic means they can read and reproduce the code in papers they cite within weeks. Immediate clinical payoff drives retention at this tier.

### Why Python for Intermediate

The builder track opens at Intermediate. EHR wrangling, feature engineering, and prediction pipelines are better served by Python's ecosystem. `scikit-learn`, `lifelines`, `polars`, `shap` — no equivalent coherence in R for this workflow.

### Why Python + AI-assisted for Advanced

By Advanced, residents have enough foundation to use AI tools critically — as a supervised junior collaborator, not an oracle. Teaching AI-assisted workflows without this foundation produces tool dependency, not competency.

### Why 4–6 residents per cohort

Small enough for substantive capstone feedback. Large enough for meaningful peer review. At steady state (all three tiers running), 12–18 residents are in the system simultaneously.

---

## Platform Decisions

### Quarto

- Polyglot: R chunks in Basic, Python chunks in Intermediate/Advanced, single consistent site
- `quarto freeze` allows publishing without re-running code against data that cannot be publicly hosted
- Parameterized capstone templates scaffold resident documents without constraining content
- Single source renders to web (reading), PDF (printing), and presentation (in-person sessions)

### GitHub

- `github.com/balinesthesia` org is the single home — no second org
- GitHub Teams handle access control per cohort per tier
- Cohort repos are private; curriculum content repo is public
- Capstone archive is public (with resident consent)
- Facilitator handoff = team permission grant, not document transfer

### No LMS

Deliberate. An LMS adds a platform dependency and separates learning from tooling. Residents learn Git as infrastructure from Week 1. The curriculum lives where the work lives.

---

## Repository Governance

### Curriculum repo (`mds-curriculum`) — public

Owned by Balinesthesia org. Facilitators have write access. Residents have read access.  
All changes via PR. No direct commits to `main`.

### Cohort repos (e.g., `cohort-basic-01`) — private

One repo per cohort per tier. Resident teams have write access scoped to their capstone directory. Facilitator has full write access.  
Archived (not deleted) after cohort completion.

### Facilitator guide (`facilitator-guide`) — private

Write access: facilitators only. Contains rubrics, onboarding materials, session notes.  
Versioned in sync with curriculum via matching tags.

---

## Data Architecture

```
datasets/
├── basic/          # Curated, clean, versioned — committed to repo
├── intermediate/   # VitalDB slices, eICU samples — committed if <100MB, else pointers
└── advanced/       # MIMIC-IV pointers only
```

**MIMIC-IV policy:** Never committed. Modules assume a local `data/mimic-iv/` directory.  
Each module that uses MIMIC-IV includes a `data/README.md` specifying exact tables, columns, and cohort query used to generate the module dataset — ensuring reproducibility without distributing data.

**PhysioNet credentialing** for eICU and MIMIC-IV is a documented prerequisite handled during Intermediate onboarding (not a barrier to entry).

---

## Versioning and Cohort Records

Each cohort records:
- Curriculum version at cohort start (e.g., `v0.2.1`)
- Any known errata for that version
- Capstone archive link

This record lives in the cohort repo `README.md`. When a graduate becomes a facilitator, they can see exactly what changed between their cohort version and the current version.

---

## Facilitator Pipeline

```
Advanced cohort completion
        ↓
Facilitator onboarding (Weeks 23–24 of Advanced, concurrent with capstone)
        ↓
Junior facilitator: assigned to Basic cohort (supervised)
        ↓
Senior facilitator: assigned to Intermediate cohort
        ↓
Curriculum contributor: write access to mds-curriculum repo
```

This pipeline is the primary curriculum sustainability mechanism. It must be explicitly maintained — it does not self-perpetuate.

---

## Decisions Log

| Date | Decision | Rationale |
|---|---|---|
| 2026-04 | License: CC BY-NC 4.0 | Institutional curriculum, protect against commercial extraction while maximizing academic adoption |
| 2026-04 | Single GitHub org (balinesthesia) | Org already exists, institutional, Teams handle access control adequately |
| 2026-04 | No LMS | Toolchain coherence, Git as infrastructure from day one |
| 2026-04 | R for Basic, Python for Intermediate/Advanced | Clinical literature compatibility vs builder ecosystem fit |
| 2026-04 | Linear tier progression | Foundation integrity over speed, no lateral entry |
| 2026-04 | 4–6 residents per cohort | Capstone feedback quality, peer review viability |
