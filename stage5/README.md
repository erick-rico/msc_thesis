# Stage 5 – Seasonal Onset Stories, Statistical Support, Physical Consistency, and ENSO Modulation

**Degree:** MSc in Environmental Engineering  
**University:** Tampere University  
**Student:** Erick Rico Esparza  

**Supervisors:**  
- Prof. Jung-Eun Chu (external)  
- Prof. Miikka Dal Maso (internal)  

**Additional guidance (Mexico):**  
- Dr. Jorge Zavala Hidalgo (ICAyCC–UNAM)  
- Mtra. Katia Trujillo (ICAyCC–UNAM)  

**Semester:** Spring 2026  

---

## Overview

This folder documents **Stage 5**, the final analysis notebook of my MSc thesis. Building directly on the monthly contrasts of Stage 3 and the seasonal synthesis of Stage 4, this stage reorganizes the thesis around:

- **seasonal onset-based synoptic composites**,
- **lag evolution around episode onset**,
- **statistical support against seasonal background conditions**,
- **focused physical consistency checks**, and
- **ENSO modulation of onset frequency, synoptic structure, and WHO exceedance behavior**.

Unlike Stage 4, which asked whether a small number of seasonal stories could summarize the polluted-event problem, Stage 5 asks the final thesis-stage question:

> Which seasonal onset-based circulation patterns are associated with extreme PM10 and PM2.5 events over the Valley of Mexico, and how are those seasonal stories modulated by ENSO?

This stage is therefore the **final bridge from seasonal synoptic interpretation to climate-scale modulation**.

---

## Methodological framework

### Seasonal onset framework

Stage 5 retains the **monthly p90 event definition** established in earlier stages and then regroups those monthly-defined episode onsets into:

- **DJF**
- **MAM**
- **JJA**
- **SON**

This means the analysis remains consistent with the earlier monthly-relative extreme framework while making the final interpretation season-centered.

### Event-centered sampling

Pollution episodes are represented using a **single day per episode**:

> **Day 0 = episode onset day**

This keeps the analysis tied to event initiation rather than duration alone and prevents long persistent episodes from dominating the sample.

### Seasonal composite design

Seasonal onset-day composites are built separately for PM10 and PM2.5 using:

- **Z500 anomalies**
- **U500 and V500 anomalies**
- seasonal grouping of onset days

The purpose is to test whether the Stage 4 benchmark, transition, wet-season contrast, and drying-season context remain visible when the analysis is fully reorganized by season.

### Lag evolution

Lag composites are built over:

> **−3 to +2 days relative to onset**

This allows the notebook to examine:

- preconditioning,
- onset organization,
- short persistence,
- and early decay.

### Statistical support

Stage 5 formally compares **onset days** against **seasonal non-onset reference days** using:

- **gridpoint-wise Welch t-tests**,
- balanced event/reference samples,
- day-0 significance maps,
- and a selected precursor test at **lag −1**.

This step asks whether the seasonal onset signals are distinguishable from their own seasonal background rather than only visually apparent.

### Focused physical consistency

A narrow physical-consistency check is retained using:

- seasonal precipitation background,
- focused February–May–July precipitation support,
- and compact interpretation notes tying seasonal circulation stories to hydroclimatic context.

In this final stage, precipitation remains central, while 850 hPa and SH850 diagnostics are treated as **supporting context inherited from Stage 4 rather than new core branches**.

### ENSO classification

ENSO phases are classified using the **CPC Relative Oceanic Niño Index (RONI)** seasonal framework.

Phase classes used in this stage:

- **El Niño**
- **Neutral**
- **La Niña**

RONI-based season-year lookup tables are then attached to:

- episode onsets,
- seasonal synoptic composites by phase,
- and daily WHO exceedance diagnostics.

---

## Stage 5 components

Stage 5 is organized into five analytical modules.

### Part I – Seasonal descriptive framework before onset analysis

This first module defines the seasonal background in which polluted onsets occur.

Diagnostics include:

- seasonal onset counts,
- seasonal WHO burden context,
- seasonal precipitation context,
- and a compact seasonal anchor table.

This step establishes the seasonal narrative used throughout the notebook:

- **DJF** → dry benchmark  
- **MAM** → transition season  
- **JJA** → wet-season contrast  
- **SON** → drying-season context / reorganization

---

### Part II – Seasonal onset-day composites and lag evolution

This module builds:

- seasonal day-0 composites at 500 hPa,
- seasonal lag composites from −3 to +2,
- and compact lag-comparison diagnostics.

This is the section where the seasonal event stories themselves are identified and compared across pollutants.

---

### Part III – Statistical support and focused physical consistency

This module tests whether the seasonal onset patterns are distinguishable from the seasonal background and physically coherent.

Diagnostics include:

- day-0 significance maps,
- lag −1 significance maps,
- fraction of significant area tables,
- seasonal precipitation support,
- and focused February–May–July precipitation summaries.

---

### Part IV – ENSO modulation

This module evaluates whether the seasonal event stories vary across climate phases.

Diagnostics include:

- ENSO phase lookup tables using CPC RONI,
- onset counts and onset rates by phase,
- seasonal onset-day composites by ENSO phase,
- seasonal WHO exceedance diagnostics by ENSO phase,
- and simple robustness tests for phase dependence.

This section treats ENSO as a **seasonal modulator rather than a universal driver**.

---

