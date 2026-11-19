# Decision log

| Date | Decision | Options considered | Reason |
|---|---|---|---|
| 2026-11-02 | Project set up: GitHub repo, GEE noncommercial project, QGIS LTR | — | — |
| 2026-11-14 | Study city: Gurugram; unit of analysis: 500 m grid | Gurugram, Ahmedabad, Pune, Bhopal; wards vs grid | Least studied (~1,740 Scholar results vs 5,600–7,400); GMDA Net Zero 2050 plan as policy hook; 17 clear pre-monsoon scenes (2025); local ground-truthing possible. No public digital ward map and ward boundaries under revision, so 500 m grid used within the MCG boundary (Dec 2020 map). |
| 2026-11-15 | Study area digitised from MCG boundary map (28 Dec 2020) via georeferencing; 500 m grid (EPSG:32643) clipped to boundary | Trace by eye vs georeference | Georeferenced with 8 control points (highway/railway junctions), Polynomial 1; 1033 grid cells || 2026-11-16 | Treat bare land separately from built-up surfaces | Use NDBI alone as "built-up" | P04: rural/bare land hotter than urban by day in NCR; NDBI cannot separate bare soil from buildings |
| 2026-11-16 | Use OSM sector boundaries as a secondary, policy-friendly unit (tentative) | Grid only | Sector outlines exist in OpenStreetMap; enables grid-vs-sector MAUP check |
| 2026-11-17 | Use Dynamic World (10 m) to compute % trees, grass, crops, built, bare, water per cell | NDVI/NDBI only; ESA WorldCover | Separates bare vs built and trees vs grass; masks water; free in Earth Engine; continuously updated (P10) |
| 2026-11-19 | Q1 effect sizes: OLS | Correlation, random forest | Interpretable °C-per-unit effect; baseline for spatial tests; RF as robustness check |
| 2026-11-19 | Q2 clustering: Moran's I + LISA | Top-10%, Gi*, Geary's C | Detects clusters and outliers; comparable with P05; Gi* as robustness check |
| 2026-11-19 | Q3 spatial dependence: lag or error model | Ignore, location variables, robust SEs | Corrects effect size and uncertainty; choice by LM tests |
| 2026-11-19 | Q4 varying effects: MGWR (tentative) | Split by area, interactions, GWR | No predefined groups; MGWR reduces overfitting vs GWR (lesson from P05) |
| 2026-11-19 | Spatial error model preferred; also test Spatial Durbin | Spatial lag | Pilot: Robust LM error 316 > Robust LM lag 94; LM WX 165 suggests neighbours' land cover matters |
| 2026-11-19 | Refine RQ: built-up vs bare land vs vegetation as drivers | Keep "are greener areas cooler?" | Pilot: NDBI dominates (r = 0.77 with LST); NDVI effect falls 87% when NDBI added; NDBI conflates buildings and bare soil |
 
