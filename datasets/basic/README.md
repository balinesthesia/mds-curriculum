# Basic Tier Datasets

Curated, clean, versioned datasets for the Basic Tier. All files in this directory are committed to the repository.

## Dataset Policy

- **Size limit:** Each file < 10MB
- **Format:** CSV with data dictionary
- **Versioning:** Filename includes version (e.g., `propofol-doses-v1.csv`)
- **Source:** Anonymized/synthetic clinical data

## Datasets

### propofol-doses.csv (PLANNED)

Anonymized propofol induction doses with patient characteristics.

**Variables:** patient_id, weight_kg, age, asa_class, propofol_mg, case_duration_min

**Planned for:** v0.3.0 Basic Week 5 (EDA I)

### iop-map.csv (PLANNED)

Intraoperative MAP time series for 10+ cases.

**Variables:** case_id, timestamp_min, map_mmhg, event_annotation

**Planned for:** v0.3.0 Basic Week 6 (EDA II)

### icu-outcomes.csv (PLANNED)

ICU admission variables with 30-day mortality outcome.

**Variables:** patient_id, age, apache_ii, sofa_score, vasopressor_use, ventilated, mortality_30d

**Planned for:** v0.3.0 Basic Week 12 (Logistic Regression)

---

*See main [datasets/README.md](../README.md) for full data policy.*
