# Customer Churn Prediction — Telecom Analytics Case Study

## 📌 Executive Summary
This project presents an end-to-end customer churn analysis and prediction system using telecom customer data. The objective was to identify key drivers of churn, predict customers at risk of leaving, and translate analytical insights into actionable business strategies for customer retention.

The project covers the full analytics lifecycle — from raw data ingestion and cleaning, through exploratory analysis and feature engineering, to machine learning model development and evaluation.

The final solution delivers a production-ready churn prediction model with strong recall and clear business interpretability.

---

## 🎯 Key Outcomes
- Identified early-tenure, month-to-month customers as the highest churn risk segment
- Built and evaluated multiple ML models (Logistic Regression, Decision Tree, Random Forest)
- Selected Random Forest as the final model based on recall, ROC-AUC, and stability
- Translated model insights into actionable retention strategies

---

## 🏢 Business Problem
Customer churn is a major revenue challenge in the telecom industry. Acquiring new customers is significantly more expensive than retaining existing ones.  

The business goal of this project is to:
- Identify customers at high risk of churning
- Understand *why* customers churn
- Enable proactive retention strategies

---

## 📊 Data Overview
- Source: Public telecom customer dataset (Kaggle)
- Records: ~7,000 customers
- Features include:
  - Customer demographics
  - Contract and billing information
  - Service subscriptions
  - Usage behavior
  - Churn status and reasons

---

## 🔍 Analytical Approach
The project followed a structured analytics workflow:

1. **Data Understanding & Profiling**
2. **Data Cleaning & Validation**
3. **Exploratory Data Analysis (EDA)**
4. **Feature Engineering**
5. **Model Development**
   - Logistic Regression (baseline)
   - Decision Tree (explainability)
   - Random Forest (final model)
6. **Model Evaluation & Selection**
7. **Business Interpretation & Documentation**

---

## 🧠 Key Insights
- Customers in their first year are at the highest risk of churn
- Month-to-month contracts significantly increase churn probability
- Long-term contracts strongly reduce churn
- High monthly charges increase churn risk
- Customer engagement indicators (e.g., referrals, add-on services) reduce churn

## 📊 Key Visual Insights

### Churn Distribution
![Churn Distribution](Images/churn_distribution.png)

### Random Forest Model Performance
![Random Forest Confusion Matrix](Images/rf_confusion_matrix.png)

### Key Churn Drivers
![Random Forest Feature Importance](Images/rf_feature_importance.png)

---

## 🤖 Modeling Summary
| Model | Purpose | Outcome |
|-----|--------|--------|
| Logistic Regression | Baseline & interpretability | High recall |
| Decision Tree | Rule extraction | Clear churn rules |
| Random Forest | Final model | Best balance of performance |

Random Forest was selected as the final model due to its strong balance between churn recall, predictive robustness, and ability to capture non-linear customer behavior.


**Final Model Selected:** Random Forest  
- ROC-AUC ≈ 0.92  
- Strong recall for churn detection  
- Robust and production-ready

---

## 📈 Business Impact
The final model enables:
- Early identification of high-risk customers
- Targeted retention campaigns
- Contract upgrade strategies
- Revenue loss reduction through proactive intervention

---

## 📁 Repository Structure
```text
Telco-Churn-Analysis/
│
├── Case-Study/          # Business & analytical documentation
├── Data/
│   ├── Raw/             # Original datasets
│   └── Processed/       # Cleaned data
├── Notebooks/           # Analysis and modeling notebooks
├── PowerBI/             # (Optional) Dashboard files
└── README.md

---

## 🗣️ How to Talk About This Project
When discussing this project in interviews or portfolio reviews, focus on:

- Designing and executing a full end-to-end churn analytics pipeline
- Handling real-world messy telecom data from ingestion to modeling
- Balancing predictive performance with business interpretability
- Comparing multiple models and justifying final model selection
- Translating machine learning outputs into actionable retention strategies

---

## 🔮 Future Enhancements
Potential improvements and extensions include:

- Churn probability threshold tuning for cost-sensitive decisions
- Retention cost vs revenue impact optimization
- Deployment of churn scoring for new customers
- Model monitoring and periodic retraining
- Interactive Power BI dashboard for executive stakeholders

---

## 👤 Author
**Ezugwu Desmond**  
Data Analyst | Telecom Analytics | Predictive Modeling  
Open to Remote & Global Opportunities


[def]: Images/rf_confusion_matrix.png