# Gaia open-cluster mass-function turnover: data and code

This local GitHub-ready package accompanies **The Gaia Open-Cluster Mass-Function Turnover: An Outcome-Blind Test of a Present-Day Dissolution Coordinate**. It preserves accepted derived products and historical code. It has not been published; no repository URL or DOI is assigned.



```sh
python3 verify_accepted_results.py
python3 verify_manifest.py
```

The checks use only Python's standard library. Optional deterministic figure reproduction:

```sh
python3 -m pip install -r requirements-figures.txt
MPLBACKEND=Agg MPLCONFIGDIR=/tmp/mf_plot_cache python3 figure_scripts/redesign_story.py
MPLBACKEND=Agg MPLCONFIGDIR=/tmp/mf_plot_cache python3 figure_scripts/realdata_from_retained_values.py
```

Outputs go to ignored `generated/`. These commands use retained values only and do not fit models or compute predictive scores. Figure 3 is a post-outcome descriptive visualization; its dashed coefficient is a retained reference, not a new regression. Rendering need not be byte-identical across library/font versions.

## Contents

- `accepted_results.json`: current scientific summaries and component statuses.
- `accepted_diagnostics/`: derived 156-cluster plotting table, selection diagnostics, uncertainty summaries, retained age-model replay.
- `accepted_figures/`: accepted publication figure assets.
- `figure_scripts/`: portable, deterministic reproduction of Figures 1, 3 and 4.
- `historical/outputs/`: retained predictor tables, frozen rules, scalar results and weighting diagnostics.
- `historical/scripts/`, `historical/phase3/`, `historical/influence/`: historical analysis code and provenance, preserved byte-identical.
- `environment/`: recorded environment, not a guarantee of the original runtime or random state.
- `manuscript/`: manuscript text and bibliography for context; this is not the complete LaTeX submission bundle.
- `DATA_SOURCES.md`, `DATA_DICTIONARY.md`, `REPRODUCIBILITY.md`: retrieval instructions, field definitions and replay limits.
- `MANIFEST.sha256`: integrity checks for every packaged file except the manifest itself.

**Do not run historical scripts as an automated reproduction pipeline.** They include fitting, simulations, orbit calculations and downloads; some require original workspace paths and unbundled upstream products. The scientific analysis is frozen. Read `REPRODUCIBILITY.md` before using that code.


