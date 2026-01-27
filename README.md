# Credit Card Customer Segmentation Using K-Means

## Overview
This project implements an unsupervised machine learning pipeline to segment credit card customers based on financial and behavioral patterns. The system groups users into distinct segments using K-Means clustering and visualizes the results in an interactive 3D analytics dashboard.

## Business Problem
Financial institutions need to better understand customer spending behavior to improve marketing effectiveness, optimize credit risk strategies, and design personalized financial products. Manual segmentation is inefficient at scale, making machine learning-driven clustering essential for data-driven decision-making.

## Dataset
The dataset contains anonymized credit card customer information, including balance amounts, purchasing behavior, credit limits, and payment patterns.

**Source:** CC GENERAL Dataset  
**Records:** ~9,000 customers  
**Format:** CSV

## Features Used
- BALANCE  
- PURCHASES  
- CREDIT_LIMIT  

These features capture core customer financial behavior for segmentation.

## Methodology
1. Data loading and inspection  
2. Missing value handling  
3. Feature scaling using MinMaxScaler  
4. K-Means clustering (k = 5)  
5. Customer segment labeling  
6. 3D visualization of clusters using Plotly  

## Results
The model identifies five distinct customer segments representing different financial behavior patterns such as high-value users, moderate spenders, and low-engagement customers. These insights can support targeted campaigns and portfolio optimization strategies.


