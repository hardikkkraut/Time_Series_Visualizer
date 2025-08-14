# Time Series Visualizer

## Overview
This project explores and visualizes temporal patterns in a univariate time series. It covers cleaning and resampling, rolling statistics, seasonal decomposition, and clear, publication-style plots for trend, seasonality, and anomalies.

## Dataset
# - **Location**: data/ folder in this repository
# - **Format**: CSV with a datetime column and a numeric value column
# - **Notes**: Ensure the datetime column is parsed with the correct timezone/format

## Implementation
# 1. Data loading with parse_dates and index set to the datetime column.
# 2. Cleaning: handle duplicates, sort by date, drop impossible or extreme outliers via IQR/z-score.
# 3. Resampling to daily/monthly frequency and computing rolling mean/median for smoothing.
# 4. Decomposition using statsmodels.tsa.seasonal_decompose to separate trend/seasonality/residuals.
# 5. Visualization: line plots for raw vs. smoothed series, monthly bar charts, yearly box plots.
# 6. Exporting figures to eports/figures/ and saving tidy intermediate CSVs to rtifacts/.

## Tech Stack
# Python, Pandas, NumPy, Matplotlib, Seaborn, Statsmodels

## Results
# - Cleaned series with clearly identified long-term trend and seasonal behavior.
# - Diagnostic plots (ACF/PACF optional) to inform downstream modeling.
# - Reproducible pipeline with saved artifacts for further forecasting tasks.

## How to Run
   python -m venv .venv
   .venv\Scripts\activate    # Windows
   pip install -r requirements.txt
   python src/visualize.py      # generates figures into reports/figures

## Project Structure
# - data/                # raw or preprocessed CSVs
# - src/                 # data loading, cleaning, visualization scripts
# - artifacts/           # intermediate cleaned/resampled CSVs
# - reports/figures/     # exported PNG charts
# - requirements.txt
# - README.md

## Reproducibility
# - Python 3.9+ recommended
# - Install exact package versions via equirements.txt
# - Set a global random seed where applicable for deterministic splits

## Future Improvements
# - Add forecasting models (ARIMA/Prophet/ETS) with cross-validation.
# - Automate report generation (Jupyter/nbconvert or Markdown reports).
# - Add anomaly detection (STL+IQR or Twitter/ADTK style detectors).

# ---
Author: Hardik Raut • GitHub: https://github.com/hardikkkraut

