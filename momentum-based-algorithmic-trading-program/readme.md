# Momentum-Based S&P 500 Trading

This project runs a momentum-driven backtest on the S&P 500. The notebook loads historical prices into SQLite, calibrates a geometric Brownian motion model each day, forecasts prices 10 trading days ahead, computes confidence bands and expected shortfall, and sizes positions from those signals. Results are stored in the `positions` table and plotted over the 2020-06-01 to 2021-05-31 window.

## Contents
- `Project_Learner.ipynb`: main notebook with code, outputs, and plots aligned to the rubric.
- `SP500.csv`: historical price data loaded into the `prices` table.
- `SP500.db`: created by the notebook; holds `prices` and `positions`.

## How to run
1) Use Python 3.12+. Install dependencies: `numpy`, `scipy`, `sqlite3` (std lib), and `matplotlib`.
2) Open `Project_Learner.ipynb` and run all cells. The notebook will load prices, create tables, run the backtest loop, and plot wealth.

## Notes
- Model: GBM calibrated from rolling log returns with bootstrapped moments.
- Signals: 10-day forecast at 95 percent confidence and expected shortfall feed the position sizing rule.
- Backtest: trades are recorded in `positions`; wealth is quantity times price plus cash through 2021-05-31.
