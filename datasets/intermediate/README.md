# Intermediate Tier Datasets

VitalDB slices, eICU samples, and other intermediate-level datasets.

## Dataset Policy

- **Size limit:** Files < 100MB committed; larger files use pointers
- **Format:** Parquet or CSV
- **Access:** PhysioNet credentialing required for eICU and VitalDB
- **Pointers:** Large datasets documented with generation queries

## Datasets

### vitaldb-cases.parquet (PLANNED)

VitalDB case metadata subset.

**Source:** VitalDB (https://vitaldb.net)

**Generation query:** Documented in module data README

**Planned for:** v0.7.0 Intermediate Week 2

### eicu-cohort.parquet (PLANNED)

eICU sample subset for Intermediate exercises.

**Source:** eICU Collaborative Research Database (PhysioNet)

**Cohort query:** Documented in module data README

**Planned for:** v0.7.0 Intermediate Week 5

---

*See main [datasets/README.md](../README.md) for full data policy and PhysioNet credentialing requirements.*
