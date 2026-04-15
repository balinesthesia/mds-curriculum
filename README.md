# mds-curriculum

**Balinesthesia Medical Data Science Curriculum**  
Anesthesiology and Intensive Therapy Study Program  
Faculty of Medicine, Universitas Udayana

---

## Overview

A tiered, cohort-based curriculum bridging traditional clinical statistics and modern data science for anesthesiology residents. Built around reproducibility, causal reasoning, and real clinical datasets.

This curriculum is **not** a generic data science course. Every concept is anchored to anesthesia and critical care practice. Residents leave as researchers who can build, or builders who can publish.

---

## Curriculum Structure

| Tier | Duration | Language | Goal |
|---|---|---|---|
| Basic | 16 weeks | R | Critical consumer + reproducible researcher |
| Intermediate | 20 weeks | Python | Independent analyst, researcher/builder entry |
| Advanced | 24 weeks | Python + AI-assisted | Clinical tool builder or preprint-ready researcher |

**Progression:** Linear. Basic → Intermediate → Advanced.  
**Cohort size:** 4–6 residents per cohort.  
**Cadence:** Rolling. All three tiers run concurrently at steady state.  
**Contact hours:** 2 hours/week.  
**Assessment:** Capstone project per tier.

---

## Capstone Deliverables

- **Basic** — Quarto report reproducing and critiquing a published anesthesia paper + R code on GitHub
- **Intermediate** — Quarto manuscript + reproducible Python pipeline using VitalDB or eICU
- **Advanced** — Deployed clinical tool prototype **or** preprint-ready manuscript (builder/researcher track)

---

## Repository Structure

```
mds-curriculum/
├── basic/
│   ├── week-01/
│   │   ├── index.qmd          # Resident-facing module
│   │   ├── facilitator.qmd    # Facilitator notes
│   │   └── data/              # Module dataset or pointer
│   └── ...
├── intermediate/
├── advanced/
├── datasets/
│   ├── basic/
│   ├── intermediate/
│   └── advanced/              # MIMIC-IV pointers only — data not stored here
├── facilitator/
│   ├── onboarding.qmd
│   └── rubrics/
├── capstone-archive/          # Past cohort capstones (with consent)
├── _quarto.yml
└── ARCHITECTURE.md
```

---

## Datasets

| Tier | Dataset | Access |
|---|---|---|
| Basic | Curated synthetic/public anesthesia datasets | Open |
| Intermediate | VitalDB, eICU-CRD | Open / PhysioNet credentialed |
| Advanced | MIMIC-IV | PhysioNet credentialed (local copy required) |

> MIMIC-IV data is **never** committed to this repository. Modules use relative paths against a local `data/` directory which is `.gitignore`d. Reproducibility is guaranteed by code, not data.

---

## Facilitator Model

Advanced graduates are trained as junior facilitators. Facilitator onboarding is documented in `facilitator/onboarding.qmd` and versioned with the curriculum. Facilitator handoff is a repo permission grant, not a document transfer.

---

## Versioning

This curriculum follows [Semantic Versioning](https://semver.org):

- **Patch** — typo fix, broken link, dataset pointer update
- **Minor** — module content revision, new exercise, facilitator note addition
- **Major** — tier restructure, language change, capstone brief rewrite

Each cohort records the curriculum version they completed.

---

## License

[Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](LICENSE)

Free to use and adapt for non-commercial academic and clinical education purposes with attribution. Commercial use requires explicit written permission from Balinesthesia.

Attribution: **Balinesthesia — Anesthesiology and Intensive Therapy Study Program, Faculty of Medicine, Universitas Udayana**

---

## Contributing

This curriculum is maintained by Balinesthesia. Contributions from Advanced graduates and external collaborators are welcome via pull request.

See `ARCHITECTURE.md` for design decisions and rationale before opening a PR.
