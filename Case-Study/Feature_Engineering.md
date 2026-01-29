# Phase 6 — Feature Engineering & ML Preparation

## Objective
The goal of this phase was to transform the cleaned dataset into a fully
numeric, leakage-free, machine-learning-ready feature set suitable for
predicting customer churn.

---

## Target Variable Definition

The churn prediction task was framed as a binary classification problem:

- Stayed → 0
- Churned → 1
- Joined customers were excluded to prevent lifecycle bias

This mirrors real-world churn modeling where predictions are made for
active customers only.

---

## Feature Pruning

The following features were removed:

- customer_id (identifier)
- churn_reason (post-churn information)
- churn_category (post-churn information)
- city and zip_code (high cardinality, noisy)

Geographic information was preserved using latitude and longitude.

---

## Encoding Strategy

### Binary Encoding (0/1)
Applied to:
- gender
- marital status
- service subscriptions
- billing preferences

Binary encoding was chosen to avoid unnecessary feature expansion.

---

### One-Hot Encoding
Applied to low-cardinality categorical variables:
- contract
- payment_method
- internet_type
- offer

Dummy variables were created with `drop_first=True` to prevent
multicollinearity.

---

### Ordinal Encoding
Applied to ordered features:
- tenure_bucket
- age_group

Ordinal mappings preserved the natural order of customer lifecycle and
age progression.

---

## Final Dataset

- Rows: 6,589
- Features: 44
- All features numeric (int64 / float64)
- No missing values
- No leakage

The dataset is now suitable for supervised machine learning models.
