# Energy-Consumption-Forecasting-in-Steel-Manufacturing-using-Machine-Learning
Energy Consumption Forecasting in Steel Manufacturing using Machine Learning

⚙️ Steel Industry Energy Usage Prediction

This project applies advanced machine learning and feature engineering techniques to predict electricity usage (kWh) in the steel manufacturing sector using historical and operational data. The aim is to support energy optimization, cost reduction, and environmental sustainability through data-driven decision-making.
📁 Dataset

    Source: Steel_industry_data.csv

    Description: The dataset contains timestamped operational metrics and energy usage logs from a steel production facility.

    Target Variable: Usage_kWh (transformed to Usage_log using log1p)

📊 Features Used
✅ Numerical Features (engineered/transformed):

    Lagging and leading reactive power (with log and power transformations)

    CO₂ emissions: CO2(tCO2), CO2_log, CO2_log_pt

    Time-based: hour, is_weekend, NSM

🧩 Categorical Features:

    WeekStatus, day_of_week, Load_Type

🛠️ Workflow Overview
1. Data Preprocessing

    Parsed dates, removed duplicates and handled nulls

    Created time-based features like hour, day_of_week, and is_weekend

    Cleaned categorical columns and ensured consistent casing

2. Exploratory Data Analysis (EDA)

    Plotted distributions, boxplots, and scatter plots

    Identified and removed outliers using IQR method

    Evaluated skewness and corrected via log + power transformation (Yeo-Johnson)

3. Feature Engineering

    Created log-transformed and power-transformed variables

    One-hot encoded categorical features

    Selected top predictors using F-test scores and correlation with target

4. Modeling & Evaluation

Trained and compared multiple regressors:

    Linear Regression

    Random Forest (with RandomizedSearchCV)

    Gradient Boosting (with GridSearchCV tuning)

    K-Nearest Neighbors

    Support Vector Regressor

    Decision Tree

🔍 Evaluation Metrics:

    RMSE

    MAE

    R² Score

    Visualized:

        Predicted vs Actual plots

        Residual distribution plots

        Feature importance (for Gradient Boosting)

🔢 Final Results Summary
## Model Performance Comparison

| Model             | RMSE     | MAE      | R² Score |
|------------------|----------|----------|----------|
| Linear Regression | 0.166014 | 0.123135 | 0.981821 |
| Random Forest     | 0.160562 | 0.105334 | 0.982995 |
| Gradient Boosting | **0.140597** | **0.096073** | **0.986961** |
| K-Neighbors       | 0.162006 | 0.114850 | 0.982688 |
| Support Vector Regression (SVR) | 0.159354 | 0.117611 | 0.983250 |
| Decision Tree     | 0.221236 | 0.141416 | 0.967715 |

**Best Model:** `Gradient Boosting` shows the best performance with the lowest RMSE and MAE, and the highest R² score.



