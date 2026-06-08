# 02 — Beated Results (Ground-Scale Pilot)

My pilot study that **outperforms the baseline** ([01-base-paper](../01-base-paper/)).

## Idea

**Physiology-driven feature engineering** on ground-based thermal imaging: instead of feeding raw thermal features to the model, derive features motivated by plant water-stress physiology, then train a model pool. The richer, physiology-aware representation predicts **grapevine stem water potential** more accurately and more robustly.

- Features expanded **30 → 176**.
- Model pool of **12 models × 20 random seeds** for robust comparison.

## Results vs baseline

| Metric | Baseline (Pires et al. 2025) | This pilot |
|--------|------------------------------|------------|
| R² (stem water potential) | 0.656 | **0.674** |
| Probe-free linear R² | 0.476 | **0.674** |
| Wins vs baseline | — | **> 87 %** of comparisons |
| Residual skewness | — | **↓ 26–55 %** |
| Variety transfer (ΔR²) | — | ≈ **0.003** (variety-agnostic) |
| Weather-station distance | — | robust **0.3–8.3 km** |

## What goes in this folder

```
02-beated-results/
├── README.md            (this file)
├── code/                your training / feature-engineering scripts
├── results/             metrics tables, figures, model outputs
└── figures/             charts used in the paper / poster
```

Suggested:
- `code/` — feature engineering, model pool, evaluation, seeds.
- `results/` — CSVs of per-model / per-seed metrics, skewness numbers.
- `figures/` — the R² comparison and residual-skewness charts.

> ⚠️ If the underlying data is from the base paper, keep it out of the repo and point to the original source. Commit only your **code, derived features, and results**.

## Reproducing

Add a short "how to run" once the scripts are in (`requirements.txt` + a `python train.py ...` line). A `requirements.txt` placeholder is included.
