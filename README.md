# Customer Growth Forecasting using SARIMA

This repository contains a Jupyter Notebook (`customer-growth-forecasting-sarima.ipynb`) demonstrating a time series forecasting project. The primary goal is to predict future customer growth (visitor reservations) for restaurants using historical data and a Seasonal Autoregressive Integrated Moving Average (SARIMA) model.

## Project Overview

This project forecasts restaurant visitor numbers using historical data and a SARIMA model. Key steps include data loading, cleaning, time series analysis (seasonality), model implementation, and performance evaluation (MAPE).

## Key Highlights

* **Comprehensive Data Handling**: Demonstrated proficiency in loading, cleaning, and transforming raw data from multiple sources for time series analysis.
* **Time Series Analysis**: Identified and visualized seasonal patterns (weekly/monthly) in customer visitation data.
* **Predictive Modeling**: Applied a SARIMA model for forecasting, showcasing understanding time series techniques.
* **Critical Evaluation & Problem Solving**: Thoroughly evaluated model performance (MAPE) and proposed actionable next steps for improvement, highlighting analytical rigor and strategic thinking.

## Dataset

Three interconnected datasets are used:
* `restaurants_visitors.csv`: Visitor reservation details (`reserve_visitors` as target).
* `store_info.csv`: Restaurant details.
* `date_info.csv`: Calendar information.

## Data Analysis & Preprocessing

This phase combined Exploratory Data Analysis (EDA) and Data Wrangling. Initial data quality checks addressed a date format error. Outliers in `reserve_visitors` were identified via visualizations. `dayofweek` and `month` features were engineered for seasonality. Visitor data was aggregated into a daily time series, and duplicates removed.

## Forecasting Model (SARIMA)

A SARIMA model was chosen for forecasting, leveraging observed seasonality. Data was split into training/test sets. `pmdarima.auto_arima` identified optimal parameters, using a seasonal period (m=7). The model generated 31-day predictions, with a MAPE of **459.21%**.

## Results & Future Work

The SARIMA model's high MAPE (459.21%) indicates limitations, emphasizing iterative development. Future work will focus on:
* **Addressing Data Complexity**: Incorporate multiple seasonalities and external factors (holidays, promotions, weather) via SARIMAX using `genre_name`, `area_name`, and `holiday_flg`.
* **Enhanced Data Handling**: Implement robust outlier/anomaly handling and advanced feature engineering (lagged values, rolling statistics).
* **Model Exploration**: Investigate alternative models like Prophet, ETS, or ML models (XGBoost, LSTMs) if needed.
This demonstrates a strong analytical mindset crucial for tackling real-world forecasting challenges.

## Relevant Graphs

<img width="1005" height="634" alt="image" src="https://github.com/user-attachments/assets/f533c2d3-cb23-47a6-814f-4060c4ffbf25" />

