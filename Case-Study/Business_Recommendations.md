# Business Recommendations — Customer Churn Reduction

## Phase 9: Translating Insights into Action

### 9.1 High-Risk Customer Segments

Based on exploratory data analysis and machine learning models (Logistic Regression, Decision Tree, Random Forest), the following customer segments were identified as having the highest churn risk:

#### 1. Short-Tenure Customers (0–12 Months)
Customers in their first year exhibit the highest churn probability. Tenure-related features consistently ranked as the most important predictors across all models.

**Business implication:** Early customer lifecycle is critical for retention.

---

#### 2. Month-to-Month Contract Customers
Month-to-month contracts show significantly higher churn compared to one-year and two-year contracts.

**Business implication:** Contract flexibility increases churn risk.

---

#### 3. High Monthly Charge Customers
Customers with higher monthly charges are more likely to churn, indicating strong price sensitivity.

**Business implication:** Perceived value may not justify cost for some customers.

---

#### 4. Fiber Optic Internet Customers
Fiber optic users demonstrate higher churn rates compared to DSL or non-internet customers.

**Business implication:** Premium service users may have higher service expectations.

---

#### 5. Low Engagement Customers
Customers with low engagement—measured by fewer referrals and lack of add-on services—are more likely to churn.

**Business implication:** Engagement and service bundling reduce churn risk.

### 9.2 Early-Warning Churn Signals

To enable proactive retention, the following early-warning churn signals were identified based on model behavior and exploratory analysis:

#### 1. Tenure Below 12 Months
Customers with tenure under 12 months show the highest churn probability.

**Trigger:** tenure_in_months < 12

---

#### 2. Month-to-Month Contract
Customers on month-to-month contracts exhibit significantly higher churn risk.

**Trigger:** contract = "Month-to-Month"

---

#### 3. High Monthly Charges Without Added Services
Customers paying high monthly charges without complementary add-on services are more price-sensitive.

**Trigger:** High monthly_charge AND no add-on services

---

#### 4. Low Customer Engagement
Customers with zero referrals and no additional services show weaker brand attachment.

**Trigger:** number_of_referrals = 0 AND add-ons = "No"

---

#### 5. Fiber Optic Customers With Low Engagement
Fiber optic customers with low engagement are at increased risk due to unmet service expectations.

**Trigger:** internet_type = "Fiber Optic" AND low engagement

---

### 9.3 Targeted Retention Strategies

Based on identified churn drivers and early-warning signals, the following targeted retention strategies are recommended:

#### 1. Early Lifecycle Retention Program
Customers within their first year should receive proactive onboarding support, service education, and temporary add-on incentives.

**Target:** tenure_in_months < 12

---

#### 2. Contract Migration Incentives
Encourage month-to-month customers to migrate to longer-term contracts through discounts and bundled offers.

**Target:** contract = "Month-to-Month"

---

#### 3. Price–Value Alignment Offers
Provide personalized pricing adjustments or plan optimization for customers with high monthly charges but low engagement.

**Target:** High monthly_charge AND low engagement

---

#### 4. Engagement and Loyalty Boosting
Increase customer attachment through referral incentives and bundled service promotions.

**Target:** number_of_referrals = 0 AND no add-ons

---

#### 5. Premium Experience for Fiber Optic Customers
Deliver enhanced service quality and proactive support for premium internet customers.

**Target:** internet_type = "Fiber Optic"

---

### 9.4 Action Prioritization (Impact vs Effort)

To guide execution, recommended retention strategies were prioritized based on expected business impact and implementation effort:

#### High Impact / Low Effort
- Targeted discounts for high-risk customers
- Contract upgrade incentives
- Early lifecycle engagement campaigns

---

#### High Impact / High Effort
- Premium support and proactive monitoring for Fiber Optic customers
- Personalized retention workflows

---

#### Low Impact / Low Effort
- Referral reward programs
- Add-on upsell promotions

---

#### Low Impact / High Effort
- Large-scale pricing restructuring
- Major infrastructure upgrades

These initiatives should be phased to maximize return on investment while minimizing operational risk.

---

### 9.5 Operationalizing the Churn Model

To ensure business impact, the churn model should be embedded into regular business operations:

#### Regular Churn Scoring
The model should be run on a weekly or monthly basis to assign churn risk probabilities to active customers.

---

#### Risk-Based Segmentation
Customers should be segmented into high, medium, and low churn risk groups to guide targeted interventions.

---

#### Action Assignment
Each risk segment should trigger predefined retention actions such as discounts, service outreach, or engagement campaigns.

---

#### Performance Monitoring
Churn rates, campaign effectiveness, and revenue retention should be continuously tracked to evaluate impact.

---

#### Model Governance
The model should be periodically retrained and monitored for performance drift and fairness.

---

### 9.6 Business Recommendations Summary

This project demonstrates that customer churn is predictable and preventable when behavioral, pricing, and engagement data are effectively leveraged.

Key findings show that churn is most prevalent among short-tenure customers, month-to-month contract holders, and customers with high monthly charges and low engagement.

To address this, the business should prioritize early lifecycle retention, contract migration incentives, pricing alignment, and engagement-focused interventions. Embedding the churn model into regular operations enables proactive retention and more efficient allocation of resources.

Overall, the recommended approach supports churn reduction, revenue protection, and long-term customer value creation.
