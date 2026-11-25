# Hydrogen-assisted fatigue of API 5L pipelines (C11)

## Industrial problem

Reusing natural-gas pipelines for hydrogen accelerates fatigue crack growth; operators need an auditable, reproducible assessment chain before repurposing a line.

**Why it happens.** Hydrogen pressure and stress-intensity factor interact; models that fit tested pressures can fail badly at untested ones.

## Data (no plant data)

Open data only: the public dataset and code accompanying Y2R13 (D07, `github.com/tRosJan/machine-learning-hydrogen-assisted-fatigue`) for API 5L X52, X70, X100. Record the commit hash and keep the original split.

> Only open datasets and published literature are used. No plant or proprietary data are held here; plant numbers quoted from papers are external literature, not independently reproduced results.

## Tool chain

ANN and RF reproduction, interpolation stress test, conformal error bands, Paris-law phenomenological comparator, Snakemake/Prefect DAG, provenance manifest, `make all`, full-physics re-check.

## Journal references

- **Y2R13** ([DOI](https://doi.org/10.1016/j.commatsci.2025.114207)) — the industrial problem, public data/code, and external ANN/RF results.
- **R01** ([DOI](https://doi.org/10.1126/science.277.5330.1237)) — ICME P–S–P–P framework for the end-to-end chain.
- **R03** ([DOI](https://doi.org/10.1063/1.4946894)) — data-driven fourth-paradigm framing.
- **R31** — V&V reporting and limitation language.
- **D07** ([source](https://github.com/tRosJan/machine-learning-hydrogen-assisted-fatigue)) — repository URL, licence and commit pin.

## Deliverables

`cases/h2_fatigue/`; per-grade parity plots; interpolation table; one-page integrity-management caveat; `make all` DAG; provenance manifest; case report.

## Validation & claims

Interpolation test executed exactly as described; low-pressure degradation of accuracy reported; clean-state reproduction from a fresh clone.

## Limitations

No safety claim beyond the data range. This is NOT a fitness-for-service certificate.

## Repository layout

- `README.md` — case summary, data policy, method, results and limitations.
- `CONTRIBUTING.md` — how to propose changes.
- `docs/index.md` — documentation map.
- `docs/model_card.md` and `docs/vv_template.md` — reporting templates.
- `.github/workflows/ci.yml` — automated checks.

Only open data and published literature are used. No plant or proprietary data
are included. All artefacts are written in English.
