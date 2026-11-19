# Pilot analysis results (2026-11-19)
Pre-monsoon 2025 · 500 m grid · Gurugram MCG boundary

⚠️ Pilot only: no water mask, no bare-land separation, one year, edge cells unfiltered

## OLS: LST ~ NDVI + NDBI
| Term | Coef | Std err | p |
|---|---|---|---|
| Intercept | 41.45 | 0.132 | < 0.001 |
| NDVI | −1.01 | 0.458 | 0.028 |
| NDBI | 27.60 | 0.818 | < 0.001 |

- R² = 0.594; condition number = 9.6
- NDVI only: coef = −7.86 (+0.1 NDVI → 0.8 °C cooler)

## Correlations
| | LST | NDVI | NDBI |
|---|---|---|---|
| LST | 1.00 | −0.38 | 0.77 |
| NDVI | −0.38 | 1.00 | −0.44 |
| NDBI | 0.77 | −0.44 | 1.00 |

NDVI–NDBI r = −0.44 → VIF ≈ 1.2 → multicollinearity not the issue.

## Spatial diagnostics
- Moran's I (LST) = 0.691, p = 0.001 → strong clustering
- Moran's I (OLS residuals) = 0.569, p = 0.001 → OLS inadequate
- LM lag 928; LM error 1,150; Robust LM lag 94; Robust LM error 316 → spatial error model preferred
- LM WX 165 → neighbours' land cover matters → test Spatial Durbin model

## Interpretation
- Surface type (NDBI) dominates: +0.1 NDBI → 2.8 °C hotter
- Vegetation's independent effect small once NDBI included (falls 87%)
- Hottest cells concentrated in west/south-west (to verify which sectors)
- NDBI conflates buildings and bare soil → separating them is now the central question
- Non-spatial methods would overstate certainty → method gap confirmed

## Next
- Add Dynamic World land-cover shares, water mask, filter edge cells
- Fit spatial error and Spatial Durbin models
- LISA cluster counts and map (pending)
