# Stage 4 – Seasonal Synthesis, Regime Extraction, Lag Evolution, and Targeted Mechanism Check

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

This folder documents **Stage 4** of my MSc thesis. Building directly on the monthly high-versus-clean contrasts established in Stage 3, this stage reduces the 12-month picture into a smaller number of robust seasonal narratives and then tests them through:

- **seasonal synthesis of the Stage 3 monthly story**,
- **light k-means regime extraction** from episode-onset days,
- **lagged composites around event onset**, and
- a **targeted physical mechanism check** using precipitation, 850 hPa circulation, and 850 hPa specific humidity.

Unlike Stage 3, which emphasized **monthly p90 versus p10 contrasts**, Stage 4 focuses on answering a narrower physical question:

> Which seasonal windows contain the clearest and most interpretable polluted-event stories, how do those stories evolve around onset, and are they dynamically and physically consistent?

This stage therefore serves as the main bridge between the monthly diagnostic backbone of Stage 3 and the large-scale climate modulation analysis planned for Stage 5.

---

## Methodological framework

### Focus-window selection

Stage 4 starts from the Stage 3 synthesis and formally narrows the analysis to three representative windows:

- **February** → primary late-winter benchmark
- **May** → primary transition-season case
- **July** → wet-season contrast case

These months were selected because they summarize the seasonal evolution of synoptic control more clearly than the full 12-month set.

### Onset-day framework

Pollution episodes are represented using a **single day per episode**:

> **Day 0 = episode onset day**

This avoids overcounting persistent events and keeps the analysis tied to event initiation rather than duration alone.

### Regime extraction

A light **k-means clustering** framework is applied separately to PM10 and PM2.5 onset-day samples using **Z500 anomaly fields** over the Mexico-centered domain.

The goal is not to build a full climatological weather-typing system, but to identify a small set of recurrent synoptic prototypes associated with polluted onset.

### Lag analysis

Lag composites are built over:

> **−3 to +2 days relative to onset**

This allows Stage 4 to examine:

- preconditioning,
- onset structure,
- short persistence,
- and early decay.

### Mechanism check

A focused physical-consistency test is added using:

- daily precipitation,
- 850 hPa geopotential height and winds,
- 850 hPa specific humidity.

This mechanism section is intentionally limited in scope and is designed to support the core Stage 4 story rather than create a new parallel branch of analysis.

---

## Stage 4 components

Stage 4 is structured into four analytical modules.

### Part I – Seasonal synthesis from Stage 3

- Monthly significance and burden diagnostics are condensed into a seasonal narrative.
- February, May, and July are selected as the main focus windows.
- The late-winter benchmark, transition-season behavior, and wet-season contrast are formalized.

---

### Part II – Synoptic regime extraction

A light k-means workflow is applied separately for PM10 and PM2.5 using **episode-onset Z500 anomalies**.

Diagnostics include:

- candidate k testing,
- selected regime solution,
- regime composite maps,
- regime frequency by month.

This step shifts the analysis from monthly contrasts to **recurrent onset-day synoptic prototypes**.

---

### Part III – Lag composites around event onset

For February, May, and July, lag composites are generated for both pollutants.

Diagnostics include:

- 6-panel lag sequences,
- onset-centered interpretation,
- regime-conditioned lag-0 fingerprints,
- comparison of February benchmark versus broader May–July structures.

This step clarifies how the selected event stories evolve before and after onset.

---

### Part IV – Targeted physical mechanism check

The physical interpretation is refined using:

- precipitation consistency around onset,
- 850 hPa circulation composites,
- 850 hPa specific humidity composites,
- lagged mechanism diagnostics over the Valley of Mexico.

This section tests whether the synoptic stories identified in Parts I–III are consistent with:

- dry versus wet backgrounds,
- lower-tropospheric ventilation,
- and lower-tropospheric moisture structure.

---

## Contents

### Notebook

- `notebook_stage4.ipynb`  
  Full reproducible workflow including:

  - loading Stage 3 outputs and event tables
  - reanalysis loading and anomaly preparation
  - seasonal synthesis diagnostics
  - pollutant-specific onset-day k-means clustering
  - lag composites for February, May, and July
  - targeted mechanism diagnostics using precipitation, H850/U850/V850, and SH850
  - export of final summary tables for presentation and thesis use

