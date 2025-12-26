# aaple-returns-ml
Predicting next-day AAPL returns using machine learning
This project builds a time-series machine learning pipeline to predict
next-day stock returns for Apple Inc. (AAPL) using historical price-based features.

## Motivation
Daily stock returns are noisy and difficult to predict. This project
demonstrates a realistic, leakage-free approach to return forecasting
and evaluates whether simple machine learning models add value beyond
naive baselines.

## Data
- Source: Yahoo Finance (`yfinance`)
- Time period: 2018–2025
- Frequency: Daily

## Features
- Lagged returns (1-day, 5-day, 10-day)

## Models
- Naive baselines (zero return, lag-1 return)
- Linear Regression
- Random Forest Regressor

## Evaluation
- Time-based train/test split (pre/post 2022)
- Root Mean Squared Error (RMSE)
- Directional accuracy
- Feature importance analysis

## Results
The models perform similarly to naive baselines, consistent with
the low signal-to-noise ratio in daily equity returns. Predictions
cluster near zero, reflecting conservative RMSE-minimizing behavior.

## Key Takeaways
- Proper evaluation matters more than headline accuracy
- Stock return prediction is challenging even with ML
- Honest baselines prevent overfitting and false conclusions

## Technologies
- Python
- pandas
- numpy
- scikit-learn
- yfinance
- matplotlib
