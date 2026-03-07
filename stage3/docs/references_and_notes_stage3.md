# References and notes – Stage 3

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

---

### Precipitation data

NARR daily precipitation rate dataset

https://downloads.psl.noaa.gov/Datasets/NARR/Dailies/monolevel/

Variable:

- prate (kg m⁻² s⁻¹)

Converted to **mm/day** for climatological diagnostics.

---

## Literature used for Stage 3 interpretation

1. Díaz-Esteban, Y., Barrett, B. S., & Raga, G. B. (2022).  
   *Circulation patterns influencing the concentration of pollutants in central Mexico.*  
   Atmospheric Environment, 274, 118976.  
   https://doi.org/10.1016/J.ATMOSENV.2022.118976  

2. Magaña, V., Amador, J. A., & Medina, S. (1999).  
   *The Midsummer Drought over Mexico and Central America.*  
   Journal of Climate, 12(6), 1577–1588.  
   https://journals.ametsoc.org/view/journals/clim/12/6/1520-0442_1999_012_1577_tmdoma_2.0.co_2.xml  

3. Maurer, E. P., Stewart, I. T., Joseph, K., & Hidalgo, H. G. (2022).  
   *The Mesoamerican mid-summer drought: The impact of its definition on occurrences and recent changes.*  
   Hydrology and Earth System Sciences, 26(5), 1425–1437.  
   https://doi.org/10.5194/hess-26-1425-2022  

4. Yoo, J. M., et al. (2014).  
   *New indices for wet scavenging of air pollutants by summertime rain.*  
   Atmospheric Environment, 82, 226–237.  
   https://doi.org/10.1016/j.atmosenv.2013.10.022  

---

## Notes on precipitation diagnostics

Stage 3 introduces precipitation climatology in order to provide hydroclimatic context for PM variability.

Key motivations:

- rainfall contributes to **wet scavenging of particulate matter**
- convective activity increases **boundary-layer mixing**
- the wet season therefore weakens persistence of high-PM regimes

Monthly precipitation climatology is derived from NARR daily prate and summarized both spatially and over the Valley of Mexico.

---

## Notes on anomaly framework

All anomaly fields are defined relative to the **calendar-month climatology** (2012–2024).

This ensures consistency between:

- monthly p90/p10 thresholds,
- anomaly baselines,
- and composite interpretation.

Zero anomaly therefore represents the **typical atmospheric state of that month**.

---

## Notes on p90 vs p10 composites

Stage 3 compares two extreme groups:

- **p90 days:** high-PM conditions
- **p10 days:** low-PM conditions

Balanced composites are constructed using: N_used = min(N_high, N_low)


This prevents statistical bias caused by unequal sample sizes.

---

## Notes on circulation contrasts

The primary diagnostic of Stage 3 is: ΔZ500′ = Z500′(p90) − Z500′(p10)


Interpretation:

- **positive ΔZ500′**
  → high-PM days exhibit stronger ridging relative to clean days

- **negative ΔZ500′**
  → high-PM days occur under relatively more trough-like conditions

Statistical significance is evaluated using a **Welch two-sample t-test**.

---

## Notes on significance interpretation

Gridpoint significance is evaluated using:

- Welch t-test
- p < 0.05 threshold

To avoid overinterpreting isolated points, the analysis also reports:

- **fraction of significant area per month**

This metric provides a domain-scale measure of robustness.

---

## Methodological scope

Stage 3 focuses on:

- precipitation context
- balanced high vs low composites
- synoptic circulation contrasts
- significance robustness

This stage does not yet include:

- lagged composites
- moisture transport diagnostics
- ENSO phase stratification
- objective regime classification

These analyses are reserved for later stages.

---

© 2026 Erick Rico Esparza  
Tampere University / ICAyCC–UNAM