# Hydrogen-assisted fatigue of API 5L pipelines (C11)

> Workspace folder: `e11-icme-end-to-end` · Suggested GitHub repository: `metallurgy-icme-pipeline`
> Epic: E11 · Weeks: W44–W47 · Evidence level: **A**
> Master specification: [`CASES.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/CASES.md) §4 · Download the papers: [`JOURNALS.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/JOURNALS.md)

## Industrial problem

Reusing natural-gas pipelines for hydrogen accelerates fatigue crack growth; operators need an auditable, reproducible assessment chain before repurposing a line.

**Why it happens.** Hydrogen pressure and stress-intensity factor interact; models that fit tested pressures can fail badly at untested ones.

## Data (no plant data)

Open data only: the public dataset and code accompanying Y2R13 (D07, `github.com/tRosJan/machine-learning-hydrogen-assisted-fatigue`) for API 5L X52, X70, X100. Record the commit hash and keep the original split. Evidence level A.

> The author cannot supply factory data. This project uses **only open datasets and
> credible peer-reviewed journals**. If this is a B-level case, the case report
> must contain the exact disclaimer from `CASES.md` §1 and must **never** claim
> plant validation.

## Tool chain

ANN and RF reproduction, interpolation stress test, conformal error bands, Paris-law phenomenological comparator, Snakemake/Prefect DAG, provenance manifest, `make all`, full-physics re-check.

## Journal references

- **Y2R13** — the industrial problem, public data/code, and external ANN/RF results.
- **R01** — ICME P–S–P–P framework for the end-to-end chain.
- **R03** — data-driven fourth-paradigm framing.
- **R31** — V&V reporting and limitation language.
- **D07** — repository URL, licence and commit pin.

Each reference above is listed with its DOI or stable URL, access status and
manual download route in [`JOURNALS.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/JOURNALS.md) §4, and in the shared
BibTeX library `papers/references.bib`. Do not cite a paper you have not been
able to obtain; if it is inaccessible, record that in `JOURNALS.md` §8.

## Deliverables

`cases/h2_fatigue/`; per-grade parity plots; interpolation table; one-page integrity-management caveat; `make all` DAG; provenance manifest; case report.

## Validation & claims

Interpolation test executed exactly as described; low-pressure degradation of accuracy reported; clean-state reproduction from a fresh clone.

## Limitations

No safety claim beyond the data range. This is NOT a fitness-for-service certificate.

## Definition of Done

1 merged PR · green tests · 1 new artefact · 1 README paragraph · 1 sprint note
`docs/sprints/wNN.md` · tag `wNN`. Before the case tag `c11` is created,
this README must contain all six sections: Industrial problem, Data (no plant
data), Tool chain, Journal references, Validation & claims, Limitations.

## Repository skeleton

Shared files: `CONTRIBUTING.md` (sprint contract), `.github/` (issue, PR and
CI templates), `docs/sprints/wNN.md`, `docs/vv_template.md` and
`docs/model_card.md`. `CASES.md`, `JOURNALS.md` and `REPOSITORIES.md` are in a
separate planning repository; their links above remain valid after this folder
is pushed as its own repository.

The real industrial case dossier is in `case/`: `README.md` (full case card),
`evidence.md`, `sources.md` and `week_plan.md`.

## Push this folder to GitHub

This folder is prepared but is **not** a Git repository yet:

```bash
cd e11-icme-end-to-end
git init
git branch -M main
git remote add origin https://github.com/<your-user>/metallurgy-icme-pipeline.git
git add .
git commit -m "Initial import: C11 · W44–W47"
git push -u origin main
```

Use weekly tags `wNN` and one case tag `c11` inside this repository.
Never commit API keys, raw downloaded datasets or publisher PDFs.

## Language

All artefacts in this repository are written in **English**.
