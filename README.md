# Urban Heat, Green Infrastructure and Climate Vulnerability

A geospatial assessment of neighbourhood-level surface heat risk in **[CITY — TBD]**.

## Research question
How do vegetation, built-up density and other urban characteristics relate to land-surface temperature (LST) patterns across neighbourhoods, and which areas should be prioritised for heat-resilience interventions?

> Note: satellite-derived land-surface temperature is **not** air temperature or experienced heat. This project is explicit about that distinction throughout.

## Status
- [ ] Phase 1 — Research problem defined
- [ ] Phase 2 — Scientific foundation
- [ ] Phase 3 — Methodology
- [ ] Phase 4 — Data collection & validation
- [ ] Phase 5 — Analysis
- [ ] Phase 6 — Intervention priorities
- [ ] Phase 7 — Outputs (report, policy brief, presentation)

## Repository structure
| Folder | Contents |
|---|---|
| `research-proposal/` | Research question, hypotheses, study design |
| `literature-review/` | Literature matrix, reading notes, research-gap log |
| `data/raw/` | Raw downloads (not committed — see data README) |
| `data/processed/` | Small cleaned outputs used in analysis |
| `notebooks/` | Exploratory analysis |
| `scripts/` | Reproducible processing and analysis code |
| `maps/` | Exported maps |
| `results/` | Tables, statistics, figures |
| `manuscript/` | Research paper drafts |
| `policy-brief/` | Two-page policy brief |
| `docs/` | Decision log, data inventory |

## Data sources
Documented in `docs/data-inventory.md` (source, licence, date accessed, processing notes).

## Reproducing the analysis
```bash
pip install -r requirements.txt
earthengine authenticate
```

## Author
Parishi — independent research.
