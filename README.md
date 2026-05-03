# 🚗 Egyptian Used Car Price Prediction

A machine learning project that predicts the prices of used cars in Egypt using real market data, featuring full data preprocessing, statistical analysis, and multiple ML models.


---

## 📌 Project Overview

The Egyptian used car market is large and complex, making it hard to determine a fair price for a car. This project builds a prediction model using real car ads data from Kaggle to help estimate used car prices based on features like brand, year, mileage, engine size, and more.

---

## 📊 Dataset

- **Source:** Kaggle — Egyptian Car Ads Dataset
- **Features include:** Brand, Model, Year, Kilometers, Engine Capacity, Fuel Type, Body Type, Transmission Type, Price (EGP)

---

## 🔧 Project Pipeline

### 1. 📥 Data Loading
- Loaded dataset using Pandas

### 2. 🧹 Data Cleaning
- Cleaned Price and Kilometers columns (removed symbols, converted to float)
- Dropped rows with missing critical values (Brand, Kilometers, Model)
- Filled missing Engine Capacity using group median
- Filled missing Model using group mode

### 3. 📉 Outlier Removal
- Applied IQR method on Price, Kilometers, and Engine Capacity
- Filtered car years between 1970 and 2026

### 4. ⚙️ Feature Engineering
- Created **KM_Category** (Brand New / Low / Medium / High / Very High Mileage)
- Created **Engine Size Category** (Very Small / Small / Medium / Large)
- Calculated **Car_Age** from manufacturing year

### 5. 🔢 Encoding & Scaling
- Applied One-Hot Encoding on categorical features
- Applied StandardScaler for Linear Regression

### 6. ✂️ Train/Test Split
- 80% Training / 20% Testing
- Log transformation on target variable (Price) to reduce skewness

---

## 🤖 Models Used

| Model | Description |
|---|---|
| **Linear Regression** | Baseline model with feature scaling |
| **Decision Tree** | Non-linear model with depth control |
| **Random Forest** | Ensemble of 200 trees with cross-validation |
| **XGBoost** | Gradient boosting with 300 estimators |

---

## 📈 Model Evaluation Metrics

- **MAE** — Mean Absolute Error
- **MSE** — Mean Squared Error
- **RMSE** — Root Mean Squared Error
- **R²** — R-Squared Score
- **Cross Validation** — Applied on Random Forest

---

## 📊 Statistical Analysis

- **Price Distribution** — Analyzed skewness and applied log transformation
- **Brand vs Price** — Median price per brand
- **Transmission vs Price** — Average price by transmission type
- **T-Test** — Automatic vs Manual transmission prices
- **ANOVA** — Fuel type effect on prices
- **T-Test** — New cars (≤5 years) vs Old cars prices
- **Cohen's D** — Effect size between Automatic and Manual prices

---

## 📉 EDA Visualizations

- Price Distribution (Histogram + KDE)
- Price vs Year (Scatter Plot)
- Price vs Kilometers (Scatter Plot)
- Body Type Distribution (Count Plot)
- Top 10 Brands (Bar Chart)
- Price Box Plot
- Feature Importance (Random Forest)

---

## 🛠️ Tech Stack

| Tool | Usage |
|---|---|
| **Python** | Programming Language |
| **Pandas** | Data Manipulation |
| **NumPy** | Numerical Operations |
| **Matplotlib & Seaborn** | Data Visualization |
| **Scikit-learn** | ML Models & Preprocessing |
| **XGBoost** | Gradient Boosting Model |
| **SciPy** | Statistical Testing |
| **Jupyter Notebook** | Development Environment |

---

## 📁 Project Structure

```
├── project_Data_Science.ipynb   # Main Jupyter Notebook
├── car_ads_details_kaggle.csv   # Dataset
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the repo
```bash
git clone https://github.com/AbdElazizYasser2/Egyptian-Used-Car-Price-Prediction.git
cd Egyptian-Used-Car-Price-Prediction
```

### 2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost scipy jupyter
```

### 3. Run the notebook
```bash
jupyter notebook project_Data_Science.ipynb
```

---
