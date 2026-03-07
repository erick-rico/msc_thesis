# Conceptual workflow – MSc Thesis

**Student:** Erick Rico Esparza  
**Degree:** MSc in Environmental Engineering  
**University:** Tampere University  
**Thesis project:** Synoptic circulation patterns associated with particulate matter pollution episodes over Central Mexico (2012–2024)

---

## Thesis workflow

```mermaid
flowchart LR

A[Stage 1<br>Data preparation and exploratory diagnostics]
--> B[Stage 2<br>Monthly structuring and baseline synoptic composites]

B --> C[Stage 3<br>Baseline atmospheric context and high vs low PM contrasts]

C --> D[Stage 4<br>Synoptic regime interpretation and seasonal consolidation]

D --> E[Stage 5<br>Large-scale climate variability framework<br>(ENSO / interannual modulation)]

subgraph Inputs
AQ[Air quality observations<br>PM10 / PM2.5]
RE[NARR reanalysis<br>Z500, U, V]
PR[Precipitation diagnostics]
end

AQ --> A
RE --> A
PR --> C
```

---

## Stage descriptions

| Stage | Main objective |
|------|----------------|
| **Stage 1** | Data preparation, air-quality climatology diagnostics, and exploratory circulation composites. |
| **Stage 2** | Establish the **monthly p90 extreme-event framework** and construct baseline Z500 anomaly composites. |
| **Stage 3** | Introduce precipitation context and contrast **high vs low pollution regimes (p90 vs p10)** with statistical significance. |
| **Stage 4** | Consolidate circulation patterns into interpretable **synoptic regimes and seasonal structures**. |
| **Stage 5** | Evaluate modulation by **large-scale climate variability** (e.g., ENSO and interannual forcing). |

---

## Conceptual progression

The thesis follows a **progressive diagnostic framework** in which each stage builds upon the previous one:

1. **Data preparation and climatology diagnostics**  
2. **Extreme-event identification and baseline circulation patterns**  
3. **High vs low pollution regime contrasts**  
4. **Seasonal synoptic regime interpretation**  
5. **Climate-scale variability and modulation**

This staged structure ensures that increasingly complex analyses are built upon **physically interpretable and statistically robust foundations**.

---

## Data foundations

The analysis combines three primary datasets:

- **Air-quality observations**  
  Daily city-mean PM₁₀ and PM₂.₅ from the RAMA monitoring network (Mexico City).

- **Atmospheric reanalysis**  
  NARR (NOAA PSL) daily fields:
  - 500 hPa geopotential height (Z500)  
  - 500 hPa zonal wind (U)  
  - 500 hPa meridional wind (V)

- **Hydroclimatic context**  
  NARR precipitation rate (prate), converted to mm/day.

---

## Analytical philosophy

The thesis emphasizes:

- internally consistent event definitions,
- seasonal interpretation of atmospheric dynamics,
- balanced statistical comparisons between event groups,
- and physically interpretable circulation diagnostics.

Each stage therefore focuses on **a limited set of variables and hypotheses** to preserve methodological clarity.

---

© 2026 Erick Rico Esparza  
Tampere University / ICAyCC–UNAM