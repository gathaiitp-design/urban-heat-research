# Data inventory

| Dataset | Source | Licence | Resolution | Period | Date accessed | Notes |
|---|---|---|---|---|---|---|
| MCG boundary map (PDF) | Haryana ULB Dept., https://ulbharyana.gov.in/Website/DynamicUploadContent/CONTENTFILES/8586aee2-d4da-4e1d-9356-549d14457813.pdf | Government publication | — | Dated 28 Dec 2020 | 2026-11-15 | Georeferenced and digitised in QGIS |
| Landsat 8/9 Collection 2 Level-2 (SR + ST) | USGS via Google Earth Engine | Public domain | 30 m (thermal ~100 m) | Mar–May 2025 | 2026-11-15 | CLOUD_COVER < 10%, QA_PIXEL mask |
 
## Update (2026-11-17 to 2026-11-19)
 
### New evidence
- Indian UHI research concentrates on megacities (Delhi most studied, 13%); smaller cities, equity and policy links are under-studied (P06)
- Arid/semi-arid cities can be cooler than bare surroundings by day and warmer at night; such climates are under-studied (P07)
- Interventions work differently by neighbourhood (trees vs cool roofs) → spatially targeted policy (P08)
- NDVI is an imperfect vegetation measure; LST–vegetation relationship changes with scale (P09)
- Dynamic World separates built, bare, trees, grass, water at 10 m (P10)
 
### Additional gap
5. Semi-arid and non-megacity Indian cities are under-studied (P06, P07)
 
### Additional design implications
- Use Dynamic World to compute % trees, grass, built, bare, water per cell
- Expect possible daytime surface cool island vs bare surroundings; choose any rural reference carefully
- Match interventions to area type (P08) → priority areas by dominant driver
- Test robustness at 250 m, 500 m and 1 km (P09, MAUP)
 
### Pilot evidence (2026-11-19)
- Residual Moran's I = 0.57 → non-spatial methods (used in P01, P02) overstate certainty → method gap confirmed with data
- NDBI dominates (r = 0.77); NDVI's independent effect small → separating bare land from built-up is now the central question
 
