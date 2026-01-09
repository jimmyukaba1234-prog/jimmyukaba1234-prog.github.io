---
layout: default
title: E-Commerce End-to-End Data Analytics Platform
permalink: /projects/E-Commerce End-to-End Data Analytics Platform/
---

# Customer Churn Prediction
**Problem:** Despite consistent transaction data, the business lacked clarity on why customers churn, which products and regions drive profit, and where operational inefficiencies were hurting growth.
**Solution:**Built a full end-to-end analytics platform combining data engineering, analytics, dashboards, and predictive models to deliver actionable business insights and support data-driven decision-making.
## Approach1. **Designed a relational database and integrated large-scale historical data
2. **EDA:** Built an automated ETL pipeline to extract, clean, transform, and load analytics ready tables
3. **Analysis** Analyzed customer behavior, churn patterns, regional performance, product profitability, and operational bottlenecks
4. **Visualization** Created interactive dashboards covering churn, revenue trends, fulfillment efficiency, and payment failures
5. **Modeling:** Built a customer churn model using RFM features (recency as a key driver) and Developed a customer lifetime value (LTV) model to identify high-value customers
6. **Deployment and Automation:** Built a web app allowing users to upload a database and instantly access dashboards and insights and Automated generation of stakeholder-ready PDF reports
## Results
- Identified a “leaky bucket” retention pattern driving customer churn
- Revealed declining sales and profit trends over time
- Highlighted operational inefficiencies in delivery and payments
- Showed that a small group of high-value customers generates most future revenue
- Enabled early churn detection and smarter prioritization through churn & LTV models

## Code Highlights
```python# Data cleaning example
if "customers" in dataframes:
            print("Cleaning customers table")

            df = dataframes["customers"].copy()

            # customer_id
            df["customer_id"] = df["customer_id"].astype(str).str.strip()
            df["customer_id"] = df["customer_id"].replace(["", "nan", "None", "NULL", "<NA>"], np.nan)
            df["customer_id"] = df["customer_id"].fillna("Unknown")
