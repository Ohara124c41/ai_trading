## Risk-Parity Portfolio Analysis

This project builds a risk-parity portfolio using front-month futures for the S&P 500 (`ES=F`), 10-year Treasuries (`ZN=F`), gold (`GC=F`), and the US dollar index (`DX=F`). The workflow lives in `projectv2.ipynb` and walks from data retrieval to performance evaluation.

### What the notebook does
1) **Import & download data**: Pulls ~10 years of futures data via `yfinance`.
2) **Resample & clean**: Resamples daily data to month-end, keeps adjusted closes, forward-fills and drops remaining gaps.
3) **Compute returns**: Calculates monthly arithmetic returns.
4) **Risk-parity weights**: Uses a rolling 36-month volatility window, inverts vol, normalizes weights, and shifts them one period to avoid look-ahead bias.
5) **Portfolio returns**: Applies weights to returns and aggregates to a portfolio series.
6) **Performance metrics**: Annualized return/volatility, skewness, kurtosis, maximum drawdown, Sharpe, Sortino, Calmar.
7) **Visuals**: Plots cumulative returns alongside drawdowns for quick interpretation.

### How to run
1) Open `projectv2.ipynb` in Jupyter/Lab (Python 3 with `pandas`, `numpy`, `matplotlib`, `yfinance` installed).
2) Run all cells in order. The notebook downloads data at runtime.
3) Review printed metrics and the cumulative-return/drawdown plot.

### Rubric alignment (quick reference)
- **Data collection/preprocessing**: yfinance download, monthly resample, cleaned adjusted closes.
- **Risk-parity weights/returns**: Rolling vol weights (36M), shifted, applied to returns.
- **Performance & visualization**: Full metric set plus cumulative-return and drawdown plot on real futures data.
