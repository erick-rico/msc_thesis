# References and notes – Stage 5

## Data sources

### Air quality

RAMA – Red Automática de Monitoreo Atmosférico  
Mexico City air-quality monitoring network

https://www.aire.cdmx.gob.mx/

Daily station data aggregated to city-wide PM diagnostics.

---

### Atmospheric reanalysis

NARR – North American Regional Reanalysis (NOAA PSL)

https://psl.noaa.gov/data/gridded/data.narr.html

Core variables used in Stage 5:

- 500 hPa geopotential height (Z500)
- 500 hPa zonal wind (U500)
- 500 hPa meridional wind (V500)
- daily precipitation

Supporting lower-tropospheric fields from earlier stages remain relevant for interpretation, but Stage 5 does not reopen them as a central branch.

---

### ENSO classification

CPC Relative Oceanic Niño Index (RONI) – NOAA Climate Prediction Center

https://www.cpc.ncep.noaa.gov/products/analysis_monitoring/enso/roni/

Stage 5 uses the CPC seasonal RONI framework to classify season-years into:

- **El Niño**
- **Neutral**
- **La Niña**

This keeps the ENSO stratification operationally consistent and avoids building a separate ad hoc phase table inside the notebook.

---

## Literature used for Stage 5 interpretation

### Nucleus: synoptic regimes / recurrent polluted-day circulation states

1. Díaz-Esteban, Y., Barrett, B. S., & Raga, G. B. (2022). *Circulation patterns influencing the concentration of pollutants in central Mexico.* Atmospheric Environment, 274, 118976. https://doi.org/10.1016/J.ATMOSENV.2022.118976

2. Jeong, Y. C., Yeh, S. W., Jeong, J. I., Park, R. J., Yoo, C., & Yoon, J. H. (2023). *Intrinsic atmospheric circulation patterns associated with high PM2.5 concentration days in South Korea during the cold season.* Science of The Total Environment, 863, 160878. https://doi.org/10.1016/j.scitotenv.2022.160878

3. Lee, D., Kim, H. C., Jeong, J. H., Kim, B. M., Lee, D. G., Choi, J. Y., Song, M. Y., & Yoon, J. H. (2022). *Relationship Between Synoptic Weather Pattern and Surface Particulate Matter (PM) Concentration During Winter and Spring Seasons Over South Korea.* Journal of Geophysical Research: Atmospheres, 127(24), e2022JD037517. https://doi.org/10.1029/2022JD037517

---

### Basin ventilation / local-circulation support

4. Salcido, A., Carreón-Sierra, S., & Celada-Murillo, A. T. (2019). *Air Pollution Flow Patterns in the Mexico City Region.* Climate 2019, Vol. 7, Page 128, 7(11), 128. https://doi.org/10.3390/CLI7110128

5. Jauregui Ostos, E., & Luyando, E. (1992). *Patrones de flujo de aire superficial y su relación con el transporte de contaminantes en el valle de México.* Investigaciones Geográficas, 24, 51–78. https://doi.org/10.14350/RIG.59008

6. Burgos-Cuevas, A., Adams, D. K., García-Franco, J. L., & Ruiz-Angulo, A. (2021). *A Seasonal Climatology of the Mexico City Atmospheric Boundary Layer.* Boundary-Layer Meteorology 2021 180:1, 180(1), 131–154. https://doi.org/10.1007/S10546-021-00615-3

---

### Source-seasonality and interpretation caveats

7. Querol, X., Pey, J., Minguillón, M. C., Pérez, N., Alastuey, A., Viana, M., Moreno, T., Bernabé, R. M., Blanco, S., Cárdenas, B., Vega, E., Sosa, G., Escalona, S., Ruiz, H., & Artíñano, B. (2008). *PM speciation and sources in Mexico during the MILAGRO-2006 campaign.* Atmospheric Chemistry and Physics, 8(1), 111–128. https://doi.org/10.5194/acp-8-111-2008

8. Mugica, V., Ortiz, E., Molina, L., De Vizcaya-Ruiz, A., Nebot, A., Quintana, R., Aguilar, J., & Alcántara, E. (2009). *PM composition and source reconciliation in Mexico City.* Atmospheric Environment, 43(32), 5068–5074. https://doi.org/10.1016/j.atmosenv.2009.06.051

9. Raga, G. B., Ladino, L. A., Baumgardner, D., Ramirez-Romero, C., Córdoba, F., Alvarez-Ospina, H., Rosas, D., Amador, T., Miranda, J., Rosas, I., Jaramillo, A., Yakobi-Hancock, J., Kim, J. S., Martínez, L., Salinas, E., & Figueroa, B. (2021). *ADABBOY: African Dust And Biomass Burning Over Yucatan.* Bulletin of the American Meteorological Society, 102(8), E1543–E1556. https://doi.org/10.1175/BAMS-D-20-0172.1

