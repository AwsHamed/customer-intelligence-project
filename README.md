# 🛍️ Customer Intelligence & Response Prediction System

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-green.svg)
![XGBoost](https://img.shields.io/badge/XGBoost-1.5+-orange.svg)
![LightGBM](https://img.shields.io/badge/LightGBM-3.0+-red.svg)

## 📋 Project Overview

This project is a comprehensive customer intelligence system that combines **unsupervised learning** (customer segmentation) and **supervised learning** (campaign response prediction) to help businesses optimize their marketing strategies.

The system analyzes customer data to:
- **Segment customers** into distinct groups based on purchasing behavior and demographics
- **Predict campaign responses** to identify which customers are most likely to engage with marketing campaigns
- **Provide actionable insights** for personalized marketing strategies

---

## 🎯 Key Features

### Customer Segmentation (Unsupervised Learning)
- **PCA (Principal Component Analysis)**: Reduces 30+ features to 12 principal components while preserving 81.14% of variance
- **K-Means Clustering**: Identifies 2 distinct customer segments:
  - **Elite Spenders**: High-income, high-spending customers
  - **Frugal Youngsters**: Younger, budget-conscious customers

### Response Prediction (Supervised Learning)
Three powerful ensemble models for predicting campaign response:

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| **LightGBM** | **88.62%** | **69.05%** | **43.28%** | **53.21%** |
| XGBoost | 87.28% | 62.50% | 37.31% | 46.73% |
| AdaBoost | 86.38% | 57.89% | 32.84% | 41.90% |

**🏆 LightGBM** outperforms other models with the highest accuracy (88.62%) and F1-Score (53.21%).

---

## 📊 Dataset

The dataset contains **2,240 customer records** with **29 features** covering:

### Customer Demographics
- `Year_Birth`: Customer birth year
- `Education`: Education level (Graduation, PhD, etc.)
- `Marital_Status`: Marital status (Single, Married, Together, etc.)
- `Income`: Annual income
- `Kidhome`: Number of children at home
- `Teenhome`: Number of teenagers at home

### Purchase Behavior
- `MntWines`, `MntFruits`, `MntMeatProducts`: Spending by product category
- `NumDealsPurchases`: Number of purchases made with discounts
- `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`: Purchase channel preferences
- `Total_Spendings`: Total spending across all categories

### Campaign History
- `AcceptedCmp1-5`: Response to previous marketing campaigns (0/1)
- `Complain`: Whether customer complained (0/1)
- `Response`: Target variable - responded to latest campaign (0/1)

**Note**: `Income` had 24 missing values which were imputed with the mean.

---

## 🏗️ Project Architecture
