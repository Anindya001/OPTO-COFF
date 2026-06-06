# Optocoupler Thermal-Cycling Reliability Study

Single-script Python analysis for an optocoupler thermal-cycling reliability study with exact right-censoring, Weibull-Coffin-Manson modeling, sensitivity models, Bayesian inference, and publication-style tables and figures.

## Repository Contents

- `optocoupler_thermal_reliability_study_pubrev_v2.py` - final revised analysis script.
- `optocoupler_thermal_reliability_study.py` - earlier analysis version kept for traceability.
- `optocoupler_ttf_unit_level.csv` - unit-level thermal-cycling dataset.
- `results_optocoupler_reliability/` - current generated outputs, including tables, figures, summaries, and revision reports.
- `old results/` - prior generated outputs used for numeric comparison in the revised script.
- `Plan.txt` - original implementation prompt/plan.

## Requirements

Python 3.10 or newer is recommended.

Install dependencies:

```bash
pip install -r requirements.txt
```

The analysis uses only:

- `numpy`
- `scipy`
- `pandas`
- `matplotlib`

## Run

From the repository root:

```bash
python optocoupler_thermal_reliability_study_pubrev_v2.py
```

The script reads `optocoupler_ttf_unit_level.csv` and writes outputs to:

```text
results_optocoupler_reliability/
```

The script uses fixed random seeds for reproducibility. A full run can take time because it includes MCMC, bootstrap/profile-likelihood work, sensitivity analysis, and figure generation.

## Key Outputs

- `results_optocoupler_reliability/run_summary.txt`
- `results_optocoupler_reliability/paper_results_summary.txt`
- `results_optocoupler_reliability/revision_report.md`
- `results_optocoupler_reliability/tables/`
- `results_optocoupler_reliability/figures/`
- `results_optocoupler_reliability/revised_figures/`

## Notes

The repository intentionally includes generated results so it can be uploaded to GitHub as a complete analysis package. Local Python cache files and editor workspace files are excluded.
