# Certificate of Competency

Issuance system for tier completion certificates.

---

## Signatories

- **Koordinator Program Studi** — Prof. Dr. dr. Tjokorda Gde Agung Senapathi, SpAn-TI, Subsp.A.R (K)
- **Kepala Divisi Data Science dan Artificial Intelligence** — dr. I Made Agus Kresna Sucandra, SpAn-TI, Subsp.T.I (K)

## Files

| File | Purpose |
|------|---------|
| `template.qmd` | Parameterized Quarto PDF template |
| `params-example.yml` | Example parameter file for generation |
| `design-reference.html` | Visual design mockup for stakeholder review |
| `assets/` | Program logo, signature scans |
| `REGISTRY.yaml` | Public verification registry |

## Verification

Every certificate carries a unique ID resolvable at:
`https://balinesthesia.github.io/mds-curriculum/verify`

Query against `REGISTRY.yaml` for: ID, tier, cohort, curriculum version, capstone URL, date.

## Generation Workflow

1. Populate `params.yml` per resident
2. Render: `quarto render template.qmd --metadata-file params.yml`
3. Append record to `REGISTRY.yaml`
4. Distribute PDF to resident

---

*Issued by Division of Data Science and Artificial Intelligence, FK Udayana.*
