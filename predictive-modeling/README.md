# Predictive Modeling for Business Strategy

This project demonstrates how predictive analytics and machine learning can be used to drive strategic business decisions.  
Using real-world customer data, the project builds, compares, and interprets multiple predictive models to identify the key factors influencing business outcomes such as customer churn.

---

## 🎯 Project Objectives
- Develop and compare machine learning models (Logistic Regression, Random Forest, XGBoost) to predict business outcomes.
- Engineer and analyze features to improve both predictive accuracy and interpretability.
- Use SQL for data extraction and Pandas for data transformation.
- Translate model insights into actionable business strategies.

---

## 🧠 Dataset

**Source:** [Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/blastchar/telco-customer-churn)

Each record represents a customer’s demographics, contract details, and billing information, along with whether they churned (left the company).

| Column Example | Description |
|----------------|-------------|
| `tenure` | Number of months the customer has stayed |
| `Contract` | Type of contract (Month-to-month, One year, etc.) |
| `MonthlyCharges` | The amount charged per month |
| `Churn` | Target variable — whether the customer left |

---

## ⚙️ Methodology

### 1️⃣ Data Preparation
- Loaded and cleaned raw data using Pandas.
- Handled missing values and converted categorical variables with one-hot encoding.
- Standardized numerical features with `StandardScaler`.

### 2️⃣ Feature Engineering
- Created new variables for customer behavior patterns.
- Performed correlation and importance analysis to identify key predictors.

### 3️⃣ Model Development
Three models were developed and compared:

| Model | Library | Description |
|--------|----------|-------------|
| Logistic Regression | scikit-learn | Baseline linear model |
| Random Forest | scikit-learn | Nonlinear ensemble method |
| XGBoost | xgboost | Gradient boosting with feature importance analysis |

### 4️⃣ Model Evaluation
Performance was assessed on AUC (Area Under ROC Curve):

| Model | AUC Score |
|--------|------------|
| Logistic Regression | 0.84 |
| Random Forest | 0.82 |
| XGBoost | 0.82 |

---

## 📊 Visualization Examples

**SHAP Summary Plot (Model Explainability):**
```python
shap.summary_plot(shap_values, X_test)

