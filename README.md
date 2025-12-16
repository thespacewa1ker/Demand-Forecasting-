# 📊 Daily Demand Forecasting using Machine Learning

This project focuses on forecasting **daily total orders** using historical demand data and machine learning techniques. The objective is to identify key demand drivers and build an accurate forecasting model to support operational and business decision-making.

---

## 🧠 Problem Statement

Accurate demand forecasting helps organizations in:
- Capacity planning  
- Resource allocation  
- Cost optimization  

Using historical daily order data, this project predicts **Total Orders** based on multiple operational and time-based features.

---

## 📁 Dataset Overview

- **Type:** Historical daily demand data  
- **Observations:** 60 days  
- **Features:** 12 independent variables  
- **Target Variable:** `Total_Orders`  

### Key Features:
- Non-Urgent Orders  
- Urgent Orders  
- Order Type A, B, C  
- Banking Orders (1, 2, 3)  
- Fiscal Sector Orders  
- Traffic Controller Orders  
- Day of Week  
- Week of Month  

✔ No missing values in the dataset.

---

## 🔍 Exploratory Data Analysis (EDA)

### Descriptive Statistics
- Average total orders ≈ **300**
- Fiscal sector and some banking orders show high variance and outliers

### Key Observations:
- Order types show increasing mean patterns
- Most features are well-distributed
- Outliers handled during modeling

---

## 📈 Order Pattern Analysis

- Non-Urgent Orders peak on **Mondays** and decrease towards Friday
- Urgent Orders follow a similar weekly trend
- Order Type A contributes the highest share among order types

This indicates clear **weekly seasonality** in demand.

---

## 🔗 Correlation Analysis

- Strong correlation between order categories and total orders
- Multicollinearity detected among several features

---

## ⚙️ Feature Engineering

- One-Hot Encoding applied to:
  - Day of Week
  - Week of Month
- Categorical variables converted to numerical format for regression models

---

## 🧪 Models Used

### 1️⃣ Linear Regression (OLS)

**Model Diagnostics:**
- Data follows normal distribution
- No autocorrelation in residuals
- High multicollinearity observed

**Significant Variables:**
- Order Type A  
- Order Type B  
- Order Type C  
- Banking Orders 2  
- Banking Orders 3  

---

### 2️⃣ PCA + OLS Regression

- Principal Component Analysis (PCA) used to reduce multicollinearity
- Regression performed on principal components
- Improved model stability and performance

---

### 3️⃣ Influence Variable Check

- Influential observations identified using residual analysis
- Removing these improved overall model robustness

---

## ✅ Final Model

- PCA + OLS Regression
- Strong explanatory power and stable predictions

### Major Demand Drivers:
- Non-Urgent Orders  
- Banking Orders (1, 2, 3)  
- Traffic Controller Orders  
- Day and Week-based features  
- Fiscal Sector Orders  

---

## 📊 Forecasting Results

- **R² Score:** 98.1%  
- **RMSE:** 13.19%  

### Results Summary:
- Predicted values closely match actual values
- Residuals are randomly distributed
- Model generalizes well on test data

---

## 🛠️ Tech Stack

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Statsmodels  
- Scikit-learn  

---

## 📌 Key Takeaways

- Demand exhibits strong weekly patterns
- Multicollinearity is common in operational datasets
- PCA combined with regression improves forecasting accuracy
- Statistical validation is essential for reliable predictions 

---

## 🚀 Future Improvements

- Implement time-series models (ARIMA, SARIMA, Prophet)
- Use longer historical datasets
- Include external factors like holidays and promotions


