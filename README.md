# Walmart-Sales-Prediction
1. Project Overview

This project focuses on predicting weekly sales for Walmart stores using historical sales data, economic indicators, promotional markdowns, and holiday information.
The dataset contains data from 45 Walmart stores, and the problem is treated as a supervised regression task where Weekly Sales is the target variable.

The project also analyzes the impact of holiday markdown events on different departments and applies dimensionality reduction techniques to reduce overfitting.

2. Problem Formulation

The problem is formulated as a supervised regression problem, where:

Target Variable:
Weekly_Sales

Predictor Variables:

Temperature

Fuel Price

CPI

Unemployment

Week number (seasonality)

Holiday indicator

The goal is to learn a model that can accurately predict weekly sales and identify key factors influencing sales performance.

3. Dataset Description

The Walmart dataset consists of three CSV files:

3.1 Files Used

train.csv – Weekly sales by store and department

features.csv – Economic indicators, markdowns, and holiday information

stores.csv – Store identifiers

3.2 Key Attributes
Feature	Description
Store	Store ID (1–45)
Dept	Department number
Date	Week of sales
Weekly_Sales	Sales amount (target variable)
IsHoliday	Indicates holiday week
Temperature	Store region temperature
Fuel_Price	Fuel cost
CPI	Consumer Price Index
Unemployment	Unemployment rate
4. Data Preprocessing

The following preprocessing steps were applied:

Merging train.csv and features.csv using Store and Date

Converting Date to datetime format

Extracting week number to capture seasonality

Converting holiday indicator into integer format

Handling missing values

Aggregating weekly sales at store level

5. Exploratory Data Analysis (EDA)

EDA was performed to understand trends and patterns in the data.

Key Observations:

Weekly sales show seasonal behavior

Sales increase during holiday weeks

Certain departments experience higher sales uplift during markdown events

Economic indicators such as unemployment and fuel price impact sales negatively

6. Department-Level Holiday Impact Analysis

Department-wise sales were analyzed for holiday and non-holiday periods.

Findings:

Holiday weeks show higher average sales

Departments related to seasonal goods and consumer essentials benefit the most

Holiday markdown events have a significant positive impact on sales

7. Machine Learning Models Implemented
7.1 Linear Regression

Linear Regression was used as a baseline model to understand the relationship between predictors and weekly sales.

Advantages:

Simple and interpretable

Helps understand feature influence

Performance Metrics:

RMSE ≈ 163,400

R² Score ≈ 0.91

7.2 LASSO Regression (Dimensionality Reduction)

LASSO regression was applied to reduce overfitting and perform feature selection.

Why LASSO?

Penalizes large coefficients

Shrinks less important features to zero

Reduces model complexity

Selected features after LASSO indicate the most influential predictors.

7.3 Random Forest Regression

Random Forest is an ensemble learning algorithm that builds multiple decision trees and averages their predictions.

Advantages:

Captures non-linear relationships

Handles feature interactions automatically

Robust against overfitting

Random Forest achieved the best predictive performance among all models used.

8. Model Evaluation Metrics

The following metrics were used to evaluate model performance:

RMSE (Root Mean Squared Error) – Measures prediction error magnitude

R² Score – Measures variance explained by the model

MAPE (Mean Absolute Percentage Error) – Measures relative prediction accuracy

MSSE (Mean Squared Sum Error) – Measures squared error magnitude

9. Feature Importance Analysis

Feature importance was evaluated using:

Linear regression coefficients

LASSO-selected features

Random Forest feature importance scores

Important Features Identified:

Week (seasonality)

Holiday indicator

Unemployment rate

Fuel price

CPI

10. Results Summary
Model	Key Outcome
Linear Regression	Interpretable baseline
LASSO Regression	Reduced overfitting
Random Forest	Best accuracy

Random Forest provided the lowest error and highest prediction accuracy.

11. Limitations

Linear models assume linear relationships

Time-series dependencies were not fully modeled

External factors such as promotions outside markdowns were not included

12. Future Scope

Time-series forecasting using ARIMA or LSTM

Hyperparameter tuning for Random Forest

Department-wise predictive models

Use of advanced ensemble models such as XGBoost

13. Conclusion

This project demonstrates how machine learning techniques can be effectively applied to retail sales forecasting. By combining exploratory analysis, linear models, regularization techniques, and ensemble methods, accurate sales predictions were achieved. Holiday markdowns and economic indicators were identified as significant drivers of weekly sales.

14. Tools & Technologies

Python

Google Colab

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn
