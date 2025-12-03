# Reinforcement Learning Trading Model

Hands-on project to build and train a Deep Q-Network (DQN) trading agent on historical GOOG data. The workflow lives in `project_nb.ipynb`, which guides you through data prep, feature engineering, agent definition, training, and testing.

## Contents
- `project_nb.ipynb`: main notebook with filled cells for the end-to-end RL pipeline.
- `GOOG_2009-2010_6m_RAW_1d.csv`: daily price data used for training/testing.
- `model_ep0.keras`, `model_ep2.keras`: sample saved checkpoints from training runs.
- `instructions.md`: rubric checklist and guardrails for working in the notebook.

## How to run
1) Open `project_nb.ipynb` (Python 3.x). Run cells in order; first cells load dependencies.
2) Notebook steps: clean/plot data, compute Bollinger Bands, normalize features, split train/test, define DQN + Agent with epsilon-greedy policy and experience replay, train over episodes, and test using a saved checkpoint.

## Notes
- Training rewards are based on realized profit from buy/sell actions; epsilon decays each replay cycle.
- Plots for price/indicators, training behavior, and loss are generated during training/testing. Adjust episodes/epsilon decay to experiment with different behaviors.