---

## Notes on the Stage 5 seasonal framework

Stage 5 does **not** redefine polluted extremes season by season from scratch.

Instead, the logic is:

1. define extreme days within each **calendar month** using the monthly p90 framework inherited from earlier stages,
2. define **episode onset** as the first day of each p90 episode,
3. and then regroup those already-defined monthly onset days into **DJF / MAM / JJA / SON**.

This was done deliberately to preserve comparability with the monthly baseline-to-extremes logic established in Stage 3 while still answering the season-based request that motivated the final stage.

---

## Notes on day 0 and lag structure

Stage 5 keeps the strict event-centered sampling rule from Stage 4:

> **day 0 = first day of the p90 episode**

Lag composites are then built for:

> **−3, −2, −1, 0, +1, +2 days relative to onset**

Interpretive purpose:

- determine whether a seasonal signal is already visible before onset,
- compare onset-centered organization across seasons,
- and test whether persistence after onset differs between PM10 and PM2.5.

---

## Notes on the seasonal narrative anchor

Stage 5 uses four seasonal roles:

- **DJF** → dry benchmark
- **MAM** → true transition season
- **JJA** → wet-season contrast
- **SON** → drying-season context / reorganization

These labels are not only descriptive. They summarize a consistent combination of:

- event coverage,
- burden behavior,
- precipitation background,
- and onset-day circulation structure.

The purpose is to make the final thesis narrative physically readable rather than purely calendar-based.

---

## Notes on day-0 seasonal composites

Stage 5 replaces the month-centered view with a season-centered onset framework.

The central interpretation is:

- **PM10** keeps its clearest and most defensible benchmark in **DJF**, weakens sharply in **JJA**, and shows only partial reorganization in **SON**.
- **PM2.5** is less winter-confined, remains organized in **MAM**, weakens less strongly in **JJA**, and shows a notable **SON re-emergence**.

A useful compact formulation is:

> **PM10 shows the clearest dry-season benchmark and the strongest wet-season weakening, whereas PM2.5 retains a more seasonally extended synoptic organization, including a marked drying-season re-emergence in SON.**

---

## Notes on significance testing

The Stage 5 significance framework compares:

> **onset days vs seasonal non-onset reference days**

Key design choices:

- comparison is performed **within each season**,
- reference-day samples are balanced against event samples,
- gridpoint-wise **Welch t-tests** are used,
- and both day 0 and a selected precursor lag (**lag −1**) are examined.

Interpretive purpose:

- determine where the onset signal is distinguishable from the seasonal background,
- avoid overclaiming patterns that are visually plausible but weak against within-season variability,
- and preserve continuity with the significance logic already used in Stage 3.

Important reading rule:

A season can be highly polluted in burden terms without necessarily giving the strongest onset-vs-reference separability, and the opposite can also occur.

---

## Notes on the focused physical consistency check

The physical-consistency section in Stage 5 is intentionally narrow.

It mainly uses:

- seasonal precipitation background,
- and focused February / May / July precipitation summaries.

Interpretive purpose:

- support the dry-benchmark role of **DJF**,
- support the transition role of **MAM**,
- support the wet-background role of **JJA**,
- and keep **SON** in the story as a drying-season context rather than a full new mechanism branch.

In this final notebook, precipitation remains the main physical-support variable. Lower-tropospheric diagnostics from Stage 4 remain scientifically useful, but are no longer treated as core products.

---

## Notes on RONI and season-year assignment

Stage 5 uses a **season-year** framework when attaching ENSO phases.

This matters especially for **DJF**:

- January and February keep their calendar year,
- but **December is assigned to the following DJF season-year**.

Example:

- December 2012 belongs to **2013_DJF** rather than 2012_DJF.

This is necessary for seasonal climate classification, but it also creates one small edge-effect limitation near the end of the study period.

---

## Notes on onset frequency by ENSO phase

Stage 5 separates two related but different ideas:

1. **raw onset counts** by phase
2. **onset rates per season-year** by phase

The onset-rate metric is the more comparable one because it divides the number of onset events by the number of available season-years in each ENSO phase.

This prevents misleading interpretation when one phase has more years represented than another.

A key thesis-reading point is:

> the ENSO phase with the highest onset occurrence is not necessarily the phase with the most sharply organized synoptic pattern.

That contrast is especially important in **MAM**.

---

## Notes on seasonal synoptic stories under ENSO

Stage 5 compares ENSO-phase composites **within a fixed season**.

This means the question is not:

- how does winter differ from summer?

but rather:

- within DJF, how do El Niño, Neutral, and La Niña onset-day structures differ?

Interpretive emphasis by season:

- **DJF** → primary benchmark season
- **MAM** → primary transition season
- **JJA** → descriptive but crucial for robust ENSO contrast
- **SON** → useful context, but not the strongest phase-structure claim

