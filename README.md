# Customer Churn Prediction – End-to-End ML Project
## Project Overview

Customer churn prediction is essential for subscription-based businesses like telecom and SaaS. Retaining existing customers is much more cost-effective than acquiring new ones.

This project implements a complete ML pipeline to predict customer churn, including:

1. Data Cleaning & Preprocessing

2. Exploratory Data Analysis (EDA)

3. Feature Engineering

4. Model Training & Hyperparameter Tuning

## Data Cleaning & Preprocessing

1. Converted TotalCharges to numeric and handled missing values

2. Encoded categorical variables using one-hot encoding

3. Handled class imbalance using class_weight and boosting weights

4. Created dataset versions with and without TotalCharges to evaluate impact

5. Scaled numeric features where necessary

### Key Insight: Small preprocessing changes (like TotalCharges) affect model performance significantly.

## Exploratory Data Analysis (EDA)

1. Identified class imbalance (26% churn)

2. Observed higher churn for month-to-month contracts and fiber optic users

3. Churn correlates with higher monthly charges

4. Correlation heatmap showed TotalCharges depends strongly on tenure and monthly charges

# Models Implemented
## Logistic Regression
1. Interpretable baseline
2. High Recall (0.861) → best for catching most churners

## Random Forest

1. Non-linear modeling capability

2. Balanced performance across all metrics

## XGBoost

1. Gradient boosting, excellent for tabular data

2. Best F1 Score (0.640) & ROC-AUC (0.848)

## LightGBM

1. Fast and efficient boosting

2. Best Accuracy (0.781) & Precision (0.571)

# Final Report

| Model               | Accuracy  | Precision | Recall    | F1 Score  | ROC-AUC   | Best At              |
| ------------------- | --------- | --------- | --------- | --------- | --------- | -------------------- |
| Logistic Regression | 0.705     | 0.470     | **0.861** | 0.608     | 0.838     | Recall               |
| Random Forest       | 0.771     | 0.550     | 0.754     | 0.636     | 0.844     | Balanced             |
| XGBoost             | 0.777     | 0.560     | 0.746     | **0.640** | **0.848** | F1 & ROC             |
| LightGBM            | **0.781** | **0.571** | 0.709     | 0.632     | 0.826     | Accuracy & Precision |

## Choosing the Right Model

1. Maximize Recall → Logistic Regression (catch more churners)

2. Maximize Precision → LightGBM (reduce unnecessary outreach)

3. Balanced F1 / Ranking → XGBoost (best overall performance)

## Key Takeaways

1. Accuracy alone is insufficient for churn prediction.

2. Class imbalance impacts evaluation metrics heavily.

3. Boosting models (XGBoost & LightGBM) excel in structured/tabular datasets.

4. Business goals dictate the best model choice.
