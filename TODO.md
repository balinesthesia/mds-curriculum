# TODO

Atomic task list for `Medical Data Science Curriculum` development.  
Follows [Semantic Versioning](https://semver.org). Each milestone maps to a deliverable state.  
Update this file via PR only. Mark tasks `[x]` on completion.

---

## v0.1.0 — Repository Foundation
> Deliverable: Repo is publicly accessible, licensed, structured, and navigable. No curriculum content yet.

### Infrastructure
- [x] Initialize `mds-curriculum` repo under `github.com/balinesthesia`
- [x] Add `LICENSE` (CC BY-NC 4.0 full text)
- [x] Add `README.md`
- [x] Add `ARCHITECTURE.md`
- [x] Add `TODO.md` (this file)
- [x] Add `.gitignore` (R, Python, Quarto, data directories)
- [x] Add `_quarto.yml` (site scaffold, no content pages yet)
- [x] Add `CHANGELOG.md` (empty, versioned from v0.1.0)
- [x] Create directory skeleton: `basic/`, `intermediate/`, `advanced/`, `datasets/`, `facilitator/`, `capstone-archive/`, `certificate/`
- [x] Add placeholder `README.md` in each top-level directory
- [x] Add `certificate/REGISTRY.yaml` — empty registry with schema comment
- [x] Add `certificate/params-example.yml` — example parameter file for template
- [x] Configure GitHub Pages deployment (source: `docs/` on `main`)
- [x] Verify site renders and deploys on push to `main`

> **Note:** `intro/` directory was considered but not implemented — site uses `index.qmd` as landing page instead.

### GitHub Org Setup
- [x] Create GitHub Team: `facilitators` — write access to `mds-curriculum` and `facilitator-guide`
- [x] Create GitHub Team: `basic-cohort-template` — read access to `mds-curriculum`
- [x] Document team permission model in `ARCHITECTURE.md`
> **Note:** `intermediate-cohort-template` and `advanced-cohort-template` teams are created at their respective tier milestones (v0.8.0 and v0.10.0), not v0.1.0.
- [x] Create private repo `facilitator-guide` under `balinesthesia` org
- [x] Add `facilitator-guide/README.md` with access and purpose description

---

## v0.2.0 — Introductory Course Content Draft
> Deliverable: All 4 Intro modules authored as `.qmd` files, unreviewed. No prior knowledge assumed.

### Environment and Setup
- [x] Author `facilitator/intro-setup-guide.qmd` — pre-session checklist: OS requirements, installation steps for R, RStudio/VSCode, Quarto, Git, GitHub account
- [x] Author `facilitator/intro-verification-checklist.qmd` — "setup works" confirmation items; must pass before Week 1
- [x] Author `intro/index.qmd` — course overview, learning goals, zero-assumption framing (renamed from README.md)

### Module Authoring — Introductory Course
- [x] `intro/week-01/index.qmd` — Command line basics; terminal, file system, paths, navigation
  - [x] Facilitator notes: `intro/week-01/facilitator.qmd`
  - [x] Exercise: navigate to a directory, create a folder, move and rename a file — all via terminal
- [x] `intro/week-02/index.qmd` — Git and GitHub fundamentals; clone, commit, push; GitHub account setup
  - [x] Facilitator notes: `intro/week-02/facilitator.qmd`
  - [x] Exercise: clone the `mds-curriculum` repo, make a small edit, commit and push to a personal fork
- [x] `intro/week-03/index.qmd` — R + RStudio/VSCode orientation; Quarto basics; render a document
  - [x] Facilitator notes: `intro/week-03/facilitator.qmd`
  - [x] Exercise: create a `.qmd` file with one code chunk and one text section; render to HTML; push to GitHub
- [x] `intro/week-04/index.qmd` — Core programming concepts; variables, data types, functions, reading/writing files; basic statistics refresher (mean, median, variance, distributions, p-value intuition — no code)
  - [x] Facilitator notes: `intro/week-04/facilitator.qmd`
  - [x] Exercise: load a CSV file in R, compute summary statistics, write results to a new file

---

## v0.3.0 — Basic Tier Content Draft
> Deliverable: All 16 Basic modules authored as `.qmd` files, unreviewed. Capstone brief drafted.

### Environment and Setup
- [x] Author `facilitator/setup-guide.qmd` — pre-session resident setup checklist (R, RStudio/VSCode, Quarto, Git, GitHub account)
- [x] Author `facilitator/verification-checklist.qmd` — "setup works" confirmation items
- [x] Author `basic/README.md` — tier overview, learning goals, dataset index

### Module Authoring — Basic Tier
- [x] `basic/week-01/index.qmd` — Environment & Philosophy; reproducibility rationale; Retraction Watch framing
  - [x] Facilitator notes: `basic/week-01/facilitator.qmd`
  - [x] Exercise: inspect a retracted anesthesia paper, identify the methodological failure
- [ ] `basic/week-02/index.qmd` — R + Quarto + GitHub basics; literate programming concept
  - [ ] Facilitator notes: `basic/week-02/facilitator.qmd`
  - [ ] Exercise: create a `.qmd` file, render to HTML, push to GitHub
- [ ] `basic/week-03/index.qmd` — Data structures & tidy data; observation vs variable
  - [ ] Facilitator notes: `basic/week-03/facilitator.qmd`
  - [ ] Exercise: tidy a messy anesthesia chart exported as CSV
- [ ] `basic/week-04/index.qmd` — Clinical data types; continuous, ordinal, nominal, time-to-event
  - [ ] Facilitator notes: `basic/week-04/facilitator.qmd`
  - [ ] Exercise: classify SOFA score components by data type; justify choices
- [ ] `basic/week-05/index.qmd` — EDA I: distributions, shape, spread, outliers
  - [ ] Facilitator notes: `basic/week-05/facilitator.qmd`
  - [ ] Exercise: describe propofol dose distribution across a curated case dataset
- [ ] `basic/week-06/index.qmd` — EDA II: ggplot2, visual thinking
  - [ ] Facilitator notes: `basic/week-06/facilitator.qmd`
  - [ ] Exercise: plot intraoperative MAP over time for 10 cases; annotate events
- [ ] `basic/week-07/index.qmd` — Table 1; `tableone`, descriptive statistics
  - [ ] Facilitator notes: `basic/week-07/facilitator.qmd`
  - [ ] Exercise: reproduce Table 1 from a resident-chosen anesthesia RCT
- [ ] `basic/week-08/index.qmd` — Inference philosophy; hypothesis, error types, effect sizes
  - [ ] Facilitator notes: `basic/week-08/facilitator.qmd`
  - [ ] Exercise: calculate effect size (Cohen's d) for a drug comparison; compare to p-value conclusion
- [ ] `basic/week-09/index.qmd` — Comparing groups; t-test, Mann-Whitney, framing as tools
  - [ ] Facilitator notes: `basic/week-09/facilitator.qmd`
  - [ ] Exercise: compare remifentanil dose between GA and regional cases; justify test choice
- [ ] `basic/week-10/index.qmd` — Categorical outcomes; chi-square, Fisher, odds ratios
  - [ ] Facilitator notes: `basic/week-10/facilitator.qmd`
  - [ ] Exercise: calculate PONV rate by anesthetic technique; compute OR with CI
- [ ] `basic/week-11/index.qmd` — Linear regression; estimation, interpretation, assumptions
  - [ ] Facilitator notes: `basic/week-11/facilitator.qmd`
  - [ ] Exercise: predict estimated blood loss from case features; check assumptions
- [ ] `basic/week-12/index.qmd` — Logistic regression; probability output, odds ratios
  - [ ] Facilitator notes: `basic/week-12/facilitator.qmd`
  - [ ] Exercise: model 30-day mortality from ICU admission variables
- [ ] `basic/week-13/index.qmd` — Survival basics; KM curves, log-rank, hazard concept
  - [ ] Facilitator notes: `basic/week-13/facilitator.qmd`
  - [ ] Exercise: KM curve for ICU length of stay; compare two patient groups
- [ ] `basic/week-14/index.qmd` — Study design; RCT, cohort, case-control, their limits
  - [ ] Facilitator notes: `basic/week-14/facilitator.qmd`
  - [ ] Exercise: classify 5 anesthesia papers by design; identify one limitation each
- [ ] `basic/week-15/index.qmd` — Capstone workshop; guided working session
  - [ ] Facilitator notes: `basic/week-15/facilitator.qmd`
- [ ] `basic/week-16/index.qmd` — Capstone submission and peer review
  - [ ] Facilitator notes: `basic/week-16/facilitator.qmd`

### Basic Capstone
- [ ] Author `basic/capstone/brief.qmd` — instructions, scope, selection criteria for target paper
- [ ] Author `basic/capstone/template.qmd` — parameterized Quarto template for submission
- [ ] Author `basic/capstone/rubric.md` — evaluation criteria (add to `facilitator-guide` repo)

### Basic Datasets
- [ ] Curate `datasets/basic/propofol-doses.csv` — anonymized/synthetic dose data with data dictionary
- [ ] Curate `datasets/basic/iop-map.csv` — intraoperative MAP time series, 10 cases minimum
- [ ] Curate `datasets/basic/icu-outcomes.csv` — ICU admission variables with 30-day mortality outcome
- [ ] Add `datasets/basic/README.md` — source, variables, known limitations for each dataset

---

## v0.4.0 — Basic Tier Internal Review
> Deliverable: All Basic modules reviewed by at least one clinical + one methodological reviewer. Errata resolved.

- [ ] Identify clinical reviewer (anesthesia staff)
- [ ] Identify methodological reviewer (biostatistics or epidemiology)
- [ ] Open GitHub Issues for each module requiring revision
- [ ] Resolve all critical issues (factual errors, broken exercises, missing data)
- [ ] Resolve all major issues (concept clarity, clinical anchor accuracy)
- [ ] Tag `v0.4.0` after all issues closed
- [ ] Update `CHANGELOG.md`

---

## v0.5.0 — Basic Tier Cohort Infrastructure
> Deliverable: Everything needed to run the first Basic cohort, including facilitator guide, cohort repo, and certificate template.

- [ ] Author `facilitator/onboarding.qmd` — facilitator role, responsibilities, session format
- [ ] Author `facilitator/basic-guide.qmd` — per-module facilitation notes compiled
- [ ] Create private repo `cohort-basic-01` under `balinesthesia` org
- [ ] Add `cohort-basic-01/README.md` — cohort record: curriculum version, resident roster (anonymized), dates
- [ ] Create GitHub Team `basic-cohort-01` — scoped to `cohort-basic-01` write + `mds-curriculum` read
- [ ] Author resident onboarding email template (in `facilitator-guide`)
- [ ] Dry-run Week 1 setup guide with at least one non-technical tester
- [ ] Document dry-run findings as GitHub Issues; resolve before cohort start
- [ ] Author `certificate/template.qmd` — parameterized Quarto PDF; fields: recipient name, tier, cohort, date, curriculum version, certificate ID
- [ ] Add `certificate/design-reference.html` — self-contained HTML mockup for visual design review and stakeholder sign-off
- [ ] Add `certificate/assets/` — program logo, HoD signature scans (two signatories)
- [ ] Test certificate PDF render end-to-end against example params

---

## v0.6.0 — Basic Tier First Cohort Delivery
> Deliverable: First Basic cohort completed, capstones submitted, certificates issued, post-cohort revisions captured.

- [ ] Deliver 16-week Basic cohort
- [ ] Collect per-module feedback from residents after each session
- [ ] Log friction points as GitHub Issues during delivery (do not fix mid-cohort)
- [ ] Complete capstone peer review (Week 16)
- [ ] Archive capstones to `capstone-archive/basic-cohort-01/` (with resident consent)
- [ ] Post-cohort review: triage all Issues into patch/minor/major
- [ ] Apply all patch and minor revisions
- [ ] Issue certificates for all capstone-passing residents
  - [ ] Generate parameterized PDF per resident from `certificate/template.qmd`
  - [ ] Append each record to `certificate/REGISTRY.yaml` (ID, tier, cohort, curriculum version, capstone URL, date)
- [ ] Update `CHANGELOG.md`
- [ ] Tag `v0.6.0`

---

## v0.7.0 — Intermediate Tier Content Draft
> Deliverable: All 20 Intermediate modules authored. Capstone brief drafted.

### Environment
- [ ] Author `intermediate/README.md` — tier overview, R-to-Python transition framing, dataset index
- [ ] Author `facilitator/intermediate-transition.qmd` — guidance for residents moving from R to Python

### Module Authoring — Intermediate Tier
- [ ] `intermediate/week-01/index.qmd` — Python environment; uv, Jupyter, R-to-Python transition
  - [ ] Facilitator notes: `intermediate/week-01/facilitator.qmd`
  - [ ] Exercise: replicate a Basic week-11 linear regression in Python; compare output
- [ ] `intermediate/week-02/index.qmd` — Pandas/Polars fundamentals; DataFrames, indexing, pipes
  - [ ] Facilitator notes: `intermediate/week-02/facilitator.qmd`
  - [ ] Exercise: load and index VitalDB case metadata; answer 5 clinical questions using DataFrame operations
- [ ] `intermediate/week-03/index.qmd` — Data wrangling I; merging, reshaping, type casting
  - [ ] Facilitator notes: `intermediate/week-03/facilitator.qmd`
  - [ ] Exercise: join OR log table to intraoperative vital signs table; resolve key mismatches
- [ ] `intermediate/week-04/index.qmd` — Data wrangling II; missing data patterns, MAR/MCAR/MNAR
  - [ ] Facilitator notes: `intermediate/week-04/facilitator.qmd`
  - [ ] Exercise: characterize missingness in an ICU dataset; classify each variable's pattern with justification
- [ ] `intermediate/week-05/index.qmd` — EDA in Python; plotly, seaborn, profiling
  - [ ] Facilitator notes: `intermediate/week-05/facilitator.qmd`
  - [ ] Exercise: produce an EDA profile report for an eICU patient cohort; identify two data quality issues
- [ ] `intermediate/week-06/index.qmd` — Prediction vs Inference; the fundamental distinction
  - [ ] Facilitator notes: `intermediate/week-06/facilitator.qmd`
  - [ ] Exercise: classify 6 clinical research questions as prediction or inference; justify each
- [ ] `intermediate/week-07/index.qmd` — Feature engineering; clinical domain knowledge as feature design
  - [ ] Facilitator notes: `intermediate/week-07/facilitator.qmd`
  - [ ] Exercise: engineer time-to-intubation, cumulative dose, and delta-MAP features from raw VitalDB signals
- [ ] `intermediate/week-08/index.qmd` — Regression as prediction; train/test, cross-validation, metrics
  - [ ] Facilitator notes: `intermediate/week-08/facilitator.qmd`
  - [ ] Exercise: predict extubation timing using cross-validated linear regression; report RMSE and MAE
- [ ] `intermediate/week-09/index.qmd` — Classification models; logistic regression, decision tree, random forest
  - [ ] Facilitator notes: `intermediate/week-09/facilitator.qmd`
  - [ ] Exercise: build three classifiers for postop AKI; compare performance on held-out test set
- [ ] `intermediate/week-10/index.qmd` — Clinical risk scores; building vs validating vs applying
  - [ ] Facilitator notes: `intermediate/week-10/facilitator.qmd`
  - [ ] Exercise: reconstruct APACHE II from MIMIC-IV variables; validate against documented scores
- [ ] `intermediate/week-11/index.qmd` — Model evaluation; ROC, AUC, calibration, Brier score
  - [ ] Facilitator notes: `intermediate/week-11/facilitator.qmd`
  - [ ] Exercise: evaluate week-09 AKI classifier with full calibration analysis; explain why AUC alone is insufficient
- [ ] `intermediate/week-12/index.qmd` — Survival in Python; lifelines, Cox regression
  - [ ] Facilitator notes: `intermediate/week-12/facilitator.qmd`
  - [ ] Exercise: reproduce a KM curve from a published critical care paper using eICU data
- [ ] `intermediate/week-13/index.qmd` — Longitudinal data; mixed models, repeated measures
  - [ ] Facilitator notes: `intermediate/week-13/facilitator.qmd`
  - [ ] Exercise: model serial lactate trajectory in sepsis using a linear mixed model
- [ ] `intermediate/week-14/index.qmd` — Missing data strategies; imputation, sensitivity analysis
  - [ ] Facilitator notes: `intermediate/week-14/facilitator.qmd`
  - [ ] Exercise: apply three imputation strategies to MIMIC missing data; compare downstream model performance
- [ ] `intermediate/week-15/index.qmd` — Interpretability; SHAP, feature importance, partial dependence
  - [ ] Facilitator notes: `intermediate/week-15/facilitator.qmd`
  - [ ] Exercise: generate SHAP summary plot for week-09 AKI model; translate top features into clinical language
- [ ] `intermediate/week-16/index.qmd` — Subgroup analysis; interaction terms, effect modification
  - [ ] Facilitator notes: `intermediate/week-16/facilitator.qmd`
  - [ ] Exercise: test whether AKI model performance differs by age group and surgical category
- [ ] `intermediate/week-17/index.qmd` — Reproducible pipelines; Git discipline, uv, Quarto + Python
  - [ ] Facilitator notes: `intermediate/week-17/facilitator.qmd`
  - [ ] Exercise: refactor week-09 notebook into a documented pipeline a stranger can re-run from scratch
- [ ] `intermediate/week-18/index.qmd` — Research communication; tables, figures, supplement structure
  - [ ] Facilitator notes: `intermediate/week-18/facilitator.qmd`
  - [ ] Exercise: produce a journal-ready Table 2 and Figure 1 from the week-09 pipeline output
- [ ] `intermediate/week-19/index.qmd` — Capstone workshop; guided working session
  - [ ] Facilitator notes: `intermediate/week-19/facilitator.qmd`
- [ ] `intermediate/week-20/index.qmd` — Capstone submission and peer review
  - [ ] Facilitator notes: `intermediate/week-20/facilitator.qmd`

### Intermediate Capstone
- [ ] Author `intermediate/capstone/brief.qmd`
- [ ] Author `intermediate/capstone/template.qmd`
- [ ] Author `intermediate/capstone/rubric.md`

### Intermediate Datasets
- [ ] Document VitalDB access and slice generation procedure
- [ ] Curate eICU sample subset for Intermediate exercises (cohort query documented)
- [ ] Add `datasets/intermediate/README.md`

---

## v0.8.0 — Intermediate Tier Review + Cohort Infrastructure
> Mirrors v0.4.0 + v0.5.0 process for Intermediate tier.

- [ ] Clinical and methodological review of all 20 modules
- [ ] Resolve all critical and major issues
- [ ] Author `facilitator/intermediate-guide.qmd`
- [ ] Create GitHub Team: `intermediate-cohort-template` — read access to `mds-curriculum`
- [ ] Create `cohort-intermediate-01` private repo and team
- [ ] Dry-run Week 1 Python environment setup
- [ ] Issue certificates for all Intermediate capstone-passing residents
  - [ ] Generate parameterized PDF per resident from `certificate/template.qmd`
  - [ ] Append each record to `certificate/REGISTRY.yaml` (ID, tier, cohort, curriculum version, capstone URL, date)
- [ ] Tag `v0.8.0`

---

## v0.9.0 — Advanced Tier Content Draft
> Deliverable: All 24 Advanced modules authored, both builder and researcher tracks scaffolded.

### Module Authoring — Advanced Tier
- [ ] `advanced/week-01/index.qmd` — Causal inference I; DAGs, d-separation, confounding
  - [ ] Facilitator notes: `advanced/week-01/facilitator.qmd`
  - [ ] Exercise: draw a DAG for the relationship between anesthetic choice, patient severity, and mortality; identify confounders
- [ ] `advanced/week-02/index.qmd` — Causal inference II; propensity scores, matching, IPW
  - [ ] Facilitator notes: `advanced/week-02/facilitator.qmd`
  - [ ] Exercise: compare anesthetic techniques in observational MIMIC-IV data using propensity score matching
- [ ] `advanced/week-03/index.qmd` — Causal inference III; instrumental variables, DiD, RDD
  - [ ] Facilitator notes: `advanced/week-03/facilitator.qmd`
  - [ ] Exercise: identify a natural experiment in a provided clinical dataset; justify instrument validity
- [ ] `advanced/week-04/index.qmd` — Sensitivity analysis; unmeasured confounding, E-values
  - [ ] Facilitator notes: `advanced/week-04/facilitator.qmd`
  - [ ] Exercise: calculate E-value for a week-02 result; interpret in clinical terms
- [ ] `advanced/week-05/index.qmd` — Bayesian thinking I; prior, likelihood, posterior — conceptual
  - [ ] Facilitator notes: `advanced/week-05/facilitator.qmd`
  - [ ] Exercise: update a prior belief about vasopressor response given simulated intraop data; no code required
- [ ] `advanced/week-06/index.qmd` — Bayesian thinking II; PyMC/Stan in practice
  - [ ] Facilitator notes: `advanced/week-06/facilitator.qmd`
  - [ ] Exercise: fit a Bayesian logistic regression for AKI using PyMC; compare posterior to frequentist result
- [ ] `advanced/week-07/index.qmd` — Bayesian thinking III; credible intervals, posterior predictive checks
  - [ ] Facilitator notes: `advanced/week-07/facilitator.qmd`
  - [ ] Exercise: report week-06 results in clinical journal format using credible intervals
- [ ] `advanced/week-08/index.qmd` — MIMIC-IV deep dive; data structure, credentialing, temporal tables
  - [ ] Facilitator notes: `advanced/week-08/facilitator.qmd`
  - [ ] Exercise: build a de novo ICU cohort from MIMIC-IV using inclusion/exclusion criteria from a published paper
- [ ] `advanced/week-09/index.qmd` — Temporal data I; time-series concepts, stationarity, resampling
  - [ ] Facilitator notes: `advanced/week-09/facilitator.qmd`
  - [ ] Exercise: preprocess a raw arterial line waveform from VitalDB; handle stationarity and resampling
- [ ] `advanced/week-10/index.qmd` — Temporal data II; waveform feature extraction from VitalDB
  - [ ] Facilitator notes: `advanced/week-10/facilitator.qmd`
  - [ ] Exercise: extract five clinically meaningful features from high-frequency VitalDB signals; document rationale
- [ ] `advanced/week-11/index.qmd` — AI-assisted workflow I; capabilities and limitations
  - [ ] Facilitator notes: `advanced/week-11/facilitator.qmd`
  - [ ] Exercise: use an LLM to generate a data wrangling script; audit the output for correctness and assumptions
- [ ] `advanced/week-12/index.qmd` — AI-assisted workflow II; failure modes — leakage, confounding
  - [ ] Facilitator notes: `advanced/week-12/facilitator.qmd`
  - [ ] Exercise: given an LLM-generated analysis with an embedded label leakage error, identify and fix it
- [ ] `advanced/week-13/index.qmd` — AI-assisted workflow III; structured prompting for analysis tasks
  - [ ] Facilitator notes: `advanced/week-13/facilitator.qmd`
  - [ ] Exercise: develop a reusable prompt template for a specific analysis task; test and document failure modes
- [ ] `advanced/week-14/index.qmd` — Clinical NLP basics; unstructured notes, tokenization, embeddings
  - [ ] Facilitator notes: `advanced/week-14/facilitator.qmd`
  - [ ] Exercise: extract structured features from 20 anesthesia notes using a simple NLP pipeline
- [ ] `advanced/week-15-builder/index.qmd` — Clinical tool architecture; validation frameworks, deployment reality
  - [ ] Facilitator notes: `advanced/week-15-builder/facilitator.qmd`
  - [ ] Exercise: define architecture and validation plan for capstone tool
- [ ] `advanced/week-15-researcher/index.qmd` — Preprint structure; bioRxiv/medRxiv norms, submission workflow
  - [ ] Facilitator notes: `advanced/week-15-researcher/facilitator.qmd`
  - [ ] Exercise: outline capstone manuscript to preprint standard
- [ ] `advanced/week-16-builder/index.qmd` — Build iteration; supervised working session
  - [ ] Facilitator notes: `advanced/week-16-builder/facilitator.qmd`
- [ ] `advanced/week-16-researcher/index.qmd` — Manuscript draft; supervised working session
  - [ ] Facilitator notes: `advanced/week-16-researcher/facilitator.qmd`
- [ ] `advanced/week-17-builder/index.qmd` — Deployment thinking; drift, monitoring, clinical integration reality
  - [ ] Facilitator notes: `advanced/week-17-builder/facilitator.qmd`
  - [ ] Exercise: write a model monitoring plan for your capstone tool
- [ ] `advanced/week-17-researcher/index.qmd` — Causal communication; presenting uncertainty to non-statisticians
  - [ ] Facilitator notes: `advanced/week-17-researcher/facilitator.qmd`
  - [ ] Exercise: present findings from capstone draft to a simulated department audience; receive structured feedback
- [ ] `advanced/week-18/index.qmd` — Capstone development week 1; progress check + facilitator feedback
  - [ ] Facilitator notes: `advanced/week-18/facilitator.qmd`
- [ ] `advanced/week-19/index.qmd` — Capstone development week 2; progress check + facilitator feedback
  - [ ] Facilitator notes: `advanced/week-19/facilitator.qmd`
- [ ] `advanced/week-20/index.qmd` — Capstone development week 3; progress check + facilitator feedback
  - [ ] Facilitator notes: `advanced/week-20/facilitator.qmd`
- [ ] `advanced/week-21/index.qmd` — Capstone development week 4; progress check + facilitator feedback
  - [ ] Facilitator notes: `advanced/week-21/facilitator.qmd`
- [ ] `advanced/week-22/index.qmd` — Capstone development week 5; final pre-submission check
  - [ ] Facilitator notes: `advanced/week-22/facilitator.qmd`
- [ ] `advanced/week-23/index.qmd` — Capstone peer review + facilitator onboarding session 1
  - [ ] Facilitator notes: `advanced/week-23/facilitator.qmd`
- [ ] `advanced/week-24/index.qmd` — Capstone submission + facilitator onboarding session 2
  - [ ] Facilitator notes: `advanced/week-24/facilitator.qmd`

### Advanced Capstone
- [ ] Author `advanced/capstone/brief.qmd` — builder and researcher tracks documented separately
- [ ] Author `advanced/capstone/builder-template.qmd`
- [ ] Author `advanced/capstone/researcher-template.qmd`
- [ ] Author `advanced/capstone/rubric.md`

### Facilitator Onboarding (embedded in Advanced Weeks 23–24)
- [ ] Author `facilitator/advanced-onboarding.qmd` — role expectations, cohort management, feedback rubrics
- [ ] Define facilitator graduation criteria (what makes an Advanced graduate ready to facilitate)
- [ ] Add facilitator onboarding to `ARCHITECTURE.md` pipeline section

### Advanced Datasets
- [ ] Document MIMIC-IV local directory convention and `.gitignore` policy
- [ ] Author data dictionary pointers for all Advanced MIMIC-IV modules
- [ ] Add `datasets/advanced/README.md`

---

## v0.10.0 — Advanced Tier Review + Cohort Infrastructure
> Mirrors v0.4.0 + v0.5.0 process for Advanced tier.

- [ ] Clinical, methodological, and AI/ethics review of all 24 modules
- [ ] Resolve all critical and major issues
- [ ] Author `facilitator/advanced-guide.qmd`
- [ ] Create GitHub Team: `advanced-cohort-template` — read access to `mds-curriculum`
- [ ] Create `cohort-advanced-01` private repo and team
- [ ] Issue certificates for all Advanced capstone-passing residents
  - [ ] Generate parameterized PDF per resident from `certificate/template.qmd`
  - [ ] Append each record to `certificate/REGISTRY.yaml` (ID, tier, cohort, curriculum version, capstone URL, date)
- [ ] Tag `v0.10.0`

---

## v1.0.0 — Full Curriculum Stable
> Deliverable: All tiers delivered at least once, post-cohort revisions applied, facilitator pipeline operational.

- [ ] Intro Course: minimum one cohort completed and revised
- [ ] Basic Tier: minimum one cohort completed and revised
- [ ] Intermediate Tier: minimum one cohort completed and revised
- [ ] Advanced Tier: minimum one cohort completed and revised
- [ ] Minimum one Advanced graduate active as junior facilitator
- [ ] Capstone archive contains at least one entry per tier
- [ ] All facilitator guides reviewed by active facilitators
- [ ] Site renders cleanly across all tiers with no broken links or missing data pointers
- [ ] `CHANGELOG.md` complete from v0.1.0 through v1.0.0
- [ ] Public announcement (Balinesthesia website, academic network)
- [ ] Tag `v1.0.0`

---

## Backlog (Post v1.0.0)

- [ ] Indonesian language track (module translation)
- [ ] Cross-institution cohort (collaborative delivery with other residency programs)
- [ ] Integration with `IJAMI` (Indonesia Journal of Augmented Medical Intelligence) for Advanced Research track capstone publication (coming soon)
- [ ] Automated Quarto site CI/CD (GitHub Actions on push to `main`)
- [ ] Dataset versioning with DVC or equivalent
- [ ] Advanced Tier expansion: waveform deep learning module (VitalDB)
- [ ] Peer-reviewed publication describing the curriculum design and outcomes
