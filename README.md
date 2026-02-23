# Project Overview

The goal of this project is to understand customer behavior and predict churn in order to support data-driven decisions for customer retention and prioritization.
Starting from raw transactional data, the analysis builds a customer-level view (Customer 360) and uses it to identify customers at risk of churn, estimate their value, and segment the customer base for targeted business actions.
The final outputs are designed to be directly usable for business purposes, such as retention campaigns, customer prioritization and strategic CRM decisions.

---

## Project Goals

- Build a Customer 360 view to summarize customer behavior at individual level
- Identify patterns and signals associated with customer churn
- Predict which customers are more likely to churn using classification models
- Rank customers by churn risk to support prioritization actions
- Estimate Customer Lifetime Value (CLV) to combine risk and value perspectives
- Use RFM segmentation to support marketing and CRM strategies
- Provide business-oriented insights to guide retention and customer management decisions

---

## Project Structure
```
customer-churn-analytics/
├── data/
│   ├── raw/
│   │   └── online_retail_raw.xlsx                 # Original transactional dataset
│   ├── processed/
│   │   └── customer_360_snapshot_2011-09-01.xlsx  # Customer-level aggregated snapshot dataset
│   └── outputs/
│       └── churn_analysis_output.xlsx             # Final outputs (scores, segments, CLV, etc.)
├── notebooks/
│   └── churn.ipynb                                # End-to-end analysis notebook
├── README.md
└── requirements.txt
```
---

## Methodology

The analysis follows an end-to-end data science workflow:

1. **Data understanding and cleaning**
   - Load raw transactional data
   - Handle missing values, outliers and inconsistencies
   - Prepare data for customer-level aggregation

2. **Feature engineering (Customer 360)**
   - Build customer-level features such as:
     - Recency, Frequency, Monetary (RFM)
     - Behavioral indicators
     - Returns and other transactional patterns
   - Create a structured dataset suitable for modeling

3. **Modeling**
   - Train classification models for churn prediction:
     - Logistic Regression (baseline)
     - XGBoost
   - Split data into training and test sets
   - Tune and compare models

4. **Model evaluation**
   - Evaluate performance using:
     - AUC
     - Precision / Recall
     - Recall@K
   - Compare models from both a technical and business perspective

5. **Scoring and business outputs**
   - Generate **churn scores** for customers
   - Rank customers by churn risk
   - Estimate **Customer Lifetime Value (CLV)**
   - Perform **RFM segmentation**
   - Interpret results with a business-oriented perspective
  
  ---

  ## Conclusion

This project shows how customer-level analytics can be used to understand different customer profiles and support decision-making on churn management. By combining churn prediction, CLV and segmentation, the analysis helps identify which customers to prioritize and which actions to take.
