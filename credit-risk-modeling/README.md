# 🏦 Retail Credit Risk Modeling & Strategy Optimization

**Predicting loan default probability and optimizing credit origination strategy using Python and Machine Learning**

---

## 📘 Project Overview

This project develops a **machine learning–based credit risk model** to predict the probability of loan default for retail borrowers.  
Beyond predictive modeling, it focuses on **portfolio analysis and strategy optimization**, offering **data-driven recommendations** for credit origination and risk-based pricing.

> 🧩 Models Used: Random Forest, XGBoost  
> 📊 Dataset: [Give Me Some Credit (Kaggle)](https://www.kaggle.com/c/GiveMeSomeCredit)  
> 🧠 Objective: Improve default prediction accuracy and enhance lending strategy decisions  

---

## 🚀 Key Features

- **Data Preparation:** Cleaned and imputed missing financial data (income, dependents).  
- **Feature Engineering:** Derived financial ratios and behavioral indicators (`income_per_debt`, `total_past_due`).  
- **Model Development:** Built Random Forest and XGBoost classifiers for credit risk scoring.  
- **Portfolio Analysis:** Simulated approval rate vs default tradeoffs across risk thresholds.  
- **Business Strategy Insights:** Identified high-risk borrower segments and recommended threshold adjustments.  
- **Visual Analytics:** Interactive risk distribution and ROC curve visualization.

---
## 📊 Workflow
1. Load & Explore Data
- Read the Give Me Some Credit dataset.
- Perform EDA to identify key risk drivers (age, DTI, delinquency history).

2. Feature Engineering
Derived features to capture borrower risk behavior:
- income_per_debt
- total_past_due
- risk_score

3. Model Development
- Train-test split (70/30 stratified)
- Models:
  - Random Forest for interpretability and robustness
  - XGBoost for performance and feature importance analysis
- Metrics: AUC, ROC Curve, Confusion Matrix

4. Portfolio & Strategy Optimization
- Use predicted probabilities to segment customers by risk.
- Simulate approval thresholds to balance approval rate and default rate.
- Visualize Approval Rate vs. Portfolio Default Rate to guide credit policy.

---

## 💡 Business Impact

| Metric | Result |
|--------|---------|
| AUC (XGBoost) | **0.86** |
| Portfolio default reduction | ↓ 4% |
| Strategy outcome | Improved risk segmentation & portfolio profitability |
