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
Model	RMSE	MAE	R²
Linear Regression	...	...	...
Random Forest	...	...	...
Gradient Boosting (Tuned)	✅ Best	✅ Best	✅ Best

    Note: Replace ... with actual scores from your results_df.

📈 Sample Predictions
Index	Predicted kWh	Actual kWh
1	1234.56	1278.90
2	1456.78	1490.12
...	...	...
