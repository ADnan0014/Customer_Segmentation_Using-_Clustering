# Customer Segmentation using Clustering

## Project Overview

The objective of this project is to segment customers based on their purchasing behavior using RFM (Recency, Frequency, Monetary Value) analysis and clustering algorithms. Customer segmentation enables businesses to develop targeted marketing strategies, personalized campaigns, and improve customer retention.

**Key Goals:**

* Understand customer purchasing behavior.
* Group customers into meaningful segments.
* Provide actionable recommendations for marketing strategies.

---

## Dataset

**Mock Transaction Data** was generated for 500 customers and 5000 transactions.

**Columns:**

| Column          | Description                   |
| --------------- | ----------------------------- |
| TransactionID   | Unique transaction identifier |
| CustomerID      | Unique customer identifier    |
| TransactionDate | Date of transaction           |
| ProductID       | Purchased product identifier  |
| Quantity        | Number of items purchased     |
| UnitPrice       | Price per item                |
| TotalPrice      | Quantity × UnitPrice          |

**Sample Data Preview:**

| TransactionID | CustomerID | TransactionDate | ProductID | Quantity | UnitPrice | TotalPrice |
| ------------- | ---------- | --------------- | --------- | -------- | --------- | ---------- |
| TRX50000_0    | CUST1302   | 2022-01-12      | Prod_107  | 3        | 53.74     | 161.22     |
| TRX50001_1    | CUST1267   | 2023-10-17      | Prod_109  | 3        | 312.02    | 936.06     |

---

## Project Steps

### 1. Data Loading & Preparation

* Loaded mock customer transaction data.
* Checked for missing values and data types.
* Created `TotalPrice` column and converted `TransactionDate` to datetime format.
* Detected outliers using boxplots.

### 2. RFM Analysis

* Calculated **Recency**: Days since last purchase.
* Calculated **Frequency**: Number of transactions per customer.
* Calculated **Monetary Value**: Total spend per customer.
* Aggregated metrics at customer level to form the RFM table.

**Snapshot Date Used:** 2023-12-31

**Sample RFM Table:**

| CustomerID | Recency | Frequency | MonetaryValue |
| ---------- | ------- | --------- | ------------- |
| CUST1000   | 9       | 41        | 6855.79       |
| CUST1001   | 49      | 10        | 2856.43       |

---

### 3. Exploratory Data Analysis (EDA)

* Plotted distributions of RFM features.
* Applied **log transformation** to reduce skewness.
* Standardized features using **StandardScaler** for clustering.

---

### 4. Customer Segmentation (Clustering)

* Applied **K-Means clustering**.
* Used **Elbow Method** and **Silhouette Score** to determine optimal number of clusters (k=4).
* Clusters assigned to customers and analyzed.

**Clusters Identified:**

| Cluster | Segment Name         |
| ------- | -------------------- |
| 0       | At-Risk Low Spenders |
| 1       | Loyal High Spenders  |
| 2       | Potential Loyalists  |
| 3       | New Customers        |

---

### 5. Segment Profiling

Analyzed average RFM values per cluster:

| Cluster | Recency | Frequency | MonetaryValue | CustomerCount |
| ------- | ------- | --------- | ------------- | ------------- |
| 1       | 79.35   | 35.96     | 9347.92       | 213           |
| 2       | 8.02    | 31.29     | 6638.69       | 95            |
| 3       | 116.14  | 17.24     | 3625.30       | 96            |
| 0       | 71.28   | 29.75     | 1768.45       | 96            |

* **Loyal High Spenders**: High frequency & monetary value, moderate recency.
* **Potential Loyalists**: Recent buyers with good spend, possible growth segment.
* **New Customers**: Low frequency, moderate spend, high recency.
* **At-Risk Low Spenders**: Low engagement and spend, potential churn risk.

---

### 6. Visualization

* Distribution plots for Recency, Frequency, Monetary Value.
* Pairplot for RFM features by segment.
* 2D PCA projection of clusters for visualization.

---

### 7. Recommendations

* **Reward loyal customers** with exclusive offers and loyalty programs.
* **Re-engage at-risk customers** with targeted campaigns.
* **Nurture potential loyalists** to increase spending.
* **Guide new customers** with onboarding campaigns and promotions.

---

### 8. Deliverables

1. **Jupyter Notebook**: Contains all code for data preprocessing, RFM calculation, EDA, clustering, and segment profiling.
2. **CSV File**: `customer_segments.csv` with `CustomerID` and assigned `Segment`.
3. **PowerPoint Report**: `Customer_Segmentation_Report.pptx` summarizing methodology, clusters, visualizations, and recommendations.

---

### 9. Tools & Libraries

* Python 3.x
* Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `python-pptx`
* Clustering: K-Means
* Feature Scaling: StandardScaler
* Dimensionality Reduction: PCA

---

### 10. Estimated Time Allocation

| Task                                       | Hours |
| ------------------------------------------ | ----- |
| Data Understanding & RFM Calculation       | 10    |
| EDA & Feature Scaling                      | 8     |
| Clustering Algorithm Selection & Execution | 12    |
| Segment Profiling & Interpretation         | 6     |
| Documentation & Presentation               | 4     |
| **Total**                                  | 40    |

---

### Conclusion

This project successfully segmented customers into meaningful clusters using RFM analysis and K-Means clustering. The segments provide actionable insights for targeted marketing campaigns, helping businesses maximize revenue and customer retention.


Do you want me to generate it as a **`README.md` file with all tables and formatting ready**?