A compact reading of the full ENSO story is:

- **DJF** remains physically important, but its ENSO signal is internally split across metrics.
- **MAM** is transitional and often descriptive rather than strongly robust.
- **JJA** is the most statistically defendible ENSO season.
- **SON** contributes modulation context, especially for occurrence and burden, but should not be overclaimed as the strongest synoptic reorganization case.

---

## Notes on WHO exceedance diagnostics by ENSO phase

Stage 5 evaluates three WHO exceedance metrics for both pollutants:

- **exceedance frequency**
- **mean exceedance magnitude**
- **exceedance load sum**

These are examined both:

- **seasonally**, and
- in a **pooled all-season summary**.

Interpretive caution:

The seasonal tables are more informative than the pooled ones.

A useful thesis-ready summary is:

> **ENSO modulation is expressed more clearly in exceedance frequency than in the average exceedance magnitude, and more clearly in seasonal diagnostics than in pooled all-season summaries.**

---

## Notes on robustness tests

Stage 5 uses two different chi-square frameworks.

### 1. Goodness-of-fit chi-square for onset frequency

Question asked:

> Is the observed phase distribution of onset events more uneven than expected from the availability of season-years in each phase?

This is used for **onset frequency by phase**.

### 2. Chi-square of independence for WHO exceedance frequency

Question asked:

> Does the proportion of exceedance vs non-exceedance days differ across ENSO phases?

This is used for **WHO exceed / non-exceed counts by phase**.

### 3. Cramér’s V

For the exceedance-frequency chi-square, Stage 5 also reports **Cramér’s V** as a compact effect-size measure.

Interpretive note used in the stage presentation:

- values around **0.09–0.18** are small-to-moderate,
- but still non-negligible seasonal ENSO effects.

Burden metrics such as exceedance load remain primarily **descriptive** in this stage.

---

## Notes on pollutant contrast in the ENSO story

A clean summary of the pollutant contrast is:

- **PM10** keeps a clearer winter benchmark and shows stronger Neutral preference from **MAM to SON**.
- **PM2.5** shows a more seasonally extended ENSO sensitivity, especially in **JJA** and, more cautiously, **SON**.

This means Stage 5 does not support one identical ENSO response for both pollutants.

---

## Notes on the strongest and weakest ENSO results

### Strongest and most defendible

- **JJA** is the clearest ENSO modulation season.
- Both pollutants show robust phase dependence in onset frequency and WHO exceedance frequency.
- PM2.5 also shows a particularly distinct ENSO-conditioned synoptic contrast in JJA.

### Physically important but internally split

- **DJF** remains essential to the thesis because it is the clearest dry benchmark.
- However, the ENSO effect in DJF is not identical across onset frequency, synoptic organization, and exceedance frequency.

### Most descriptive / least robust

- **MAM** remains the cleanest transition season physically, but its ENSO results are not the strongest statistically.

### Secondary but informative

- **SON** contributes to the ENSO story, especially for occurrence and burden, but should be treated more cautiously than DJF or JJA.

---

## Notes on the 31 unlabeled daily observations

A small edge-effect limitation affects the ENSO assignment.

Because **December 2024** belongs to **DJF 2025** under season-year logic, but the ENSO lookup table was truncated at **2024**, a set of **31 daily observations** remained without assigned ENSO phase.

These days were excluded from ENSO-conditioned diagnostics.

Interpretive note:

- this is a real limitation,
- but it is small,
- and it represents **less than 1% of the full daily record**.

A concise thesis-ready wording is:

> A small edge-effect limitation arose from the DJF season-year definition: December 2024 days belong to DJF 2025, but the ENSO lookup table was truncated at 2024, leaving 31 daily observations without assigned phase. These days were excluded from ENSO-conditioned diagnostics, but they represent less than 1% of the full daily record and are unlikely to alter the main seasonal conclusions.

---

## Methodological scope

Stage 5 focuses on:

- seasonal onset stories,
- lag evolution,
- significance support,
- focused physical consistency,
- and ENSO modulation.

This final notebook does **not** aim to:

- perform full source apportionment,
- prove full boundary-layer causality,
- build a complete dynamical ENSO-attribution study,
- or reopen lower-tropospheric diagnostics as a parallel major branch.

The purpose of Stage 5 is closure and synthesis, not expansion.

---

## Final role of Stage 5 in the thesis

Stage 5 is the **final analysis-stage notebook**.

Its main contribution is to show that:

- the thesis can now be told through a compact seasonal framework,
- the event story is most readable in DJF / MAM / JJA with SON as context,
- and ENSO modulates that story in a seasonally selective and metric-dependent way.

This notebook is therefore the final analytical step before full thesis writing.

---

© 2026 Erick Rico Esparza  
Tampere University / ICAyCC–UNAM
