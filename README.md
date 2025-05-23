# Conformal Prediction in Finance

This repository provides a complete workflow for applying conformal prediction methods to financial time series, demonstrated on AAPL stock returns.

## Contents

- `conformal_prediction_full_workflow.ipynb`: Jupyter notebook implementing:
  - Data download & preparation (using `yfinance`)
  - Feature engineering (lags, rolling mean & volatility)
  - Split‑conformal (MAPIE “base”) and Jackknife+ (cross‑conformal) prediction intervals
  - Rolling‑window backtests of interval width and coverage

## Requirements

Install the required Python packages:

```bash
pip install yfinance mapie scikit-learn matplotlib pandas
```

## Usage

1. Clone this repository:
   ```bash
git clone <repo-url>
cd <repo-folder>
```
2. Launch Jupyter Notebook:
   ```bash
jupyter notebook
```
3. Open and run `conformal_prediction_full_workflow.ipynb`.

## Interpretation

- **Split‑Conformal** (method="base"): fast, constant-width intervals with guaranteed coverage.
- **Jackknife+** (method="plus"): adaptive-width intervals that tighten in calm regimes and widen in volatile ones.



