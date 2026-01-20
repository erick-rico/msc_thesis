# Stage 1 – Exploratory diagnostics and event definition

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

Stage 1 focuses on **exploratory diagnostics** and **methodological setup** for the MSc thesis on
extreme PM₂.₅ and PM₁₀ pollution episodes over the Valley of Mexico.

The main objectives of this stage are to:
- define a robust and transparent event-selection strategy,
- explore seasonal and monthly background conditions,
- establish reproducible workflows for synoptic-scale analysis,
- generate preliminary diagnostics to guide later stages.

This stage does **not** aim at final interpretation, but at building confidence in the data,
methods, and feasibility of the planned analyses.

---

## Contents

- **Monthly synoptic composites**  
  Monthly p90-based event selection and 500-hPa geopotential height anomaly composites
  using NARR reanalysis, including winds and significance masks.

- **Diurnal PM maxima diagnostics**  
  Hourly RAMA data used to characterize the timing and magnitude of daily PM maxima
  across months, as an exploratory indicator of accumulation and ventilation regimes.

---

## Data sources

- **Air quality data (PM₂.₅, PM₁₀):**  
  RAMA (Red Automática de Monitoreo Atmosférico), Mexico City.  
  Hourly station data aggregated to city-wide diagnostics.

- **Meteorological data:**  
  NARR reanalysis (NOAA PSL).  
  Variables: geopotential height and winds at 500 hPa.

Raw data are not included in this repository due to size and access constraints.

---

## Files

📂 stage1
┣ 📜 README.md
┣ 📜 notebook_stage1.ipynb ← Reproducible analysis code
┣ 📜 thesis_stage1.pdf ← Stage 1 presentation
┗ 📂 docs
┣ 📜 references_and_notes_stage1.md
┗ 📜 research_question_stage1.md


---

## Role within the thesis

Stage 1 corresponds to the **exploratory and setup phase** of the thesis.
Its outputs guide the design of:
- synoptic regime classification,
- event-based composites,
- intraseasonal diagnostics,
- ENSO phase separation in later stages.

---

## Files and reproducibility

To ensure privacy and size limits:
- Raw CSVs and NetCDFs are **not included** in this repository.  
- All figures are available in the Stage 1 presentation (`thesis_stage1.pdf`); screenshots may be freely used with citation.  
- Anyone interested in the datasets may contact me directly.

---

© 2026 Erick Rico Esparza
Tampere University / ICAyCC-UNAM
