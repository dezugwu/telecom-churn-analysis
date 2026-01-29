# Final Model Selection — Customer Churn Prediction

## 1. Objective
The objective of this section is to evaluate and compare multiple machine learning models developed for customer churn prediction and to justify the selection of a final model for business deployment.

Models were assessed based on predictive performance, stability, interpretability, and alignment with business objectives.

---

## 2. Models Evaluated
The following models were developed and evaluated:

1. **Logistic Regression**
2. **Decision Tree Classifier**
3. **Random Forest Classifier**

Each model was trained on the same feature set and evaluated on a stratified test dataset.

---

## 3. Evaluation Metrics
The following metrics were used to compare model performance:

- **Recall (Churn Class)** — ability to correctly identify churners  
- **Precision (Churn Class)** — accuracy of churn predictions  
- **F1-Score** — balance between precision and recall  
- **ROC-AUC** — overall ranking performance  
- **Model Interpretability** — ease of explaining predictions to stakeholders  

---

## 4. Model Performance Comparison

| Model | Recall (Churn) | Precision | F1-Score | ROC-AUC | Interpretability |
|-----|---------------|-----------|----------|--------|------------------|
| Logistic Regression | 0.85 | 0.63 | 0.72 | 0.918 | Medium |
| Decision Tree | 0.74 | 0.70 | 0.72 | 0.896 | High |
| **Random Forest** | **0.82** | **0.68** | **0.74** | **0.918** | Medium |

---

## 5. Final Model Selection
After evaluating all models, **Random Forest** was selected as the final model for churn prediction.

### Justification:
- Strong recall performance for identifying churners
- High ROC-AUC indicating excellent ranking ability
- Better generalization compared to single decision trees
- Ability to capture non-linear relationships and feature interactions
- Stable performance across multiple churn drivers

While Logistic Regression provided slightly higher recall, Random Forest offered a better balance between recall, precision, and robustness.

---

## 6. Key Drivers Identified by the Final Model
The Random Forest model consistently identified the following features as the most influential churn drivers:

- Customer tenure (months and tenure buckets)
- Contract duration (Two-Year and One-Year contracts)
- Number of referrals
- Monthly charges and total revenue
- Internet type (Fiber Optic)

These findings align with earlier exploratory analysis and model interpretations, reinforcing confidence in the model’s reliability.

---

## 7. Business Implications
The final model enables the business to:

- Proactively identify high-risk churn customers
- Target retention campaigns during early customer tenure
- Promote long-term contracts to reduce churn
- Incentivize referral behavior to improve loyalty
- Apply pricing interventions for high-risk segments

---

## 8. Limitations & Future Improvements
- Model performance may vary over time as customer behavior evolves
- Threshold tuning could further optimize cost-sensitive decisions
- Incorporating customer interaction or support data may improve predictions
- Periodic retraining is recommended to maintain accuracy

---

## 9. Conclusion
The Random Forest model provides a reliable and scalable solution for customer churn prediction. It balances predictive performance with practical interpretability, making it suitable for real-world deployment and strategic decision-making.

This concludes the modeling phase of the customer churn analytics project.
