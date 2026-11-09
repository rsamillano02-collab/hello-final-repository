# 🍷 Wine Quality Prediction System

A classroom prototype (Data Mining Laboratory, Section B) that classifies a red-wine sample as **GOOD QUALITY** or **NEEDS IMPROVEMENT** based on its physicochemical measurements.

## Problem
A small wine producer needs a consistent, preliminary way to screen wine samples using recorded physicochemical measurements, before deeper quality assessment.

## Dataset
[UCI Machine Learning Repository — Wine Quality (Red Wine)](https://archive.ics.uci.edu/dataset/186/wine+quality)

Predictors: fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol.

## Prediction rule
- `quality >= 6` → **GOOD QUALITY**
- `quality < 6` → **NEEDS IMPROVEMENT**

The original `quality` score is used only to build the target. It is **never** used as an input feature (to avoid target leakage).

## Technologies
Python 3.10+, pandas, scikit-learn (Random Forest), joblib, Streamlit, GitHub

## Installation and run steps
```bash
# 1. Clone the repository
git clone https://github.com/YOUR-USERNAME/wine-quality-prediction.git
cd wine-quality-prediction

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download the dataset, train the model, and save wine_model.pkl
python train_model.py

# 4. Run the Streamlit app
streamlit run app.py
```
Open http://localhost:8501 in your browser. Download the sample input CSV from the app and upload it to test predictions.

## Features
- Dataset summary and preview
- Sample input CSV download
- CSV upload with required-column validation
- Prediction results table and CSV download

## Limitations
- Trained only on a specific red-wine dataset; may not generalize to other wine types, producers, regions, or testing conditions.
- Predictions are a **preliminary screening aid only** — not a substitute for laboratory testing, sensory evaluation, food-safety procedures, or professional quality-control decisions.
