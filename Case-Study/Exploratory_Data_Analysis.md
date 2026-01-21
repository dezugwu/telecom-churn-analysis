# PHASE 5 — Exploratory Data Analysis (EDA)

## 1. Objective of EDA

The purpose of this phase was to explore the cleaned telecom customer dataset to:

- understand churn behavior and customer lifecycle patterns
- identify key drivers of customer churn
- generate business insights for retention strategies
- inform feature engineering and predictive modeling decisions

EDA bridges the gap between data preparation and machine learning by transforming raw variables into **interpretable business signals**.

---

## 2. Target Variable Overview

### Customer Status Distribution

The dataset contains three customer states:

- **Stayed** ≈ 67%
- **Churned** ≈ 26%
- **Joined** ≈ 6%

This distribution shows that churn is **significant but not overly imbalanced**, making the dataset suitable for both descriptive analysis and supervised machine learning classification.

---

## 3. Churn by Contract Type

### Key Findings

| Contract Type | Churn Rate |
|--------------|-----------|
| Month-to-Month | ~46% |
| One Year | ~11% |
| Two Year | ~3% |

### Interpretation

Contract length is one of the **strongest churn predictors**:

- Month-to-month customers are highly volatile
- Longer contracts dramatically reduce churn
- Two-year contracts show near-lock-in behavior

### Business Insight

Telecom providers reduce churn by:

- migrating customers to longer-term contracts
- offering contract renewal incentives
- bundling contracts with discounts and add-on services

---

## 4. Churn by Payment Method

### Key Findings

| Payment Method | Churn Rate |
|---------------|-----------|
| Credit Card | ~14% |
| Bank Withdrawal | ~34% |
| Mailed Check | ~37% |

### Interpretation

Customers using **automatic payment methods** churn significantly less than those using manual payment methods.

### Business Insight

- Autopay increases customer commitment
- Paper billing customers are easier to lose
- Many telcos actively incentivize autopay adoption

---

## 5. Churn by Internet Type

### Key Findings

| Internet Type | Churn Rate |
|--------------|-----------|
| Fiber Optic | ~41% |
| Cable | ~26% |
| DSL | ~19% |
| None | ~7% |

### Interpretation

Fiber customers exhibit the **highest churn**, despite being high-value customers.

This reflects:
- high price sensitivity
- competitive market dynamics
- performance-driven switching behavior

### Business Insight

Fiber users require:
- proactive retention offers
- contract incentives
- bundle strategies to reduce churn

---

## 6. Impact of Value-Added Services (Add-ons)

### Security, Backup, Protection, Tech Support

Customers subscribed to:
- **Online Security**
- **Premium Tech Support**
- **Device Protection Plans**

show **30–50% lower churn** compared to customers without these services.

### Streaming Services

Streaming add-ons (TV, Movies, Music) show:
- slightly higher churn
- association with fiber users
- younger, more competitive customer segments

### Business Insight

Two clear segments emerge:

**Low-Churn Segment**
- security & support subscribers
- longer tenure
- higher dependency on services

**High-Churn Segment**
- streaming-heavy users
- fiber customers
- price-sensitive and competitive

---

## 7. Tenure Cohort Analysis

Tenure was bucketed into lifecycle stages:

| Tenure Bucket | Churn Rate |
|--------------|-----------|
| 0–3 months | ~57% |
| 4–12 months | ~39% |
| 13–24 months | ~29% |
| 25–48 months | ~20% |
| 49–72 months | ~9% |

### Interpretation

- The **first 3 months** represent the highest churn risk (onboarding failure)
- Churn decreases steadily with tenure
- Long-tenure customers are highly loyal

### Business Insight

Retention strategies should be **lifecycle-specific**:
- onboarding support for new customers
- bundle and contract upgrades for mid-tenure users
- loyalty rewards for long-term customers

---

## 8. Pricing and Revenue Analysis

### Monthly Charges

| Status | Avg Monthly Charge |
|------|-------------------|
| Churned | ~$73 |
| Stayed | ~$62 |
| Joined | ~$43 |

Churned customers pay significantly more than retained customers.

### Total Revenue

| Status | Avg Total Revenue |
|------|------------------|
| Stayed | ~$3,736 |
| Churned | ~$1,971 |
| Joined | ~$120 |

### Interpretation

- High monthly pricing increases churn risk
- Retained customers generate nearly **2× more lifetime revenue**
- Retention is more profitable than acquisition

---

## 9. Visual Confirmation

A boxplot of **monthly charge vs customer status** confirms:

- churned customers cluster at higher price points
- joined customers enter at low promotional prices
- stayed customers show wider tolerance and value perception

---

## 10. Summary of Key Churn Drivers

The strongest churn drivers identified are:

- short contract duration
- higher monthly charges
- fiber internet usage
- lack of value-added services
- short tenure (early lifecycle)
- manual payment methods

Conversely, churn is reduced by:

- long-term contracts
- autopay methods
- security & support add-ons
- longer tenure
- bundled services

---

## 11. Relevance for Predictive Modeling

Insights from EDA directly inform feature engineering:

- Contract type, tenure, monthly charge → core predictors
- Add-on services → retention signals
- Payment method → behavioral commitment indicator
- Internet type → competitive pressure proxy

These features will be encoded and used in **Phase 6–7** to build a churn prediction model that identifies customers at risk **before they churn**.

---

## 12. Next Phase

Proceed to:

> **PHASE 6 — Feature Engineering & Encoding**

Where categorical variables will be encoded, churn labels prepared, and the dataset structured for supervised machine learning.
