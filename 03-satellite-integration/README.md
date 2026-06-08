# 03 — Satellite Integration (Ongoing)

Extending the framework from ground scale to the **satellite scale**, so fusion spans all scales:
**ground IoT → proximal (robot) → UAV → satellite.**

## Goal

Bring **satellite data (optical / SAR)** into the pipeline and align it spatially and temporally with the ground/UAV observations, then fuse — moving from the single-scale ground pilot ([02-beated-results](../02-beated-results/)) towards the full multi-scale, uncertainty-aware framework.

## Planned steps

1. **Acquire** satellite imagery for the study site/period (e.g. Sentinel-2 optical, Sentinel-1 SAR).
2. **Pre-process**: atmospheric correction, cloud masking, resampling to a common grid.
3. **Align** with ground/UAV data (spatio-temporal registration & harmonisation).
4. **Fuse**: feature-level + probabilistic fusion, carrying **calibrated uncertainty**.
5. **Evaluate**: accuracy, calibration, robustness to missing/degraded inputs.

## What goes in this folder

```
03-satellite-integration/
├── README.md            (this file)
├── data-access/         scripts/notes to fetch & preprocess satellite data
├── alignment/           registration & harmonisation with ground/UAV
├── fusion/              multi-scale fusion experiments
└── results/             metrics & figures
```

## Status

🚧 **In progress.** This stage is being built out — expect frequent changes.

> Tip: keep large raster files out of git (use `.gitignore`); store only code, configs, and small result artifacts. For big data, link to the source or use Git LFS / external storage.
