<div align="center">

# 🚀 Customer Churn Prediction
### End-to-End Machine Learning Project for Customer Retention

<p align="center">
  <img src="https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" />
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/EDA-Data%20Analysis-0A66C2?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Machine%20Learning-Churn%20Prediction-FF4B4B?style=for-the-badge" />
</p>

<p align="center">
  <b>Predicting customer churn using preprocessing, feature engineering, and multiple ML models</b>
</p>

</div>

---

## 📌 Project Overview

Customer churn prediction is a critical problem for subscription-based businesses such as telecom and SaaS platforms. Retaining existing customers is often far more cost-effective than acquiring new ones.

This project builds a complete machine learning pipeline to identify customers who are likely to churn and helps support better retention strategies.

---

## 🎯 Objectives

- Clean and preprocess raw customer data
- Perform exploratory data analysis (EDA)
- Engineer meaningful features
- Train and evaluate multiple machine learning models
- Compare models based on business-driven metrics

---

## 🧠 ML Pipeline

| Stage | Description |
|-------|-------------|
| Data Cleaning | Converted `TotalCharges` to numeric and handled missing values |
| Encoding | Applied one-hot encoding to categorical features |
| Imbalance Handling | Managed class imbalance using `class_weight` and boosting weights |
| Feature Variants | Built datasets with and without `TotalCharges` to study impact |
| Scaling | Scaled numerical features where needed |
| Modeling | Trained Logistic Regression, Random Forest, XGBoost, and LightGBM |
| Evaluation | Compared models using Accuracy, Precision, Recall, F1 Score, and ROC-AUC |

---

## 🧹 Data Cleaning & Preprocessing

### Steps Performed

- Converted `TotalCharges` to numeric format and handled missing values
- Encoded categorical variables using one-hot encoding
- Addressed class imbalance using weighted learning techniques
- Created multiple dataset variants to evaluate feature impact
- Scaled numeric features wherever required

> ### 🔍 Key Insight
> Even a small preprocessing decision, such as whether to include `TotalCharges`, can significantly influence model performance.

---

## 📊 Exploratory Data Analysis

### Major Findings

- Around **26% of customers** belong to the churn class
- Customers with **month-to-month contracts** showed higher churn
- **Fiber optic users** were more likely to churn
- Higher churn was associated with **higher monthly charges**
- Correlation analysis showed that `TotalCharges` strongly depends on `tenure` and `MonthlyCharges`

---

## 🤖 Models Implemented

### 1. Logistic Regression
- Strong interpretable baseline
- Best suited when **high recall** is the priority
- Achieved **Recall = 0.861**

### 2. Random Forest
- Captures non-linear relationships effectively
- Delivered balanced performance across metrics

### 3. XGBoost
- Powerful gradient boosting model for structured/tabular data
- Achieved the **best F1 Score (0.640)** and **best ROC-AUC (0.848)**

### 4. LightGBM
- Efficient and fast boosting framework
- Achieved the **best Accuracy (0.781)** and **best Precision (0.571)**

---

## 📈 Final Model Performance

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC | Best At |
|------|----------|-----------|--------|----------|---------|---------|
| Logistic Regression | 0.705 | 0.470 | **0.861** | 0.608 | 0.838 | Recall |
| Random Forest | 0.771 | 0.550 | 0.754 | 0.636 | 0.844 | Balanced Performance |
| XGBoost | 0.777 | 0.560 | 0.746 | **0.640** | **0.848** | F1 Score & ROC Ranking |
| LightGBM | **0.781** | **0.571** | 0.709 | 0.632 | 0.826 | Accuracy & Precision |

---

## ✅ Choosing the Right Model

| Business Goal | Recommended Model | Why |
|--------------|-------------------|-----|
| Catch maximum churners | Logistic Regression | Highest recall |
| Reduce unnecessary retention outreach | LightGBM | Highest precision |
| Best overall balance | XGBoost | Best F1 score and ROC-AUC |

---

## 📌 Key Takeaways

- Accuracy alone is not enough for churn prediction
- Class imbalance strongly affects evaluation metrics
- Boosting models perform especially well on structured/tabular datasets
- The best model depends on the actual business objective

---

## 🛠️ Tech Stack

<p>
  <img src="https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54" />
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/ML-Classification-blueviolet?style=flat-square" />
  <img src="https://img.shields.io/badge/EDA-Visualization-orange?style=flat-square" />
</p>

---

## 📂 Project Workflow

```text
Raw Data
   ↓
Data Cleaning
   ↓
EDA
   ↓
Feature Engineering
   ↓
Model Training
   ↓
Hyperparameter Tuning
   ↓
Evaluation & Model Selection
```

---

## 🌟 Business Impact

By identifying customers who are likely to churn, businesses can:

- Run targeted retention campaigns
- Reduce customer acquisition costs
- Improve long-term customer lifetime value
- Make data-driven retention decisions

---

## 📬 Conclusion

This project demonstrates a complete end-to-end churn prediction workflow, from raw data preprocessing to model selection. It also highlights how model choice should align with business goals such as maximizing recall, improving precision, or balancing performance.
