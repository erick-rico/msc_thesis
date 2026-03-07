# Stage 3 – Monthly Baseline, Precipitation Context, and Extreme Circulation Contrasts

**Degree:** MSc in Environmental Engineering  
**University:** Tampere University  
**Student:** Erick Rico Esparza  

**Supervisors:**  
- Prof. Jung-Eun Chu    (external)
- Prof. Miikka Dal Maso (internal)

**Additional guidance (Mexico):**  
- Dr. Jorge Zavala Hidalgo (ICAyCC–UNAM)  
- Mtra. Katia Trujillo (ICAyCC–UNAM)  

**Semester:** Spring 2026  

---

## Overview

This folder documents **Stage 3** of my MSc thesis, which bridges the baseline climatological framework established in Stage 2 with a systematic comparison of **extreme high- and low-PM circulation patterns**.

Stage 3 introduces additional diagnostics and methodological refinements to:

- establish a clear **monthly atmospheric baseline** (Z500 climatology),
- incorporate **precipitation climatology** as hydroclimatic context,
- evaluate **WHO exceedance behavior** (frequency, magnitude, and load),
- compute balanced **p90 vs p10 synoptic composites**, and
- quantify circulation contrasts through **p90 − p10 anomaly maps with statistical significance**.

Unlike Stage 2, which focused on identifying circulation structures associated with extreme PM days, Stage 3 focuses on **contrasting high- and low-PM regimes** in order to isolate the circulation features that distinguish polluted from clean conditions.

---

## Methodological framework

### Extreme-day definition

Extreme conditions are defined within each calendar month:

> **High-PM days:** PM ≥ monthly p90  
> **Low-PM days:** PM ≤ monthly p10  

Using month-specific thresholds preserves the seasonal cycle and avoids mixing different atmospheric regimes.

### Balanced composite construction

To ensure a fair comparison between extreme groups:

> **N_used = min(N_high, N_low)**

The same number of days is used for p90 and p10 composites within each month.

This prevents biased statistical comparisons caused by unequal sample sizes.

---

## Stage 3 components

Stage 3 is structured into four analytical modules.

### Part I – Seasonal context diagnostics

- Monthly precipitation climatology (NARR prate → mm/day)
- Valley of Mexico precipitation seasonal cycle
- Interpretation of wet-season ventilation and scavenging effects

---

### Part II – Baseline atmospheric structure

- Monthly Z500 climatology (2012–2024)
- Mean 500 hPa wind vectors
- Definition of the anomaly reference state used for Z500′

This step clarifies the meaning of **zero anomaly** in subsequent composite maps.

---

### Part III – Extreme circulation contrasts

Balanced composites are generated for:

- **p90 (high-PM days)**
- **p10 (low-PM days)**
- **ΔZ500′ = p90 − p10**

Diagnostics include:

- Z500′ shading
- wind anomaly vectors (U′, V′)
- Welch t-test significance testing

Stippling marks grid points where **p < 0.05**.

The p90−p10 maps represent the **primary diagnostic** for Stage 3.

---

### Part IV – Air-quality exceedance diagnostics

WHO exceedances are evaluated using three complementary metrics:

1. **Frequency**  
   Percentage of days exceeding WHO thresholds.

2. **Magnitude**  
   Mean exceedance above the threshold.

3. **Load**  
   Integrated exceedance burden (frequency × magnitude).

These diagnostics provide a cross-month measure of **air-quality severity**, independent of percentile definitions.

---

## Contents

### Notebook

- `notebook_stage3.ipynb`  
  Full reproducible workflow including:

  - precipitation climatology diagnostics
  - Z500 baseline computation
  - WHO exceedance statistics
  - balanced p90/p10 composite construction
  - statistical significance testing
  - monthly synthesis tables and diagnostics

---

### Presentation

- `thesis_stage3.pdf`

This presentation summarizes:

- methodological refinements introduced in Stage 3,
- precipitation and circulation baselines,
- extreme-event circulation contrasts,
- and the monthly synthesis of synoptic drivers of extreme PM.

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

Variables used:

- 500 hPa geopotential height (Z500)
- 500 hPa zonal wind (U)
- 500 hPa meridional wind (V)

---

### Precipitation

NARR daily precipitation rate (prate)

https://downloads.psl.noaa.gov/Datasets/NARR/Dailies/monolevel/

Converted from kg m⁻² s⁻¹ to **mm/day** for climatological analysis.

---

## Files

📂 stage3  
┣ 📜 README.md  
┣ 📜 notebook_stage3.ipynb ← Reproducible analysis code  
┣ 📜 thesis_stage3.pdf ← Stage 3 presentation  
┗ 📂 docs  
┣ 📜 references_and_notes_stage3.md  
┗ 📜 research_question_stage3.md  

---

## Outputs

Outputs generated during Stage 3 are saved locally under:

┗ 📂 outputs/
┣ 📜 figures/
┣ 📜 tables/
┗ 📜 data/


These include:

- composite maps
- precipitation diagnostics
- exceedance statistics
- synthesis tables

Outputs are not uploaded to the repository to keep the repository lightweight.

Figures can be consulted in the presentation file.

---

## Key outcomes of Stage 3

- Dry-season months show a **clear stagnation–ventilation contrast** between high and low PM days.
- February exhibits the **strongest synoptic separation** between polluted and clean regimes.
- Core wet-season months (especially July) show **weak or absent Z500 separation for PM10**, consistent with wet scavenging and convective mixing.
- PM₂.₅ retains moderate synoptic sensitivity across more months than PM₁₀.
- Precipitation seasonality provides a physical explanation for the collapse of synoptic control during the wet season.

Stage 3 therefore refines the physical interpretation of Stage 2 by explicitly contrasting **high vs low pollution regimes**.

---

## Transition to Stage 4

Stage 4 will extend this framework toward:

- identification of dominant synoptic circulation patterns,
- consolidation of seasonal circulation regimes,
- evaluation of intraseasonal variability,
- and connections with larger-scale climate drivers.

Stage 3 provides the **monthly diagnostic backbone** required for these analyses.

---

## Reproducibility notes

To respect repository size limits:

- Raw data files (CSV and NetCDF) are **not included**.
- Figures are available within the presentation.

Screenshots or derived figures may be used **with proper citation of this repository and author**.

---

© 2026 Erick Rico Esparza  
Tampere University / ICAyCC–UNAM