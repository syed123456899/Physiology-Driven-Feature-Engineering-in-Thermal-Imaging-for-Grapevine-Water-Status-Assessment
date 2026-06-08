# Reliable Multi-Scale Sensor Fusion Framework for Agricultural Robots

PhD research repository — **AIGreenBots** project, University of Coimbra (ISR-UC & INESC Coimbra).
Funded by the European Union under MSCA **Grant Agreement No. 101169330**.

| | |
|---|---|
| **Author** | Syed Bukhari |
| **Programme** | PhD in Electrical Engineering and Intelligent Systems, University of Coimbra |
| **Supervisor** | Prof. Gil Gonçalves (INESC Coimbra) |
| **Co-supervisor** | Prof. Lino José Forte Marques (ISR-UC) |
| **Project** | AIGreenBots (MSCA GA No. 101169330) |

---

## Overview

This repository tracks my PhD work towards a **reliable multi-scale sensor-fusion framework for agricultural robots** — fusing data from ground IoT, proximal (robot-mounted), UAV, and satellite scales, with calibrated uncertainty and a dynamic digital twin, validated in the field.

The work is organised in three stages that mirror the research progression:

```
01-base-paper/             → the published baseline I build on (Pires et al., 2025)
02-beated-results/         → my ground-scale pilot that beats that baseline
03-satellite-integration/  → ongoing: extending fusion to the satellite scale
poster/                    → CoDEEC 2026 poster (LaTeX source + PDF)
docs/                      → extra documentation, figures, references
```

---

## 1. Base paper — the baseline

**Pires et al. (2025)** — scalable estimation of grapevine water status from ground-based thermal imaging.
This is the reference method my pilot is compared against (R² ≈ 0.656 on stem water potential).

See [`01-base-paper/README.md`](01-base-paper/README.md) for the citation and a summary of the method and dataset.

## 2. Beated results — my ground-scale pilot

A **physiology-driven feature-engineering** approach on the same ground-based thermal data that **outperforms the baseline**:

- Beats the baseline in **> 87 %** of comparisons.
- Reduces residual skewness by **26–55 %** using features alone.
- **Variety-agnostic** (ΔR² ≈ 0.003 across four white varieties).
- Robust to weather-station distance (**0.3–8.3 km**).
- **Probe-free** model improves linear R² from **0.476 → 0.674**.

See [`02-beated-results/README.md`](02-beated-results/README.md) for details, metrics, and where the code/results go.

## 3. Satellite integration — ongoing

The next stage: bringing the **satellite scale** into the fusion pipeline (optical / SAR), aligning it with ground and UAV data so the framework spans all scales — ground IoT → proximal → UAV → satellite.

See [`03-satellite-integration/README.md`](03-satellite-integration/README.md) for the plan and current status.

---

## Poster

`poster/` contains the **CoDEEC 2026** poster (LaTeX source + all figures + compiled PDF).
Build with a single `pdflatex poster.tex` (after compiling the figure `.tex` files). See [`poster/README.md`](poster/README.md).

---

## Status

🔒 **Private repository** — for the author and collaborators only.

| Stage | Status |
|-------|--------|
| Base paper documented | ✅ |
| Ground-scale pilot (beated results) | ✅ completed |
| Satellite integration | 🚧 in progress |
| Multi-scale fusion engine | 🔜 planned |
| Digital twin + field validation | 🔜 planned |

---

## Acknowledgement

This work is carried out within the **AIGreenBots** project, funded by the European Union under MSCA Grant Agreement No. 101169330, with the support of **ISR-UC**, **INESC Coimbra**, and the **University of Coimbra**.
