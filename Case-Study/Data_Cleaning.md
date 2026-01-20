# PHASE 4 — Data Cleaning & Validation

## 1. Purpose

The goal of this phase was to transform raw telecom customer data from Kaggle into a clean, consistent, analysis-ready dataset suitable for exploratory analytics and predictive modeling (customer churn risk).

This phase ensures:

- no missing values
- no semantic contradictions
- correct data types
- telecom domain business rules preserved
- no leakage from churn-related fields
- dataset reproducibility for modeling

---

## 2. Source Data Overview

Dataset contained **7,043 customer records** and **38 attributes** related to:

- demographic information
- product subscriptions (phone, internet, streaming)
- billing & payments
- revenue usage metrics
- churn status and churn reasons

---

## 3. Key Data Issues Identified

During profiling, multiple issues were observed:

### **3.1 Missingness (Structured)**
Several fields showed structured missingness, especially:

| Attribute | Missing Pattern |
|---|---|
| `offer` | many customers had no marketing offer |
| `internet_type` | missing mostly for non-internet subscribers |
| `online_security` & other add-ons | missing for non-internet subs |
| `avg_monthly_long_distance_charges` | missing for non-phone subs |
| `churn_reason` & `churn_category` | only applies to churned customers |

These patterns aligned with **business logic**, not accidental data loss.

---

## 4. Business Logic-Based Cleaning Decisions

Cleaning was guided by telecom service rules rather than generic imputation.

### **4.1 Offer Imputation**
Customers without an accepted offer were labeled:

offer = 'None'

This avoids implying missing marketing activity.

### **4.2 Internet Block Resolution**

If `internet_service = 'No'`, then:

| Field | Assigned Value |
|---|---|
| `internet_type` | `None` |
| `avg_monthly_gb_download` | `0` |
| add-on services (security, streaming, etc.) | `No` |

Rationale:
> non-subscribers cannot consume add-on internet features.

### **4.3 Phone Block Resolution**

If `phone_service = 'No'`, then:

| Field | Value |
|---|---|
| `avg_monthly_long_distance_charges` | `0` |
| `multiple_lines` | `No` |

Rationale:
> long-distance usage requires an active phone line.

### **4.4 Churn Labeling Logic**

If `customer_status != 'Churned'`, then:
churn_category = 'No Churn'
churn_reason = 'No Churn'

Ensures clean grouping for churn analytics.

---

## 5. Type Standardization

### **5.1 Column Renaming**
All columns converted to `snake_case` for modeling compatibility:

Example:
Total Charges → total_charges
Customer Status → customer_status


### **5.2 ZIP Code Correction**
Converted ZIP to string:

zip_code → dtype: object


Since ZIP codes are identifiers, not numeric measures.

### **5.3 ID Handling**
`customer_id` retained for traceability but will be dropped before ML to prevent leakage.

---

## 6. Validation Checks

### **6.1 Missingness Validation**

Final state:


Since ZIP codes are identifiers, not numeric measures.

### **5.3 ID Handling**
`customer_id` retained for traceability but will be dropped before ML to prevent leakage.

---

## 6. Validation Checks

### **6.1 Missingness Validation**

Final/Current state:

0 missing values across all 38 attributes


### **6.2 Revenue Arithmetic Verification**

Dataset stated:

total_revenue = total_charges
- total_refunds
+ total_extra_data_charges
+ total_long_distance_charges


Validation result:

np.float64(6.34e-10) ≈ 0

Rounding noise confirms equation consistency.

### **6.3 Lifecycle Consistency (Tenure)**

| Status | Mean Tenure |
|---|---|
| Joined | ~1.7 months |
| Churned | ~18 months |
| Stayed | ~41 months |

Matches telecom lifecycle expectations:

- **onboarding**
- **mid-life churn window**
- **loyal high-LTV customers**

### **6.4 Churn Reason Logic Check**

Non-churned customers contained:

['No Churn']


No leakage detected.

---

## 7. Final Dataset Status

After cleaning:

✔ 7,043 customers  
✔ 38 attributes preserved  
✔ zero missing values  
✔ type-consistent  
✔ business-consistent  
✔ audit-ready for ML

Dataset exported to:


No leakage detected.

---

## 7. Final Dataset Status

After cleaning:

✔ 7,043 customers  
✔ 38 attributes preserved  
✔ zero missing values  
✔ type-consistent  
✔ business-consistent  
✔ audit-ready for ML

Dataset exported to:

/Data/Processed/clean_telco.csv


---

## 8. Next Phase

Proceed to:

> **PHASE 5 — Exploratory Data Analysis (EDA)**

to understand churn drivers across:

- tenure
- pricing
- contract type
- payment method
- services bundle
- churn category

These insights will later feed into:

> **PHASE 7 — Predictive Modeling (Churn Prediction)**





