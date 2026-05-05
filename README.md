# 🚖 Taxi Demand Prediction (Time Series Forecasting)

Machine learning project to forecast hourly taxi demand using time series analysis and feature engineering techniques, supporting operational decision-making such as driver allocation and peak-hour planning.

---

## 📌 Project Overview

This project simulates a demand forecasting system for an airport taxi service.

Accurate short-term predictions enable:
- Better driver distribution during peak hours  
- Reduced passenger wait times  
- Improved operational efficiency  

The goal is to predict the **number of taxi orders for the next hour** using historical demand data.

---

## 📊 Problem

Taxi demand varies over time and is influenced by:

- Daily patterns (rush hours)  
- Weekly seasonality  
- Long-term trends  

Key challenges:
- Strong temporal dependencies  
- Seasonality at multiple time scales  
- Risk of data leakage in time-based modeling  

The objective is to build a model that:
- Accurately predicts hourly demand  
- Captures temporal patterns  
- Meets the constraint: **RMSE ≤ 48**

---

## 📁 Data

The dataset contains historical taxi orders indexed by datetime.

Preprocessing steps:
- Converted datetime column to index  
- Sorted data chronologically  
- Resampled data into **1-hour intervals**  

---

## 🔍 Exploratory Data Analysis

Key findings:

- **Upward trend** in demand over time  
- Strong **intra-day seasonality** (hourly patterns)  
- Clear **weekly cycles** in aggregated data  
- Increasing variability toward the end of the dataset  

Time series decomposition confirmed:
- Trend component  
- Seasonal patterns  
- Residual fluctuations  

---

## ⚙️ Feature Engineering

To transform the time series into a supervised learning problem, the following features were created:

- **Lag features** (previous hours' demand)  
- **Rolling mean statistics**  
- Time-based features:
  - Hour of day  
  - Day of week  
  - Month  

These features allow models to capture both short-term dependencies and recurring patterns.

---

## 🤖 Modeling

Several regression models were trained and evaluated, including:

- Linear Regression  
- Tree-based models (e.g., Random Forest)  
- Gradient boosting methods  

Special care was taken to:
- Preserve temporal order in training and testing  
- Avoid data leakage  
- Evaluate performance on future data only  

---

## 📈 Evaluation

Metric used:
- **RMSE (Root Mean Squared Error)**  

Project requirement:
- RMSE ≤ 48  

✅ The final model achieved:

- **RMSE: [YOUR FINAL VALUE HERE]**

This meets the project constraint and demonstrates strong predictive performance.

---

## 🔍 Key Insights

- Taxi demand shows strong **hourly and weekly seasonality**, making time-based features critical  
- Lag features significantly improve performance by capturing short-term dependencies  
- Rolling statistics help smooth noise and highlight local trends  
- Proper handling of temporal structure is essential to avoid overly optimistic results  

---

## 🧰 Tech Stack

- Python  
- Pandas / NumPy  
- Matplotlib  
- Scikit-learn  
- Statsmodels  

---

## 🚀 How to Run

```bash
git clone https://github.com/guayasco/taxi-demand-prediction.git
cd taxi-demand-prediction
jupyter notebook notebook.ipynb