---

### Presentation

- `thesis_stage4.pdf`

This presentation summarizes:

- the reduction from monthly diagnostics to three focus windows,
- the onset-day synoptic regimes for PM10 and PM2.5,
- the lagged evolution of benchmark, transition, and wet-season cases,
- and the mechanism-oriented interpretation used to prepare Stage 5.

---

## Data sources

### Air quality data

**RAMA – Red Automática de Monitoreo Atmosférico**  
Mexico City air-quality monitoring network.

https://www.aire.cdmx.gob.mx/

Daily and hourly station data aggregated to city-wide diagnostics.

---

### Atmospheric reanalysis

**NARR – North American Regional Reanalysis (NOAA PSL)**  
https://psl.noaa.gov/data/gridded/data.narr.html

Variables used in Stage 4:

- 500 hPa geopotential height (Z500)
- 500 hPa zonal wind (U)
- 500 hPa meridional wind (V)
- daily precipitation
- 850 hPa geopotential height (H850)
- 850 hPa zonal wind (U850)
- 850 hPa meridional wind (V850)
- 850 hPa specific humidity (SH850)

---

## Files

📂 stage4  
┣ 📜 README.md  
┣ 📜 notebook_stage4.ipynb ← Reproducible analysis code  
┣ 📜 thesis_stage4.pdf ← Stage 4 presentation  
┣ 📜 shum850_mex_2012_2024.nc ← Local SH850 domain subset used in the mechanism check  
┗ 📂 docs  
┣ 📜 references_and_notes_stage4.md  
┣ 📜 research_question_stage4.md  

---

## Outputs

Outputs generated during Stage 4 are saved locally under:

┗ 📂 outputs/  
┣ 📂 figures/  
┣ 📂 tables/

These include:

- seasonal synthesis figures
- regime composite and regime-frequency figures
- lag composite figures
- mechanism-check figures
- summary CSV tables for presentation and thesis writing

**Exception:** the locally subsetted `shum850_mex_2012_2024.nc` file is stored at the same directory level as the notebook rather than inside `outputs/`.

Outputs are not uploaded to the repository to keep the repository lightweight.

Figures and summary information can be consulted in the presentation file.

---

## Key outcomes of Stage 4

- The Stage 3 monthly story can be reduced to **three robust windows**: February, May, and July.
- February behaves as the clearest **late-winter benchmark** for both PM10 and PM2.5.
- May emerges as a true **transition case**, not simply a weaker February.
- July acts as a **wet-season contrast**, with a much stronger collapse of robust synoptic control for PM10 than for PM2.5.
- A three-regime onset-day solution provides a practical and physically interpretable summary of polluted-event synoptic prototypes.
- Lag composites show that PM2.5 retains more organized nonwinter structure than PM10.
- The mechanism check supports the seasonal interpretation by linking February to persistent dryness, May to transition-season moisture reorganization, and July PM10 onset to a rainfall-break / reduced-ventilation signature.

Stage 4 therefore turns the monthly contrast framework of Stage 3 into a smaller set of **seasonally interpretable onset stories**.

---

## Transition to Stage 5

Stage 5 will extend this framework toward:

- ENSO-phase stratification,
- comparison of focus-window behavior across El Niño / La Niña / neutral conditions,
- and evaluation of whether the February benchmark, May transition, and July PM10–PM2.5 contrast are seasonally robust only, or also systematically climate-modulated.

Stage 4 provides the **seasonal, synoptic, and mechanism-oriented synthesis** required for that next step.

---

## Reproducibility notes

To respect repository size limits:

- Raw PM and NetCDF input files are **not included**.
- Outputs under `outputs/` are **not uploaded**.
- Figures are available within the presentation.
- The SH850 local subset file is referenced in this folder structure but is not intended for public redistribution.

Screenshots, derived figures, or summarized information may be used **with proper citation of this repository and author**.

---

© 2026 Erick Rico Esparza  
Tampere University / ICAyCC–UNAM
