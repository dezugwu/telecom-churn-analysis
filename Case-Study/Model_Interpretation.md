# Model Interpretation — Churn Drivers & Retention Insights

## 1. Objective
The objective of this section is to interpret the results of the baseline churn prediction model (Logistic Regression) and translate statistical outputs into clear business insights. The focus is on identifying key drivers of customer churn and factors that improve customer retention.

This interpretation supports data-driven decision-making for proactive churn prevention strategies.

---

## 2. Model Overview
- **Model Type:** Logistic Regression
- **Target Variable:** `churn_target`  
  - `1` = Churned  
  - `0` = Not Churned (Stayed)
- **Class Handling:** Balanced class weights
- **Feature Scaling:** StandardScaler applied to numeric features
- **Evaluation Metric Focus:** Recall (Churn class), ROC-AUC

---

## 3. How to Interpret Coefficients
Logistic Regression estimates the impact of each feature on the log-odds of churn.

- **Positive coefficient:** Increases likelihood of churn
- **Negative coefficient:** Reduces likelihood of churn
- **Odds Ratio > 1:** Feature increases churn risk
- **Odds Ratio < 1:** Feature reduces churn risk

The absolute magnitude of coefficients indicates relative importance.

---

## 4. Key Retention Drivers (Churn Reducers)

### 4.1 Customer Tenure
- **Feature:** `tenure_bucket_ord`
- **Odds Ratio:** ~0.19
- **Insight:** Customers with longer tenure are significantly less likely to churn.

**Business Interpretation:**  
Early customer lifecycle is the most vulnerable period for churn.

**Recommended Action:**  
Focus retention programs within the first 3–12 months of customer onboarding.

---

### 4.2 Customer Referrals
- **Feature:** `number_of_referrals`
- **Odds Ratio:** ~0.22
- **Insight:** Customers who refer others are much less likely to churn.

**Business Interpretation:**  
Referral behavior indicates strong engagement and loyalty.

**Recommended Action:**  
Strengthen referral incentive programs as both acquisition and retention strategies.

---

### 4.3 Contract Length
- **Features:**  
  - `contract_Two Year` (OR ≈ 0.29)  
  - `contract_One Year` (OR ≈ 0.56)

**Insight:**  
Longer contract durations dramatically reduce churn risk.

**Recommended Action:**  
Encourage upgrades from month-to-month contracts to longer-term commitments through incentives.

---

## 5. Key Churn Drivers (Risk Factors)

### 5.1 Monthly Charges
- **Feature:** `monthly_charge`
- **Odds Ratio:** ~1.82
- **Insight:** Higher monthly charges significantly increase churn risk.

**Business Interpretation:**  
Price sensitivity is a major contributor to customer churn.

**Recommended Action:**  
Introduce targeted discounts, bundles, or loyalty pricing for high-paying customers.

---

### 5.2 Demographic Signals
- **Features:** `married`, `age`
- **Odds Ratios:**  
  - Married ≈ 2.30  
  - Age ≈ 1.31

**Interpretation Note:**  
These variables act as behavioral proxies rather than causal factors.

**Business Interpretation:**  
Certain household and age groups may have higher service-switching tendencies.

**Recommended Action:**  
Design personalized retention offers rather than broad demographic targeting.

---

## 6. Add-On Services & Stickiness
Features such as:
- `online_security`
- `phone_service`
- `premium_tech_support`

showed negative coefficients, indicating reduced churn risk.

**Business Interpretation:**  
Value-added services increase customer stickiness and reduce churn probability.

**Recommended Action:**  
Bundle core services with high-retention add-ons during onboarding.

---

## 7. Model Limitations
While Logistic Regression provides interpretability, it has known limitations:

- Sensitive to multicollinearity (e.g., tenure vs tenure buckets)
- Assumes linear relationships
- Cannot naturally capture interaction effects

These limitations motivate the use of tree-based models in subsequent phases.

---

## 8. Summary of Key Insights
- Early tenure customers are the highest churn risk group
- Contract duration is the strongest retention lever
- Pricing and perceived value drive churn decisions
- Engagement indicators (referrals, add-ons) significantly reduce churn

---

## 9. Next Steps
To address non-linear relationships and capture decision rules:
- **Phase 7.3:** Decision Tree Model
- **Phase 7.4:** Random Forest Model

These models will improve predictive power and uncover actionable churn rules.
