# CoDEEC 2026 Poster

A1 portrait poster presenting the PhD thesis proposal at **CoDEEC 2026 Summer Edition** (17 June 2026), DEEC, University of Coimbra.

## Files

| File | What it is |
|------|------------|
| `CoDEEC2026_Poster.pdf` | Compiled poster (ready to print) |
| `poster.tex` | Main LaTeX source (tikzposter, A1 portrait) |
| `framework_viz.tex/.pdf` | Multi-scale framework pipeline diagram |
| `gantt_viz.tex/.pdf` | Work-plan Gantt chart (native, large fonts) |
| `results_chart.tex/.pdf` | R² baseline-vs-ours bar chart |
| `skew_viz.tex/.pdf` | Residual-skewness chart |
| `scales_viz.tex/.pdf` | Sensor-scale icons (IoT→proximal→UAV→satellite) |
| `thermal_viz.tex/.pdf` | Thermal-imaging concept figure |
| `map_viz.tex/.pdf` | Study-area map (Portugal: Coimbra & Lisbon) |
| `uc_white.png`, `deec.png`, `isr.png` | Institution logos (header) |

## Build

The figure `.pdf` files are already included, so to rebuild the poster:

```bash
pdflatex poster.tex
```

To regenerate a figure after editing its source (e.g. the Gantt):

```bash
pdflatex gantt_viz.tex      # then rebuild the poster
pdflatex poster.tex
```

## Notes

- Built with **tikzposter** (`a1paper, portrait`), base font 17 pt.
- All diagrams/charts are **native TikZ/pgfplots** (vector, crisp at any size).
- The skewness chart uses representative per-model values — swap in exact numbers if needed.
- Verify against the official UC CoDEEC template before final submission.
