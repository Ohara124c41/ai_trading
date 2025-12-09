# AI Trading Projects (Udacity)

This repository holds five trading-focused projects covering data prep, portfolio construction, momentum backtesting, classification for signals, and a reinforcement learning agent. Each project lives in its own folder so you can run it independently with Python 3.12+ and standard scientific packages.

## Projects Overview

### 1) backtest_a_dynamic_investment_strategy
- Goal: Build a monthly risk-parity portfolio across ES, ZN, GC, and DX futures.
- Highlights: yfinance download, monthly resample, rolling vol weights (36M), performance stats and drawdown plots.
- Tech: Python, pandas, numpy, matplotlib, yfinance.

### 2) data_transformation_for_trading_models
- Goal: Clean and align Apple, Microsoft, inflation, and GDP data for downstream modeling.
- Highlights: Price cleaning, return calc, inflation resampling, GDP standardization, correlation visuals, exported clean CSVs.
- Tech: Python, pandas, matplotlib, seaborn.

### 3) momentum-based-algorithmic-trading-program
- Goal: Momentum backtest on the S&P 500 using a geometric Brownian motion model and expected shortfall.
- Highlights: SQLite price load, GBM calibration and 10-day forecasts, position sizing from forecasts and ES, wealth tracking plot.
- Tech: Python, numpy, scipy, sqlite3, matplotlib.

### 4) optimize-classification-model-trading
- Goal: Train and tune a binary classifier to predict 5-day XLV direction using VIX, Google Trends, and technical features.
- Highlights: Feature engineering, correlation pruning, RandomForest with GridSearchCV, baseline vs tuned comparison, feature importances.
- Tech: Python, scikit-learn, pandas, numpy, plotly, seaborn, yfinance, ta.

### 5) reinforcement_learning_trading_model
- Goal: Train a Deep Q-Network trading agent on GOOG data.
- Highlights: Feature prep with Bollinger Bands, DQN and Agent setup with replay and epsilon decay, training/testing runs with saved checkpoints.
- Tech: Python, TensorFlow/Keras, numpy, pandas, matplotlib.

## How to work with the repo
1) Enter the project you want (for example `cd momentum-based-algorithmic-trading-program`).
2) Open the notebook in that folder and run cells in order; install any listed dependencies first.
3) Each project folder includes its own README with details, data files, and rubric notes. Follow those for exact steps and settings.
