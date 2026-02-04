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

This folder documents **Stage 1** of my MSc thesis, which focuses on exploratory analysis, data diagnostics, and the definition of extreme PM episodes to be used in subsequent synoptic and climate analyses.

Stage 1 is divided into three sub-stages:

- **Stage 1.1** — Initial exploratory analysis and percentile-based extremes using daily city-mean PM data.
- **Stage 1.2** — Monthly composites and seasonal structure of PM extremes.
- **Stage 1.3** — Harmonic diagnostics and comparison with official air-quality thresholds (NOM-172 and PCAA).

The goal of this stage is **not** to establish causality, but to:
- understand the structure of PM variability,
- evaluate alternative episode definitions,
- and converge toward a defensible and efficient methodology for Stage 2.

---

## Contents

### Notebooks
- `notebook_stage1_1.ipynb`  
  Initial exploratory analysis (Stage 1.1):  
  percentile-based extremes (p90/p10), daily city-mean PM data, and first monthly composites.

- `notebook_stage1_2&3.ipynb`  
  Stage 1.2 and 1.3 analyses:
  - Monthly composites of PM extremes.
  - Diurnal and semidiurnal harmonic analysis (24h + 12h).
  - Comparison between statistical extremes and official thresholds.
  - Sensitivity analyses using hourly RAMA data.

---

### Presentations / summaries
- `thesis_stage1_1.pdf`  
  Presentation summarizing Stage 1.1 results.

- `thesis_stage1_2.pdf`  
  Presentation summarizing Stage 1.2 (monthly composites and seasonal structure).

- `thesis_stage1_3.pdf`  
  Presentation summarizing Stage 1.3 (harmonics, thresholds, and contingency-based composites).

- `thesis_stage1_composites_summary.pdf`  
  Comparative summary of three event-definition branches:
  - **Branch A**: Percentile-based extremes (p90/p10) using daily city-mean PM data.
  - **Branch B**: NOM-172 “Extremely Poor” thresholds using hourly RAMA data.
  - **Branch C**: PCAA Phase I/II contingency thresholds (MA24) using hourly RAMA data.

  This document was used to support the final methodological decision.

---

## Data sources

- **Air quality data (PM₂.₅, PM₁₀):**  
  RAMA (Red Automática de Monitoreo Atmosférico), Mexico City.  
  Daily & Hourly station data aggregated to city-wide diagnostics.

- **Meteorological data:**  
  NARR reanalysis (NOAA PSL).  
  Variables: geopotential height and winds at 500 hPa.

Raw data are not included in this repository due to size and access constraints.

---

## Files

📂 stage1
┣ 📜 README.md
┣ 📜 notebook_stage1_1.ipynb ← Reproducible analysis code
┣ 📜 thesis_stage1_1.pdf ← Stage 1.1 presentation
┣ 📜 notebook_stage1_2&3.ipynb ← Reproducible analysis code
┣ 📜 thesis_stage1_2.pdf ← Stage 1.2 presentation
┣ 📜 thesis_stage1_3.pdf ← Stage 1.3 presentation
┣ 📜 thesis_stage1_composites_summary.pdf ← Stage 1 composites summary presentation
┗ 📂 docs
┣ 📜 references_and_notes_stage1.md
┗ 📜 research_question_stage1.md

---

## Key outcomes of Stage 1

- Percentile-based definitions (p90) provide **robust sample sizes** suitable for synoptic and ENSO-modulated analyses.
- Official thresholds (NOM-172, PCAA) capture **rare tail events**, useful for policy comparison but insufficient as the main episode definition.
- City-mean daily PM metrics are **better aligned with synoptic-scale circulation patterns** than station-based hourly maxima.

**Decision:**  
Stage 2 will proceed using **daily city-mean PM data (2012–2024)** with **percentile-based episode definitions (p90)**, while hourly RAMA-based analyses are retained as sensitivity and policy-oriented benchmarks.

---

## Next stage

Stage 2 will focus on:
- Seasonal and monthly stratification of extreme PM episodes.
- Refined monthly composites for episode-active periods.
- Preparation for synoptic regime classification and lagged composites

---

## Files and reproducibility

To ensure privacy and size limits:
- Raw CSVs and NetCDFs are **not included** in this repository.  
- All figures are available in the Stage 1 presentations; screenshots may be freely used with citation.  

---

© 2026 Erick Rico Esparza
Tampere University / ICAyCC-UNAM
