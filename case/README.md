# C11 · Hydrogen-assisted fatigue of API 5L pipelines — W44–W47

> **Real industrial case dossier.** Copied from the authoritative case card in
> `CASES.md` §4 so this repository stays self-contained after it is pushed to
> GitHub. Planning links: [`CASES.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/CASES.md) ·
> [`JOURNALS.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/JOURNALS.md) ·
> [`WEEKLY_PLAN.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/WEEKLY_PLAN.md).
> **Evidence level: A** · No plant data is held in this repository.

**Repository:** `e11-icme-end-to-end` · **Evidence: A** ·
**References:** R01, R03, R31, Y2R13, D07.

**Industrial problem.** Reusing natural-gas pipelines for hydrogen accelerates
fatigue crack growth; operators need an auditable, reproducible assessment chain
before repurposing a line (Y2R13).

**Why it happens.** Hydrogen pressure and stress-intensity factor interact; models
that fit the tested pressures can fail badly at untested ones.

**Data (open, no plant data).** The public dataset and code accompanying Y2R13
(D07: `github.com/tRosJan/machine-learning-hydrogen-assisted-fatigue`) for API
5L X52, X70, X100. Record the commit hash and keep the original split.

**Tool chain.** ANN and RF reproduction → interpolation stress test at unseen
pressures → conformal error bands → Paris-law phenomenological comparator →
Snakemake/Prefect DAG chaining data → model → report → provenance manifest →
full-physics re-check of the final recommendation.

**What each reference validates.**
- Y2R13 — the industrial problem, public data/code, and external ANN/RF results.
- R01 — ICME P–S–P–P framework for the end-to-end chain.
- R03 — data-driven fourth-paradigm framing.
- R31 — V&V reporting and limitation language.
- D07 — repository URL, licence and commit pin.

**Deliverables.** `cases/h2_fatigue/`; per-grade parity plots; interpolation
table; one-page integrity-management caveat; `make all` DAG; provenance manifest.

**Validation.** Interpolation test executed exactly as described; low-pressure
degradation of accuracy reported; clean-state reproduction from a fresh clone.

**Acceptance.** No safety claim beyond the data range; the report says explicitly
this is **not** a fitness-for-service certificate.

## Claim boundary

See [`evidence.md`](evidence.md) for the evidence level and the exact wording
that must be used when quoting literature numbers. All datasets and references
are listed in [`sources.md`](sources.md); the four-week execution plan is in
[`week_plan.md`](week_plan.md).
