## Data Transformation for Trading Models

A short, end-to-end walkthrough of cleaning, aligning, and exploring market and macro data for Apple, Microsoft, inflation, and GDP. The work lives in `Preparing-for-data-analysis-project-student.ipynb`; all derived CSV outputs are saved alongside it.

### Dataset inventory
- `apple_historical_data.csv`, `microsoft_historical_data.csv`: Daily OHLCV with dollar-formatted prices.
- `inflation_monthly.csv`: Monthly core inflation series.
- `GDP.csv`: Quarterly GDP levels.
- `consumer_price_index.csv`: Duplicate of inflation source (kept for reference).

### Processing highlights
- Load from GitHub with local fallback.
- Clean price columns (remove `$`/`,` and cast to numeric), parse dates, sort.
- Forward-fill missing prices, compute daily returns.
- Align inflation to month-end; resample to weekly (interpolated) and quarterly (mean).
- Standardize GDP (min–max) into `GDP_standardized`.
- Export cleaned/derived CSVs:
  - `apple_prices_clean.csv`, `microsoft_prices_clean.csv`
  - `inflation_monthly_aligned.csv`, `inflation_weekly_interpolated.csv`, `inflation_quarterly_avg.csv`
  - `gdp_standardized.csv`
  - `returns_inflation_corr_data.csv`

### EDA visuals (last 3 months focus)
- Apple open vs close line chart.
- Histogram of Apple closing prices.
- Correlation heatmap: Apple returns, Microsoft returns, inflation change.
- Dual-axis plot: Apple close vs 1-week rolling volatility.

### How to run
1) Open `Preparing-for-data-analysis-project-student.ipynb` in Jupyter/Lab.
2) Run all cells (Python 3, pandas/matplotlib/seaborn installed).
3) Outputs are written to the repo root as listed above.

