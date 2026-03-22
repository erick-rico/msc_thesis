# References and notes – Stage 4

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

Variables used:

- 500 hPa geopotential height (Z500)
- 500 hPa zonal wind (U)
- 500 hPa meridional wind (V)
- daily precipitation
- 850 hPa geopotential height (H850)
- 850 hPa zonal wind (U850)
- 850 hPa meridional wind (V850)
- 850 hPa specific humidity (SH850)

---

## Literature used for Stage 4 interpretation

### Nucleus: synoptic regimes / clustering / recurrent prototypes

1. Díaz-Esteban, Y., Barrett, B. S., & Raga, G. B. (2022). *Circulation patterns influencing the concentration of pollutants in central Mexico.* Atmospheric Environment, 274, 118976. https://doi.org/10.1016/J.ATMOSENV.2022.118976

2. Jeong, Y. C., Yeh, S. W., Jeong, J. I., Park, R. J., Yoo, C., & Yoon, J. H. (2023). *Intrinsic atmospheric circulation patterns associated with high PM2.5 concentration days in South Korea during the cold season.* Science of The Total Environment, 863, 160878. https://doi.org/10.1016/j.scitotenv.2022.160878

3. Lee, D., Kim, H. C., Jeong, J. H., Kim, B. M., Lee, D. G., Choi, J. Y., Song, M. Y., & Yoon, J. H. (2022). *Relationship Between Synoptic Weather Pattern and Surface Particulate Matter (PM) Concentration During Winter and Spring Seasons Over South Korea.* Journal of Geophysical Research: Atmospheres, 127(24), e2022JD037517. https://doi.org/10.1029/2022JD037517

---

### Basin ventilation / local-circulation support

4. Salcido, A., Carreón-Sierra, S., & Celada-Murillo, A. T. (2019). *Air Pollution Flow Patterns in the Mexico City Region.* Climate 2019, Vol. 7, Page 128, 7(11), 128. https://doi.org/10.3390/CLI7110128

5. Jauregui Ostos, E., & Luyando, E. (1992). *Patrones de flujo de aire superficial y su relación con el transporte de contaminantes en el valle de México.* Investigaciones Geográficas, 24, 51–78. https://doi.org/10.14350/RIG.59008

6. Burgos-Cuevas, A., Adams, D. K., García-Franco, J. L., & Ruiz-Angulo, A. (2021). *A Seasonal Climatology of the Mexico City Atmospheric Boundary Layer.* Boundary-Layer Meteorology 2021 180:1, 180(1), 131–154. https://doi.org/10.1007/S10546-021-00615-3

---

### Source and interpretation caveats

7. Querol, X., Pey, J., Minguillón, M. C., Pérez, N., Alastuey, A., Viana, M., Moreno, T., Bernabé, R. M., Blanco, S., Cárdenas, B., Vega, E., Sosa, G., Escalona, S., Ruiz, H., & Artíñano, B. (2008). *PM speciation and sources in Mexico during the MILAGRO-2006 campaign.* Atmospheric Chemistry and Physics, 8(1), 111–128. https://doi.org/10.5194/acp-8-111-2008

8. Mugica, V., Ortiz, E., Molina, L., De Vizcaya-Ruiz, A., Nebot, A., Quintana, R., Aguilar, J., & Alcántara, E. (2009). *PM composition and source reconciliation in Mexico City.* Atmospheric Environment, 43(32), 5068–5074. https://doi.org/10.1016/j.atmosenv.2009.06.051

9. Raga, G. B., Ladino, L. A., Baumgardner, D., Ramirez-Romero, C., Córdoba, F., Alvarez-Ospina, H., Rosas, D., Amador, T., Miranda, J., Rosas, I., Jaramillo, A., Yakobi-Hancock, J., Kim, J. S., Martínez, L., Salinas, E., & Figueroa, B. (2021). *ADABBOY: African Dust And Biomass Burning Over Yucatan.* Bulletin of the American Meteorological Society, 102(8), E1543–E1556. https://doi.org/10.1175/BAMS-D-20-0172.1

