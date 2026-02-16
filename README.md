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

flowchart LR
  %% ======================
  %% Customer Segmentation — Architecture & Workflow
  %% ======================

  subgraph S1[Data Intake]
    A[1. Data ingestion & inspection<br/>(CSV / DB / API)] --> B[2. Missing value handling<br/>& data cleaning]
  end

  subgraph S2[Feature Engineering]
    B --> C[3. Feature scaling<br/>(MinMax normalization)]
  end

  subgraph S3[Modeling]
    C --> D[4. Optimal cluster selection<br/>(Elbow + Silhouette)]
    D --> E[5. K-Means training<br/>& customer segmentation]
  end

  subgraph S4[Business Layer]
    E --> F[6. Segment profiling<br/>& automated segment naming]
  end

  subgraph S5[Analytics & Delivery]
    F --> G[7. Interactive 3D visualization<br/>(dashboard)]
    F --> H[8. Persist model & scaler<br/>(production-ready artifacts)]
  end

  H --> I[Deployment / Reuse<br/>(batch scoring or API)]
  I -. feedback loop .-> A



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


