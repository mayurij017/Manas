# MANAS: Student Mental Health Score Prediction

An end-to-end machine learning project that predicts a student's mental health score from lifestyle and academic factors, served as a real-time web app with FastAPI.

> **Disclaimer:** MANAS is an academic project for learning and early-awareness purposes. It is not a clinical or diagnostic tool.

## Highlights
- Regression pipeline with **R² = 0.878** on held-out data
- Full preprocessing: EDA, outlier handling, feature engineering, scaling, ordinal and one-hot encoding
- Random Forest model deployed with **FastAPI + Uvicorn** for real-time predictions

## Tech Stack
Python · Pandas · NumPy · Scikit-learn · FastAPI · Uvicorn · Joblib

## How It Works
1. **EDA:** distributions, correlations, missing values
2. **Cleaning:** outlier handling
3. **Feature engineering:** Country grouping: Retained the 10 most frequent countries and grouped all remaining countries into an “Others” category to reduce categorical complexity and simplify model preprocessing. 
4. **Encoding & scaling:** ordinal encoding for ordered categories, one-hot for the rest, scaling for numeric features
5. **Model:** Random Forest Regressor, evaluated with R²

| Model                    | MAE   | RMSE  |
|--------------------------|-------|-------|
| Random Forest (Default)  | 0.347 | 0.464 |
| Random Forest (Tuned)    | 0.369 | 0.487 |
| Linear Regression        | 0.536 | 0.676 |

6. **Deployment:** model saved with Joblib and served through a FastAPI endpoint

## Dataset
Dataset name: Student Mental Health Dataset


## Results
| Metric | Value |
|--------|-------|
| R²     | 0.878 |

## Future Improvements
- Compare against gradient boosting models
- Add feature importance plots to the app
- Add a simple front-end form

## Author
Mayuri Joshi
