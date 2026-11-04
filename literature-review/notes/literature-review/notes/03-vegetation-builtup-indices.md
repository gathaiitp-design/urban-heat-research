# Note 03 — Vegetation and Built-up Indices
Sources: NASA Earth Observatory, Measuring Vegetation; Zha, Gao & Ni (2003) (accessed 2026-11-04)

## Key concepts
- **Spectral signature:** each surface reflects/absorbs wavelengths differently.
- **NDVI = (NIR − Red) / (NIR + Red)** — vegetation greenness
  - < 0 water · 0–0.2 concrete/soil · 0.2–0.4 sparse vegetation · > 0.5 dense vegetation
- **NDBI = (SWIR1 − NIR) / (SWIR1 + NIR)** — built-up intensity
  - Positive = built-up · Negative = vegetation/water

## Landsat 8/9 bands
| Band | GEE name | Used for |
|---|---|---|
| B4 Red | SR_B4 | NDVI |
| B5 NIR | SR_B5 | NDVI, NDBI |
| B6 SWIR1 | SR_B6 | NDBI |

Reflectance scaling: **value × 0.0000275 − 0.2** (apply before computing indices).

## Pitfalls in cities
- NDVI can't separate **trees from grass** — cooling differs
- NDBI confuses **bare soil/construction with buildings** — check with land-cover data or high-res imagery
- NDVI is **seasonal** — compare like seasons
- **Water** lowers NDVI and LST → mask with MNDWI
- **Mixed pixels** at 30 m
- NDVI and NDBI are **collinear** → check correlation and VIF before regression

## Project link
- LST = outcome. NDVI and NDBI = explanatory variables.
