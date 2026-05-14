# Customer Segmentation using RFM Analysis and K‑Means Clustering

## 📌 Project Title
Customer Segmentation using RFM Analysis and K‑Means Clustering

## 🛒 Business Problem
The company wants to better understand customer behavior to design targeted marketing strategies. By segmenting customers into meaningful groups, the business can increase loyalty, re‑engage inactive buyers, and maximize revenue.

## 📂 Dataset Source
- **Name:** Online Retail dataset  
- **Origin:** UCI Machine Learning Repository  
- **Accessed via:** [Google Drive Link](https://drive.google.com/file/d/1QRMxOkrzez3TEO9SweRq1nfRN_joF6Z7/view?usp=sharing)

## 📑 Dataset Description
- **Period:** 2010–2011  
- **Size:** ~500,000 rows  
- **Columns:** InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country  
- **Granularity:** Each row represents a single product in an invoice  

## 🛠️ Tools and Libraries Used
- Python (Google Colab)  
- pandas, numpy → data cleaning & feature engineering  
- matplotlib, seaborn → visualizations  
- scikit‑learn → K‑Means clustering  
- gdown → dataset download  

## 🔎 Steps Performed
1. Data Understanding  
2. Data Cleaning  
3. Feature Engineering (RFM table)  
4. Exploratory Data Analysis (EDA)  
5. Customer Segmentation using K‑Means  
6. Cluster Interpretation  
7. Business Recommendations  

## 🧹 Data Cleaning Summary
- Removed cancelled invoices and negative quantities  
- Dropped missing CustomerIDs and product descriptions  
- Removed duplicates  
- Created a new `Revenue` column = Quantity × UnitPrice  

## 🏗️ Feature Engineering Summary
Built RFM table:  
- Recency = days since last purchase  
- Frequency = number of purchases  
- Monetary = total revenue per customer  

## 📊 EDA Insights
- UK dominates sales revenue  
- A few products generate most revenue, while everyday items dominate sales volume  
- Most customers purchase only a few times; a small group buys frequently  
- Outliers exist in Quantity and UnitPrice (bulk orders, data entry errors)  
- A small set of customers contribute disproportionately to revenue  

## 🤖 Clustering Approach
- Standardized RFM features using StandardScaler  
- Applied Elbow Method to determine optimal clusters (k=4)  
- Used K‑Means to segment customers  
- Visualized clusters with scatter plots (Frequency vs Monetary)  

## 🧩 Cluster Interpretation
- **Cluster 0 – High Value Loyal:** Frequent, high‑spending, recent buyers  
- **Cluster 1 – Inactive / At‑Risk:** Long recency, low frequency, low spend  
- **Cluster 2 – Frequent Low‑Spend Buyers:** Buy often but spend little  
- **Cluster 3 – Occasional Buyers:** Purchase occasionally, moderate spend  

## 💡 Final Business Recommendations
- **High Value Loyal:** VIP loyalty programs, exclusive launches, thank‑you campaigns  
- **Inactive / At‑Risk:** Reactivation discounts, win‑back emails, trending product highlights  
- **Frequent Low‑Spend Buyers:** Bundle deals, cross‑selling, tiered discounts  
- **Occasional Buyers:** Seasonal promotions, free shipping vouchers, personalized suggestions  

## ▶️ How to Run the Project
Clone the repository and install requirements:

```bash
git clone https://github.com/Gurkamal-kaur/business-project-part-1.git
cd business-project-part-1
pip install -r requirements.txt
