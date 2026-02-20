# References and notes – Stage 2

## Data sources

- RAMA (Red Automática de Monitoreo Atmosférico), Mexico City  
  https://www.aire.cdmx.gob.mx/

- NARR Reanalysis – NOAA Physical Sciences Laboratory  
  https://psl.noaa.gov/data/gridded/data.narr.html

---

## Notes on event definition (monthly p90)

- Extreme events are defined using the **90th percentile of each calendar month (2012–2024)**.
- Percentiles are computed from **daily city-mean PM10 and PM2.5**.
- The seasonal cycle is preserved; thresholds vary by month.
- This approach:
  - ensures balanced seasonal sampling,
  - provides adequate sample size for composites,
  - avoids artificially mixing wet- and dry-season dynamics.

Stage 2 intentionally shifts from exploratory threshold testing (Stage 1) to a **fixed and consistent event definition**.

---

## Notes on climatology and anomalies

- Z500 anomalies (Z500′) are computed relative to the **monthly climatology**.
- Monthly baselines are used instead of day-of-year climatology to:
  - maintain alignment with the monthly p90 event definition,
  - reduce overfitting to intra-seasonal variability,
  - preserve interpretability of seasonal contrasts.

- Composites represent **mean large-scale circulation during event days**, not individual extreme cases.

---

## Notes on statistical significance

- A two-sample **Welch t-test** is applied at each grid point:
  - Event days vs. non-event days (within the same calendar month).
- Stippling indicates grid points where **p < 0.05**.
- Testing within-month prevents seasonal leakage in significance assessment.
- Statistical significance highlights robust circulation differences, not necessarily dynamical causality.

---

## Notes on focused composites (Top months)

- Months are ranked transparently using:
  - event-day frequency,
  - mean exceedance above threshold (severity).
- Focused composites improve signal clarity compared to 12-panel monthly layouts.
- Ranking does not redefine events; it only prioritizes interpretation.

---

## Notes on seasonal aggregation

- Seasonal composites (DJF, MAM, JJA, SON) use the same monthly p90 event flags.
- No seasonal re-thresholding is applied.
- Seasonal synthesis is intended to:
  - reinforce dry vs. wet season contrasts,
  - identify dominant synoptic regimes,
  - prepare for Stage 3 classification.

---

## Methodological position (Stage 2 outcome)

Stage 2 establishes a physically consistent baseline linking:

- percentile-based extreme PM events,
- large-scale Z500 anomaly patterns,
- and seasonal circulation structure.

This stage does not yet include:
- moisture transport diagnostics,
- precipitation composites,
- boundary-layer stability metrics,
- or lagged circulation analysis.

These components are reserved for subsequent stages to avoid methodological inflation within Stage 2.

---

© 2026 Erick Rico Esparza  
Tampere University / ICAyCC–UNAM