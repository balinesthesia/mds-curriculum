# Advanced Tier Datasets

MIMIC-IV pointers and local data conventions only. No clinical data is committed to this repository.

## Dataset Policy

- **Never committed:** MIMIC-IV data remains on your local machine only
- **Pointers only:** Modules reference `data/mimic-iv/` in your local environment
- **Reproducibility:** Each module includes exact cohort query in its data README
- **Credentialing:** PhysioNet credentialing required (CITI training, data use agreement)

## Local Directory Convention

```
mds-curriculum/
├── data/
│   └── mimic-iv/
│       ├── hosp/        # Hospital module tables
│       ├── icu/         # ICU module tables
│       └── ed/          # Emergency department tables
```

Add `data/` to your local `.gitignore` — never commit clinical data.

## Module-Specific Cohort Queries

Each Advanced module that uses MIMIC-IV includes:
- Exact inclusion/exclusion criteria
- SQL query to generate the module dataset
- Expected row counts for verification

**Example:** See `advanced/week-08/data/README.md` (coming in v0.9.0)

---

*See main [datasets/README.md](../README.md) for full data policy and PhysioNet credentialing requirements.*
