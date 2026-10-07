# 🏎️ F1 Predictions - Machine Learning Model

Welcome to the F1 Predictions repository! This project uses machine learning, the FastF1 API, and historical Formula 1 race results to predict race outcomes and rank drivers for upcoming Grand Prix weekends.

---

## 🚀 Project Overview

This repository contains a Gradient Boosting Machine Learning model that predicts race results based on past performance, qualifying times, and other structured F1 data. The model leverages:
- **FastF1 API** for historical race data, lap times, and telemetry.
- **Historical Race Results** (e.g., 2024 season) to establish performance baselines.
- **Current Season Qualifying Results** to generate starting grid context.
- **Continuous Updates:** Additional race data is integrated over the course of the season to improve model accuracy.
- **Feature Engineering techniques** to refine prediction accuracy.

---

## 📊 Data Sources

- **FastF1 API:** Fetches granular lap times, race results, and telemetry data.
- **Qualifying Data:** Utilized as a primary input for race day predictions.
- **Historical F1 Results:** Processed and cleaned from FastF1 for training the Gradient Boosting model.

---

## 🏁 How It Works

1. **Data Collection:** The script pulls relevant F1 session data using the FastF1 API.
2. **Preprocessing & Feature Engineering:** Converts lap times, normalizes driver names, and structures the race data for machine learning.
3. **Model Training:** A Gradient Boosting Regressor is trained using historical race results.
4. **Prediction:** The model predicts overall race times for the upcoming Grand Prix and ranks the drivers accordingly.
5. **Evaluation:** Model performance is measured using Mean Absolute Error (MAE).

---

## 📦 Dependencies

Ensure you have the following installed to run the pipeline:
- `fastf1`
- `numpy`
- `pandas`
- `scikit-learn`
- `matplotlib`

---

## 📂 File Structure

For every race, the prediction script is numbered in correlation to the race on the calendar calendar. 

```text
├── prediction1.py    # Round 1 - Australia
├── prediction2.py    # Round 2 - China
├── prediction3.py    # Round 3 - Japan
└── requirements.txt
