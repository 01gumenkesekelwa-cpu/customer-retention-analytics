# Customer Retention Analytics

## Project Overview

Customer retention is one of the most important drivers of business growth. Acquiring a new customer is often more expensive than retaining an existing one, making customer retention analysis a valuable business function.

This project analyzes customer purchasing behaviour using the **Online Retail** dataset from the UCI Machine Learning Repository. The objective was to identify valuable customer segments, analyze churn behaviour, and build predictive models that can help businesses improve customer retention.

The project demonstrates an end-to-end data analytics workflow, from data cleaning and feature engineering in Python to customer segmentation, machine learning, and interactive Power BI dashboards.

---

## Business Problem

Businesses often struggle to answer questions such as:

- Which customers generate the most revenue?
- Which customers are at risk of leaving?
- Which customer groups should receive targeted marketing campaigns?
- Can customer behaviour be used to predict future churn?

This project addresses these questions using RFM (Recency, Frequency, Monetary) analysis and predictive analytics.

---

## Dataset

## Dataset Source

This project uses the **Online Retail** dataset from the **UCI Machine Learning Repository**.

**Dataset:** Online Retail

**Creator:** Daqing Chen, School of Engineering, London South Bank University

**Repository:** UCI Machine Learning Repository

**DOI:** https://doi.org/10.24432/C5BW33

**Dataset Link:** :contentReference[oaicite:0]{index=0}

Citation:

> Chen, D. (2015). *Online Retail* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33

- UCI Machine Learning Repository
- Online Retail Dataset

The dataset contains over 500,000 retail transactions from a UK-based online retailer.

Features include:

- Invoice Number
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- Power BI

---

## Project Workflow

### 1. Data Cleaning

The raw transaction data was cleaned by:

- Removing cancelled orders
- Removing negative quantities
- Removing invalid prices
- Handling missing Customer IDs
- Creating a TotalPrice feature

---

### 2. Feature Engineering

Customer-level features were created using RFM Analysis:

- **Recency** – Days since the customer's last purchase
- **Frequency** – Number of purchases
- **Monetary** – Total customer spending

Customers were then segmented into:

- Champion
- Loyal
- Potential Loyalist
- At Risk
- Lost

---

### 3. Churn Analysis

A churn indicator was created using customer recency.

Machine learning models were developed to predict customer churn using customer purchasing behaviour.

Models explored:

- Logistic Regression
- Random Forest Classifier

During model evaluation, target leakage was identified when Recency was used as both a feature and part of the target definition. The model was then re-evaluated using only independent features to obtain more realistic performance.

---

### 4. Power BI Dashboard

Interactive dashboards were created to communicate business insights.

Dashboard pages include:

- Executive Overview
- Customer Segmentation Analysis
- Customer Churn Analysis

These dashboards enable users to explore customer behaviour, revenue contribution, and churn patterns through interactive visualizations.

---

## Repository Structure

```
customer-retention-analytics/
│
├── dashboards/
│   └── Customer_Retention_Analytics.pbix
│
├── data/
│   ├── customer_segments.csv
│   └── retail_transactions_sample.csv
│
├── images/
│   ├── executive_dashboard.png
│   ├── customer_segmentation.png
│   └── churn_analysis.png
│
├── notebooks/
│   └── Customer_Retention_Analytics.ipynb
│
├── README.md
└── requirements.txt
```

---

## Dashboard Preview

### Executive Overview

<img width="878" height="496" alt="image" src="https://github.com/user-attachments/assets/bda85a47-a8bf-45cd-918d-c4e3b10b5857" />


---

### Customer Segmentation

<img width="882" height="494" alt="image" src="https://github.com/user-attachments/assets/88d4ba82-b90c-463c-80a3-0f3cb3db9611" />


---

### Customer Churn Analysis

<img width="884" height="492" alt="image" src="https://github.com/user-attachments/assets/d4a0dd40-90ca-4ee9-a39b-93dd25247213" />


---

## Key Business Insights

- Champion customers generated the highest revenue despite representing a smaller customer group.
- Lost customers exhibited low purchase frequency and low spending.
- Customer purchase frequency and spending behaviour provide useful indicators of customer retention.
- RFM segmentation enables businesses to target marketing campaigns more effectively.
- Understanding target leakage is critical when building predictive machine learning models.

---

## Future Improvements

Possible future enhancements include:

- Time-series forecasting
- Customer Lifetime Value (CLV) prediction
- Recommendation systems
- Hyperparameter tuning
- Deployment using Streamlit or Flask
- Cloud deployment on Azure or AWS

---

## Author

**Sekelwa Gumenke**

Postgraduate Diploma in Data Science | Mathematics Teacher | Aspiring Data Scientist

GitHub: https://github.com/01gumenkesekelwa-cpu

LinkedIn: www.linkedin.com/in/sekelwa-gumenke-323478171
