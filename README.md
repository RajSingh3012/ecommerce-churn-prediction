# E-Commerce Customer Segmentation & Churn Prediction

## 📌 Executive Summary
The goal of this project was to analyze over 100,000 e-commerce transactions to identify distinct customer purchasing behaviors and predict future customer churn. By combining unsupervised clustering (K-Means) with supervised machine learning (Random Forest), this pipeline transforms raw transaction logs into actionable business intelligence.

## 🏗️ Data Architecture & Methodology
1. **Data Engineering (ETL):** Cleaned and aggregated raw transaction data into an RFM (Recency, Frequency, Monetary) matrix using Pandas.
2. **Feature Scaling:** Applied `StandardScaler` to normalize distributions for machine learning algorithms.
3. **Customer Segmentation:** Deployed an unsupervised **K-Means Clustering** model to group customers into 4 distinct profiles.
4. **Predictive Analytics:** Engineered a **Random Forest Classifier** to predict customer churn, validated via 5-Fold Cross-Validation.

## 📊 Key Business Insights
Through K-Means clustering, the customer base was segmented into four actionable groups:
* **Segment 0 (Recent Buyers):** High potential for second purchase.
* **Segment 1 (Lost/Churned):** Highest recency (437+ days); dormant accounts.
* **Segment 2 (VIPs / Whales):** Smallest group but highest monetary value (~$1,197 average spend).
* **Segment 3 (Loyalists):** Highest purchase frequency; steady recurring revenue.

### Churn Prediction Performance
* The Random Forest model successfully predicted customer churn with a **cross-validated accuracy of 70.8%**.
* **Feature Importance Analysis** revealed that *Monetary Value* and *Average Order Value* were the strongest predictors of churn, while *Frequency* had negligible impact due to the high volume of single-purchase users in the dataset.

## 💻 Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (K-Means, Random Forest)
* **Visualization:** Plotly, Matplotlib
