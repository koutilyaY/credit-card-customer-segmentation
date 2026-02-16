# Credit Card Customer Segmentation Engine  
**Unsupervised Machine Learning | Business Intelligence | 3D Analytics Dashboard**

## Overview
This project implements an end-to-end customer segmentation pipeline for credit card users using unsupervised machine learning. It clusters customers into meaningful behavioral segments based on financial activity and visualizes the results through an interactive 3D analytics dashboard. The system is designed to support data-driven decision-making in marketing, risk management, and customer strategy teams.

## Business Problem
Financial institutions manage millions of customers with diverse spending and credit usage patterns. Traditional rule-based segmentation fails to scale and adapt to evolving customer behavior. This project addresses that challenge by using machine learning to automatically discover behavioral groups, enabling:
- Targeted marketing and personalized offers  
- Identification of high-value and low-engagement customers  
- Portfolio optimization and credit strategy support  
- Customer retention and lifecycle management  

## Dataset
**CC GENERAL Dataset**  
The dataset contains anonymized credit card customer records with behavioral and financial attributes such as balances, purchases, credit limits, payment history, and tenure.

- Format: CSV  
- Records: ~9,000 customers  
- Granularity: One row per customer  

## Feature Engineering
Clustering is performed using the following core financial behavior features:
- `BALANCE` – Average outstanding balance  
- `PURCHASES` – Total purchase amount  
- `CREDIT_LIMIT` – Assigned credit limit  

Additional features are used for post-clustering business profiling:
- `PAYMENTS`  
- `TENURE`  

## 📊 Customer Segmentation ML Pipeline Architecture

```
Customer Data Sources
 (CSV / Database / API)
          |
          ▼
 Data Ingestion & Inspection
          |
          ▼
 Data Cleaning Pipeline
 (Missing Value Handling)
          |
          ▼
 Feature Engineering
 (MinMax Normalization)
          |
          ▼
 Cluster Optimization Engine
 (Elbow + Silhouette Analysis)
          |
          ▼
 ML Training Layer
 (K-Means Segmentation)
          |
          ▼
 Business Intelligence Layer
 (Segment Profiling + Auto Naming)
          |
          ▼
 Visualization Layer
 (Interactive 3D Dashboard)
          |
          ▼
 Production Artifacts
 (Saved Model + Scaler)
```

## Machine Learning Approach
- Algorithm: K-Means Clustering  
- Learning Type: Unsupervised Learning  
- Validation Techniques:
  - Elbow Method (WCSS optimization)
  - Silhouette Score (cluster separation quality)

The final model assigns each customer to a behavioral segment based on similarity in financial activity patterns.

## Output
- Customer-level segment labels  
- Business-readable segment summary table  
- Executive summary report (customer distribution by segment)  
- Interactive 3D visualization dashboard  
- Serialized model and scaler for deployment  


