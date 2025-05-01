MTN Ghana Volatility Forecasting Using GARCH Models

This project applies ARCH and GARCH family models to forecast stock return volatility for MTN Ghana using R. It demonstrates practical skills in time series modeling, financial data analysis, and risk forecasting relevant to both banking and oil & gas sectors.

# Duration

February – March 2025

# Dataset

MTN Ghana daily stock prices (custom .csv file cleaned and processed)

Columns: Date, Price

# Project Overview

Objective: Forecast stock return volatility and identify risk patterns using GARCH-type models.

Approach: Data cleaning (removing NAs, formatting date/price)

Log return computation

Stationarity testing (ADF, KPSS)

ARCH effect test (Lagrange Multiplier)

Model fitting: GARCH(1,1), EGARCH, TGARCH

Forecasting: 30-day ahead volatility

Rolling window forecasting and comparison

# Key Steps
Preprocessing: Cleaned price column, computed log returns, removed NAs.

Stationarity Check: ADF and KPSS tests confirmed stationarity of returns.

ARCH Effect: Significant ARCH effect detected (p < 0.01), justifying GARCH modeling.

# Model Fitting:
GARCH(1,1): Detected volatility clustering, β₁ = 0.9271 (high persistence).

EGARCH: Captured asymmetry (leverage effect with γ > 0).

TGARCH: Modeled shock sensitivity, especially negative events.

Forecasting: 30-day volatility forecasts matched real patterns in calm periods (RMSE < 2%).

Diagnostics: Ljung-Box and Jarque-Bera confirmed residual quality.

Rolling Forecasting: Implemented a rolling window forecast to simulate real-time prediction.

# Tools & Packages
Language: R

Packages: rugarch, tseries, forecast, PerformanceAnalytics, ggplot2, FinTS

Techniques: Time series modeling, residual diagnostics, statistical testing, visualization

# Key Results

30-day GARCH(1,1) forecast showed strong alignment with realized volatility

EGARCH revealed that positive shocks caused more volatility than negative (unexpected asymmetry)

Rolling window RMSE: ~1.7% | MAE: ~1.2%

Forecasts useful for short-term risk evaluation

# Applications

Banking: Useful for forecasting asset return volatility, managing treasury risk, and building risk models.

Oil & Gas: Helps forecast commodity price volatility, budget sensitivity analysis, and project cost-risk planning.

# What I Learned

Building end-to-end time series pipelines

Applying volatility models in R

Diagnosing model performance

Communicating results with plots and summaries

# Repository Structure

MTN-Ghana-Volatility-Forecasting/
├── data/
│   └── MTN_GH.csv
├── scripts/
│   └── mtn_volatility_model.R
├── plots/
│   └── returns_plot.png
│   └── volatility_forecast.png
└── README.md

# How to Use

Clone repo and run script using RStudio.

Input dataset: data/MTN_GH.csv

Output: diagnostic plots, volatility forecasts, error metrics
