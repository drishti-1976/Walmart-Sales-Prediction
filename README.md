# 🛒 Walmart Sales Prediction using Machine Learning

## 📌 Project Overview
This project aims to predict **Weekly Sales** for Walmart stores using historical sales data, economic indicators, promotional markdowns, and holiday information.

The dataset includes sales data from **45 Walmart stores** across multiple departments.  
The problem is formulated as a **supervised regression task**, where **Weekly Sales** is the target variable.

This project was developed as part of an **Internship / Academic Data Science Project** using **Python and Google Colab**.

---

## 🎯 Objectives
- Predict weekly sales using machine learning models
- Analyze the impact of **holiday markdown events**
- Identify departments affected by holidays
- Reduce overfitting using **dimensionality reduction**
- Compare linear and non-linear regression models

---

## 📂 Dataset Description
The project uses the **Walmart Sales Dataset**, consisting of three CSV files:

| File Name | Description |
|----------|------------|
| `train.csv` | Historical weekly sales by store and department |
| `features.csv` | Economic indicators, markdowns, and holiday data |
| `stores.csv` | Store type and size information |

### Target Variable
- **Weekly_Sales**

### Important Features
- Temperature  
- Fuel Price  
- CPI  
- Unemployment  
- Markdowns  
- Holiday Indicator  
- Store ID  

---

## 🧠 Methodology

### 1️⃣ Data Preprocessing
- Merged datasets using `Store` and `Date`
- Converted dates to datetime format
- Engineered **Week Number** feature
- Converted holiday flag to numeric
- Applied **one-hot encoding** to Store IDs

---

### 2️⃣ Exploratory Data Analysis (EDA)
- Visualized weekly sales trends
- Analyzed store-wise and department-wise sales
- Compared holiday vs non-holiday sales
- Identified departments with highest holiday impact

---

### 3️⃣ Feature Engineering
- Created time-based features
- Encoded categorical variables
- Selected economic indicators as predictors

---

### 4️⃣ Linear Regression Model
A **Linear Regression model** was trained as a baseline model to predict weekly sales.

**Features used:**
- Temperature  
- Fuel Price  
- CPI  
- Unemployment  
- Week Number  
- Holiday Indicator  
- Store Dummy Variables  

This model provides interpretability and baseline performance.

---

### 5️⃣ Model Evaluation
The models were evaluated using the following metrics:
- **R² Score**
- **RMSE**
- **MAPE**
- **MSSE**

**Linear Regression Results:**
- R² Score ≈ **0.91**
- MAPE ≈ **8.9%**
- RMSE ≈ **163,400**

---

### 6️⃣ Dimensionality Reduction (Lasso Regression)
To reduce overfitting:
- Implemented **Lasso Regression**
- Applied coefficient shrinkage
- Selected only important features
- Improved generalization performance

---

### 7️⃣ Random Forest Regression
To capture non-linear patterns:
- Implemented **Random Forest Regressor**
- Improved prediction stability
- Achieved better performance compared to linear models

---

### 8️⃣ Holiday Impact Analysis
- Grouped sales by **Department** and **Holiday**
- Calculated average sales difference
- Ranked departments based on holiday impact

This analysis helps understand promotional effectiveness.

---

## 📊 Model Comparison

| Model | R² Score | Performance |
|------|---------|-------------|
| Linear Regression | ~0.91 | Baseline |
| Lasso Regression | ~0.91+ | Reduced Overfitting |
| Random Forest | Highest | Best Performance |

---

## 🛠 Technologies Used
- Python
- Google Colab
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Linear Regression
- Lasso Regression
- Random Forest Regression

---

## 📁 Project Structure
```text
Walmart-Sales-Prediction/
│
├── internproject.ipynb
├── README.md
├── requirements.txt
└── data/
    ├── train.csv
    ├── features.csv
    └── stores.csv


