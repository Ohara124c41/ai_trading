# Optimize Classification Model Trading

This project trains and tunes a binary classifier to predict 5-day price direction for the XLV ETF using VIX levels, Google Trends for "recession," and engineered technical features. The notebook `project_starter.ipynb` walks through data loading, feature engineering, correlation analysis, model tuning, and evaluation.

## Contents
- `project_starter.ipynb`: completed notebook with code, plots, and answers aligned to the rubric.
- `xlv_data.csv`, `vix_data.csv`, `GoogleTrendsData.csv`: provided datasets (daily XLV/VIX, monthly Google Trends).
- `instructions.md`: quick rubric and workflow reminders.

## How to run
1) Open `project_starter.ipynb` and run all cells (Python 3.12+). First cell installs required packages (`yfinance`, `ta`, `plotly`, `seaborn`).
2) Follow the notebook outputs for data prep, feature engineering, correlation pruning, RandomForest training with GridSearchCV, and evaluation (full vs. reduced feature sets).

## Notes
- Baseline accuracy (majority class) is ~0.554; tuned models achieve similar but slightly lower accuracy, illustrating the challenge of short-horizon prediction.
- Feature importances highlight Bollinger mid-band, Google Trends recession interest, volume, VIX, and historical returns as top contributors.
