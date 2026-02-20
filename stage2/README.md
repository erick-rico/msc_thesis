# Stage 2 – Monthly Structuring and Baseline Synoptic Composites

**Degree:** MSc in Environmental Engineering  
**University:** Tampere University  
**Student:** Erick Rico Esparza  

**Supervisors:**  
- Prof. Jung-Eun Chu  
- Prof. Miikka Dal Maso  

**External guidance (Mexico):**  
- Dr. Jorge Zavala Hidalgo (ICAyCC–UNAM)  
- Mtra. Katia Trujillo (ICAyCC–UNAM)  

**Semester:** Spring 2026  

---

## Overview

This folder documents **Stage 2** of my MSc thesis, which establishes a climatological and synoptic baseline of extreme PM events in the Valley of Mexico (2012–2024).

Stage 2 consolidates the methodological decisions from Stage 1 and applies a fixed, percentile-based event definition to:

- characterize event climatology (frequency, severity, persistence),
- recompute and refine monthly Z500 anomaly composites,
- assess seasonal structuring of event-related circulation patterns,
- prepare a clean physical baseline for Stage 3 (objective synoptic regime classification).

Unlike Stage 1, this stage focuses on **physical interpretation**, not exploratory testing.

---

## Methodological framework

### Event definition

A day is classified as an extreme event if:

> PM ≥ 90th percentile of its calendar month (monthly p90)

- Based on daily city-mean PM10 and PM2.5.
- Period: 2012–2024.
- Seasonal cycle is preserved.
- Thresholds are computed independently for each calendar month.

This definition ensures:
- balanced seasonal sampling,
- sufficient sample size for composites,
- comparability across pollutants.

---

## Stage 2 components

Stage 2 is structured into four analytical modules:

### Part I – Event climatology
- Annual frequency trends  
- Year × month clustering  
- Mean exceedance above threshold  
- Episode persistence (run-length statistics)

### Part II – Monthly synoptic composites
- Z500 anomaly (Z500′) composites during p90 event days  
- 500 hPa wind vectors  
- Statistical significance (Welch t-test vs non-event days)  
- 12-panel monthly diagnostics for PM10 and PM2.5

### Part III – Focused composites (Top months)
- Transparent ranking by:
  - event-day frequency  
  - mean exceedance (severity)  
- High-signal composite maps for improved interpretability

### Part IV – Seasonal synthesis
- DJF / MAM / JJA / SON aggregation  
- Seasonal summary statistics  
- Seasonal Z500′ composites  

---

## Contents

### Notebook
- `notebook_stage2.ipynb`  
  Full reproducible workflow for:
  - event flagging,
  - climatology diagnostics,
  - monthly and seasonal composite construction,
  - statistical significance testing,
  - focused ranking analysis.

---

### Presentation
- `thesis_stage2.pdf`  
  Presentation summarizing:
  - methodological framework,
  - climatological results,
  - synoptic composite interpretation,
  - transition toward Stage 3.

---

## Data sources

- **Air quality data (PM₂.₅, PM₁₀):**  
  RAMA (Red Automática de Monitoreo Atmosférico), Mexico City.  
  Daily & Hourly station data aggregated to city-wide diagnostics.

**Meteorological reanalysis:**  
NARR (NOAA PSL).  
Variables:
- 500 hPa geopotential height (Z500)  
- 500 hPa zonal and meridional winds (U, V)

Raw data are not included due to size and access constraints.

---

## Files

📂 stage2
┣ 📜 README.md
┣ 📜 notebook_stage2.ipynb ← Reproducible analysis code
┣ 📜 thesis_stage2.pdf ← Stage 2 presentation
┗ 📂 docs
┣ 📜 references_and_notes_stage2.md
┗ 📜 research_question_stage2.md

Outputs (CSV files, NetCDF subsets, figures) are not uploaded in this stage.

---

## Key outcomes of Stage 2

- Extreme PM events during the **dry season (Nov–May)** are strongly associated with positive Z500 anomalies (ridge structures).
- Winter (DJF) exhibits the most robust and statistically significant synoptic signal.
- Summer (JJA) shows weak or absent large-scale coherence, suggesting different drivers (e.g., monsoon ventilation).
- Approximately 10% of episodes persist ≥3 days, indicating sustained synoptic forcing.
- PM10 and PM2.5 respond to similar large-scale circulation patterns, with spring PM10 showing additional sensitivity to surface emissions (dust/fire season influence).

This stage establishes a physically consistent baseline linking extreme PM episodes to upper-level circulation patterns.

---

## Transition to Stage 3

Stage 3 will move beyond anomaly composites toward:

- objective synoptic regime classification,
- identification of dominant large-scale circulation modes,
- association of p90 event-days with specific regimes,
- regime frequency and persistence diagnostics.

Stage 2 provides the structured foundation necessary for this transition.

---

## Reproducibility notes

To ensure privacy and size limits:
- Raw CSVs and NetCDFs are **not included** in this repository.  
- All figures are available in the Stage 2 presentations; screenshots may be freely used **with** citation.  

---

© 2026 Erick Rico Esparza
Tampere University / ICAyCC-UNAM