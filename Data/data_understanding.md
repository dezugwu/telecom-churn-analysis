# Data Understanding — Telecom Churn Dataset

## 1. Dataset Overview

- Dataset origin: Kaggle
- Business domain: Telecom Customer Churn
- Geographic scope: California, USA
- Time reference: Q2 2022
- Unit of analysis: Customer

---

## 2. Raw Field Inventory

| Field | Description | Type (Initial Guess) |
|---|---|---|
| CustomerID | Unique customer identifier | categorical |
| Gender | Customer gender | categorical |
| Age | Age in years | numeric |
| Married | Customer marital status | categorical |
| Number of Dependents | Household dependents | numeric |
| City | Customer city of residence | categorical |
| Zip Code | Postal zip code | categorical |
| Latitude | Latitude of residence | numeric |
| Longitude | Longitude of residence | numeric |
| Number of Referrals | Number of referrals made | numeric |
| Tenure in Months | Total months with company | numeric |
| Offer | Last marketing offer accepted | categorical |
| Phone Service | Subscribes to phone service | categorical |
| Avg Monthly Long Distance Charges | Avg long distance usage charges | numeric |
| Multiple Lines | Multi-line phone service | categorical |
| Internet Service | Subscribes to internet service | categorical |
| Internet Type | Internet connection type | categorical |
| Avg Monthly GB Download | Avg monthly data usage | numeric |
| Online Security | Internet security addon | categorical |
| Online Backup | Backup service addon | categorical |
| Device Protection Plan | Device protection addon | categorical |
| Premium Tech Support | Premium support addon | categorical |
| Streaming TV | Uses internet to stream TV | categorical |
| Streaming Movies | Uses internet to stream movies | categorical |
| Streaming Music | Uses internet to stream music | categorical |
| Unlimited Data | Has unlimited data plan | categorical |
| Contract | Contract type | categorical |
| Paperless Billing | Uses paperless billing | categorical |
| Payment Method | Billing payment method | categorical |
| Monthly Charge | Current monthly charge | numeric |
| Total Charges | Accumulated charges | numeric |
| Total Refunds | Total refunded amount | numeric |
| Total Extra Data Charges | Extra data charges | numeric |
| Total Long Distance Charges | Extra long distance charges | numeric |
| Total Revenue | Total revenue from customer | numeric |
| Customer Status | Final status (Churned/Stayed/Joined) | categorical |
| Churn Category | High-level churn reason | categorical |
| Churn Reason | Specific churn reason | categorical |

---

## 3. Target Definition (Churn)

- Target field: `Customer Status`
- Churn definition:
  - `Churned` → customer has churned
  - `Stayed` → customer retained
  - `Joined` → new customer acquisition
