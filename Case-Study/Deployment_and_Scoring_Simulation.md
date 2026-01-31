# Deployment and Churn Scoring Simulation

## Phase 11: From Model to Business Use

### 11.1 Churn Scoring Output
The model outputs a churn probability score for each customer, which is translated into risk categories (Low, Medium, High) to support business decisions.

---

### 11.2 Scoring Schedule
Churn scoring is recommended on a monthly basis for all active customers, with more frequent scoring for new customers during their early lifecycle.

---

### 11.3 Risk Thresholds
Customers are categorized based on churn probability:
- High Risk: ≥ 0.70
- Medium Risk: 0.40 – 0.69
- Low Risk: < 0.40

These thresholds can be adjusted based on operational capacity and business priorities.

---

### 11.4 Operational Workflow
Model outputs feed into retention workflows where targeted actions are triggered based on customer risk level. Outcomes are tracked to measure effectiveness and inform model updates.

---

### 11.5 Business Integration
The churn model functions as a decision-support system embedded within marketing, customer success, and revenue operations.

