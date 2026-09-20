# Customer Behavior Analysis — Alfido Tech

**Task 1 of 3 — Alfido Tech Data Analytics Internship Program**

## Overview
Analysis of 250,000 e-commerce transactions from 49,673 customers (Jan 2020 – Sep 2023) to segment customers, understand purchase patterns, and assess churn risk, with actionable recommendations for Alfido Tech.

**Dataset:** [Customer Behavior Analysis](https://www.kaggle.com/datasets/bhanupratapbiswas/customer-behavior-analysis) (Kaggle) — `ecommerce_customer_data_custom_ratios.csv`

## Files in this repo
| File | Description |
|---|---|
| `Customer_Behavior_Analysis.ipynb` | Full Jupyter notebook — data cleaning, feature engineering, RFM segmentation, K-Means clustering, visualizations, and churn analysis (executed, all outputs included) |
| `Customer_Behavior_Analysis_Report.pdf` | Detailed 9-page analytical report — methodology, segment profiles, findings, and recommendations |
| `Task1_Submission_Summary.pdf` | 1-page submission summary — executive summary, key findings, top recommendations, key charts, and notebook screenshots |

## Approach
1. **Data cleaning** — removed a duplicate column, handled missing values, checked for duplicate/invalid rows, flagged a data quality quirk in the `Total Purchase Amount` field.
2. **Feature engineering** — aggregated transactions into customer-level RFM features (Recency, Frequency, Monetary, tenure, return rate).
3. **Segmentation** — RFM rule-based scoring into 7 segments, cross-validated with K-Means clustering.
4. **Visualization** — purchase trends, category/payment mix, segment profiles, retention trends.
5. **Churn analysis** — tested the dataset's pre-labeled `Churn` field for behavioral signal (found none) and used RFM/recency as a practical churn-risk proxy instead.

## Key Findings
- Revenue is flat (~$15M/month) with no growth trend across 3.5+ years.
- **Champions** + **Loyal Customers** (37.6% of customers) generate **52.5%** of total revenue.
- A large **Lost** segment (18.8% of customers) has gone quiet (~580 days inactive) but still represents 8.9% of historical revenue.
- Clothing and Books drive the most orders; Electronics and Home earn more revenue per order.
- The provided `Churn` label shows no behavioral correlation — recency/RFM segment is used as the practical churn-risk indicator.

## Top 5 Recommendations
1. Win back "At Risk (High Value)" and "Lost" segments with targeted offers.
2. Build a loyalty/VIP program for Champions and Loyal Customers.
3. Convert "New/Promising" customers into repeat buyers via a structured onboarding flow.
4. Cross-sell Electronics/Home to high-frequency Clothing/Books buyers.
5. Instrument a real, time-based churn definition (e.g., 90+ days inactive) for future tracking.

---
*Prepared as part of the Alfido Tech Data Analytics Internship Program.*
