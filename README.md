# F1 Race Prediction

A collection of Python experiments for predicting Formula 1 race results from historical race data and qualifying or driver-performance features.

## Main project

[`predict_f1.py`](./predict_f1.py) is the primary script. It fetches race results for the 2022–2024 seasons with [FastF1](https://docs.fastf1.com/), builds a Random Forest model, and produces a simulated finishing order for the 2025 Chinese Grand Prix in Shanghai.

The script also saves three visualizations in the current working directory:

- `shanghai_gp_prediction.png` — predicted finishing positions by driver and team
- `grid_vs_finish.png` — simulated starting grid compared with predicted finish
- `team_performance.png` — average predicted position by team

The other `prediction*.py` files are separate experiments with different approaches and assumptions; run them individually if you want to explore them.

## Requirements

- Python 3.9 or later
- Internet access to retrieve historical data through FastF1
- scikit-learn 1.2 or later

Install the packages used by the main script:

```bash
python -m pip install fastf1 pandas numpy scikit-learn matplotlib seaborn
```

## Run

From the project directory:

```bash
python predict_f1.py
```

FastF1's cache is stored in a `f1_cache/` directory under the current working directory. The script prints its prediction and model feature importances to the terminal and writes the charts listed above.

## Notes and limitations

- The race, season range, and 2025 driver lineup are hard-coded in `predict_f1.py`; this is not a live or configurable race-prediction tool.
- The starting grid is simulated with random sampling, so results can vary between runs.
- If too little historical data can be loaded, the script supplements it with synthetic results. Predictions based on that fallback are illustrative, not based entirely on real race results.
- The model is a learning project and does not account for all race-day factors. Predictions are not official results or betting advice.