### Part V – Final synthesis and export-ready outputs

The final module compiles:

- thesis-ready summary tables,
- figure-bank notes for core vs appendix use,
- compact final interpretation bullets,
- and notebook closing notes.

This module marks the end of the staged analysis workflow and prepares the transition into thesis writing.

---

## Contents

### Notebook

- `notebook_stage5.ipynb`  
  Full reproducible workflow including:

  - loading prior-stage event and composite diagnostics
  - loading 500 hPa reanalysis and precipitation support fields
  - building seasonal onset-day and lag composites
  - computing significance support against seasonal non-onset reference days
  - attaching CPC RONI phase labels to season-years and daily records
  - comparing onset frequency, synoptic structure, and WHO exceedance behavior across ENSO phases
  - exporting summary tables for slides and thesis writing

---

### Presentation

- `thesis_stage5.pdf`

This presentation summarizes:

- the final seasonal reorganization of the thesis narrative,
- seasonal onset-day synoptic stories for PM10 and PM2.5,
- lag evolution and significance support,
- focused precipitation consistency,
- ENSO modulation of onset frequency and synoptic structure,
- and the final conclusions and limitations carried into thesis writing.

---

## Data sources

### Air quality data

**RAMA – Red Automática de Monitoreo Atmosférico**  
Mexico City air-quality monitoring network.

https://www.aire.cdmx.gob.mx/

Daily station data aggregated to city-wide PM diagnostics.

---

### Atmospheric reanalysis

**NARR – North American Regional Reanalysis (NOAA PSL)**  
https://psl.noaa.gov/data/gridded/data.narr.html

Variables used in Stage 5 core analysis:

- 500 hPa geopotential height (Z500)
- 500 hPa zonal wind (U500)
- 500 hPa meridional wind (V500)
- daily precipitation

Supporting lower-tropospheric diagnostics used earlier in the thesis remain part of the broader interpretive context but are not expanded as core Stage 5 products.

---

### ENSO classification

**CPC Relative Oceanic Niño Index (RONI) – NOAA Climate Prediction Center**  
https://www.cpc.ncep.noaa.gov/products/analysis_monitoring/enso/roni/

RONI is used here as the operational seasonal ENSO classification framework for assigning:

- El Niño
- Neutral
- La Niña

phase labels to season-years across the 2012–2024 study period.

---

## Files

📂 stage5  
┣ 📜 README.md  
┣ 📜 notebook_stage5.ipynb ← Reproducible analysis code  
┣ 📜 thesis_stage5.pdf ← Stage 5 presentation  
┗ 📂 docs  
&nbsp;&nbsp;&nbsp;&nbsp;┣ 📜 references_and_notes_stage5.md  
&nbsp;&nbsp;&nbsp;&nbsp;┗ 📜 research_question_stage5.md  

---

## Outputs

Outputs generated during Stage 5 are saved locally under:

┗ 📂 outputs/  
&nbsp;&nbsp;&nbsp;&nbsp;┣ 📂 figures/  
&nbsp;&nbsp;&nbsp;&nbsp;┗ 📂 tables/  

These include:

- seasonal onset-day composite figures
- seasonal lag composite figures
- significance-support figures
- precipitation-support summary tables
- ENSO onset-frequency figures
- ENSO synoptic composite figures
- WHO exceedance tables by phase
- robustness-test tables
- final synthesis tables for slides and thesis writing

Outputs are **not uploaded** to the repository in order to keep the repository lightweight.

Figures and summary information can be consulted in the presentation file.

---

## Key outcomes of Stage 5

- The final thesis story can be expressed clearly through a **seasonal onset-based framework** rather than a month-by-month diagnostic sequence.
- **DJF** remains the clearest **dry benchmark** for both pollutants.
- **MAM** emerges as the strongest **transition season**: organized and interpretable, but not a simple winter extension.
- **JJA** provides the clearest **wet-season contrast**, especially through the stronger weakening of PM10 and the strongest ENSO modulation signal.
- **PM2.5** keeps a more seasonally extended synoptic organization than PM10, including a notable **SON re-emergence**.
- Seasonal significance support shows that the clearest and most defendible signals are not always identical to the seasons with the highest burden.
- ENSO acts as a **seasonal modulator**, not as a single dominant driver with one uniform sign throughout the year.
- The most statistically defendible ENSO result in this stage is the **JJA modulation signal**, while **MAM** remains more descriptive and transitional.

Stage 5 therefore closes the staged analysis framework by linking:

- seasonal onset structure,
- lag evolution,
- seasonal background support,
- and climate-phase modulation.

---

## After Stage 5

Stage 5 is the **last analysis-stage notebook** of the thesis.

The next step is not a new analytical stage, but the transition into:

- thesis Results writing,
- integrated Discussion writing across Stages 3–5,
- and later preparation of the full thesis-wide final presentation.

In practical terms, the main task after this notebook is to move from stage-wise interpretation to the full written thesis narrative.

---

## Reproducibility notes

To respect repository size limits:

- Raw PM and NetCDF input files are **not included**.
- Exported outputs under `outputs/` are **not uploaded**.
- Figures are available within the presentation.
- This repository documents the analysis logic, workflow, and stage-level interpretation.

Screenshots, derived figures, or summarized information may be used **with proper citation of this repository and author**.

---

© 2026 Erick Rico Esparza  
Tampere University / ICAyCC–UNAM
