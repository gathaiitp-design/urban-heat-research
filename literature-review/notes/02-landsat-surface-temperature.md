# Note 02 — Landsat Land-Surface Temperature
Source: USGS, Landsat Collection 2 Surface Temperature (accessed 2026-11-03)

## Key concepts
- Satellite measures **thermal radiation**, not temperature directly.
- Stefan–Boltzmann: **E = εσT⁴** → same temperature, different emissivity (ε) → different signal.
- **Brightness temperature** (assumes ε = 1) ≠ **LST** (corrected).
- Two corrections: **atmospheric** (water vapour) and **emissivity** (surface material).

## Product facts — Landsat 8/9 Collection 2 Level-2
| Item | Value |
|---|---|
| Band | ST_B10 |
| Resolution | ~100 m native, resampled to 30 m |
| Scaling | value × 0.00341802 + 149.0 = K; − 273.15 = °C |
| Revisit | 16 days per satellite, ~8 days combined |
| Overpass | ~10:00–10:30 am local |
| QA bands | ST_QA (uncertainty), ST_CDIST (distance to cloud), QA_PIXEL (cloud mask) |

Example: 44,000 → 299.39 K → **26.24 °C**. Always sanity-check the range.

## Limitations
- Surface only (roofs, canopy tops) — not air, walls or street level
- Mixed pixels at ~100 m
- Clear-sky only; one morning snapshot
- Humid/pre-monsoon air → larger correction → more uncertainty
- Thin clouds can slip past the mask → pixels read too cold
- Emissivity based on older land-cover data → errors in fast-changing areas

## Project link
- Prefer dry, clear seasons (e.g., Mar–Apr in north India) for lower uncertainty.
