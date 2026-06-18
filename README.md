# Mundial26 ⚽ — World Cup 2026 Forecaster

A probabilistic forecasting system for the FIFA World Cup 2026. It learns from 150+ years
of international match results, estimates per-match outcome probabilities with a
Dixon–Coles goals model, and runs Monte Carlo simulations of the remaining bracket to
produce live tournament-win probabilities — validated against real results as the
knockouts unfold.

## Project structure
```
mundial26/
├── data/
│   ├── raw/          # the 4 Kaggle CSVs go here
│   └── processed/    # cleaned data written by notebooks
├── notebooks/
│   └── 01_eda.ipynb  # Phase 1: loading + exploratory analysis
├── src/              # reusable modules (added in later phases)
├── app.py            # Streamlit dashboard (later phase)
├── requirements.txt
└── README.md
```

## Setup
```bash
conda create -n mundial26 python=3.11
conda activate mundial26
pip install -r requirements.txt
```

## Data
Source: [International football results 1872–present](https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017) (Kaggle, martj42).
Place `results.csv`, `goalscorers.csv`, `shootouts.csv`, and `former_names.csv` in `data/raw/`.

## Roadmap
1. **EDA & cleaning** ← you are here
2. Baseline classifier (logistic / random forest / XGBoost)
3. Dixon–Coles goals model
4. Monte Carlo bracket simulation
5. Backtesting & calibration (2018, 2022)
6. Live Streamlit dashboard

## Author
Mahmoud Ahmed — [LinkedIn](https://linkedin.com/in/mahmoud-ahmed-9454a8253) · [GitHub](https://github.com/mmahmoudahmedd)