---

## Notes on Stage 4 seasonal synthesis

Stage 4 begins by reducing the full monthly diagnostic set from Stage 3 into a smaller number of robust seasonal stories.

Selected focus windows:

- **February** → late-winter benchmark
- **May** → transition-season case
- **July** → wet-season contrast

These months were chosen not because they maximize the same metric, but because together they summarize:

- strong late-winter synoptic control,
- transitional seasonal reorganization,
- and wet-season weakening or pollutant divergence.

---

## Notes on onset-day definition

To avoid overcounting persistent episodes, clustering and lag diagnostics use:

> **one representative day per episode**

Specifically:

> **day 0 = episode onset day**

This makes the regime extraction step event-centered rather than duration-weighted.

---

## Notes on k-means regime extraction

Stage 4 applies a **light k-means classification** separately to PM10 and PM2.5 onset-day samples.

Key design choices:

- input field: **Z500 anomaly**
- one onset day per episode
- focused months only: **February, May, July**
- small candidate k range

Purpose:

- identify a few recurrent polluted-onset synoptic prototypes,
- not construct a full climatological weather-type atlas.

The preferred solution was selected using a combination of:

- visual separation,
- physical interpretability,
- and acceptable sample size per regime.

---

## Notes on lag composites

Lag composites are built over:

> **−3 to +2 days relative to onset**

Interpretive purpose:

- test whether onset is preceded by clear preconditioning,
- evaluate whether the benchmark structure persists beyond day 0,
- compare dry-season and wet-season evolution.

The key contrast in Stage 4 is not only February versus July, but also:

- **PM10 weakening in July**
- versus
- **PM2.5 retained structure in July**

---

## Notes on the physical mechanism check

The Stage 4 mechanism check is intentionally narrow in scope.

It evaluates whether the selected onset stories are physically consistent with:

- **reduced precipitation / dry-day persistence**
- **lower-tropospheric flow anomalies linked to ventilation or stagnation**
- **850 hPa moisture anomalies**

It is **not** intended as a full moisture-transport or boundary-layer process study.

---

## Notes on precipitation diagnostics

Stage 4 uses precipitation in two complementary ways:

1. **selected-window onset composites**  
   to compare February, May, and July backgrounds

2. **lagged Valley of Mexico precipitation curves**  
   to test whether onset coincides with suppressed rainfall or rainfall breaks

Interpretive caution:

- area-mean precipitation can hide convective spatial heterogeneity
- therefore precipitation is treated as a **consistency diagnostic**, not as a direct causal proof

---

## Notes on 850 hPa circulation diagnostics

The 850 hPa level was used to complement Z500 by examining the lower-tropospheric environment more directly.

This helps interpret whether polluted onset is associated with:

- reduced ventilation,
- altered transport direction,
- weak-flow conditions,
- or seasonal reorganization of low-level circulation.

The comparison between 500 hPa and 850 hPa is one of the main physical refinements introduced in Stage 4.

---

## Notes on SH850 diagnostics

Specific humidity at 850 hPa was used as a compact lower-tropospheric moisture indicator.

Interpretive purpose:

- determine whether polluted onset systematically coincides with anomalously dry lower-tropospheric conditions,
- and assess whether May and July reflect distinct moisture structures.

Important interpretation note:

Stage 4 results suggest that there is **not one universal dry-signature pattern** across all selected windows.

Instead:

- February is dry mainly as a background state,
- May shows the clearest transition-season moisture reorganization,
- July remains wet but still allows pollutant-specific differences.

---

## Methodological scope

Stage 4 focuses on:

- seasonal synthesis,
- light onset-day regime extraction,
- lagged event evolution,
- and a limited mechanism-oriented consistency check.

This stage does not yet include:

- ENSO stratification,
- climate-phase comparison of regime frequency,
- or broader teleconnection attribution.

Those analyses are reserved for Stage 5.

---

© 2026 Erick Rico Esparza  
Tampere University / ICAyCC–UNAM
