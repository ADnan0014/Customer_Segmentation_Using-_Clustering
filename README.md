# Customer Churn Prediction

## Project Overview

This project focuses on predicting **customer churn** for a telecom company using advanced data analysis and machine learning techniques. The objective is to proactively identify customers likely to leave, allowing the company to implement retention strategies and reduce revenue loss.

The project covers the full pipeline from **data exploration** and **feature engineering** to **model building, evaluation**, and **customer segmentation**.

---

## Objective

* Develop a predictive model to identify customers likely to churn.
* Understand the key drivers of churn using RFM and clustering analysis.
* Provide actionable business insights for customer retention strategies.

---

## Dataset

A mock telecom customer dataset was generated for this project with the following attributes:

* **CustomerID** – Unique customer identifier
* **Demographics:** Gender, SeniorCitizen, Partner, Dependents
* **Account Information:** Tenure, Contract, PaymentMethod, PaperlessBilling
* **Services:** PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies
* **Billing:** MonthlyCharges, TotalCharges
* **Target Variable:** Churn (Yes/No)

Dataset contains **2000 simulated customer records** with realistic distributions of churn behavior.

---

## Tools & Libraries

* **Python**: pandas, numpy, matplotlib, seaborn, scikit-learn
* **Machine Learning**: Logistic Regression, Random Forest, Gradient Boosting, KMeans Clustering
* **Data Visualization**: matplotlib, seaborn
* **Presentation**: python-pptx (PowerPoint report)

---

## Steps / Methodology

### 1. Data Exploration and Cleaning

* Loaded and inspected the dataset.
* Checked for missing values and handled inconsistencies (`No internet service`, `No phone service`).
* Performed basic descriptive statistics and outlier detection.

### 2. Feature Engineering

* Created additional features such as **tenure in years**, **average monthly charges**, and **total spend**.
* Encoded categorical variables for model training.

### 3. RFM Analysis & Customer Segmentation

* Calculated **Recency, Frequency, Monetary (RFM)** metrics for each customer.
* Applied **log transformation** and **standard scaling** to normalize RFM values.
* Used **KMeans clustering** to identify 4 distinct customer segments:

  1. Loyal High Spenders
  2. At-Risk Low Spenders
  3. Potential Loyalists
  4. New Customers
* Visualized clusters using **PCA 2D projections**.

### 4. Model Building & Training

* Split dataset into **training** and **testing** sets.
* Trained multiple classifiers:

  * Logistic Regression
  * Random Forest
  * Gradient Boosting
* Performed **hyperparameter tuning** for optimal performance.

### 5. Model Evaluation

* Evaluated models using:

  * Accuracy
  * Precision
  * Recall
  * F1-Score
  * ROC-AUC
* Identified **key drivers of churn** using feature importance from the best model.

### 6. Reporting & Presentation

* Saved segmented customer data as `customer_segments.csv`.
* Prepared a **PowerPoint report** summarizing:

  * RFM analysis
  * Clustering results
  * Model performance
  * Actionable recommendations for business

---

## Results

### RFM Segments

| Segment              | Recency | Frequency | Monetary Value | Customer Count |
| -------------------- | ------- | --------- | -------------- | -------------- |
| Loyal High Spenders  | 79.35   | 35.96     | 9347.92        | 213            |
| Potential Loyalists  | 8.02    | 31.29     | 6638.69        | 95             |
| New Customers        | 116.14  | 17.24     | 3625.30        | 96             |
| At-Risk Low Spenders | 71.28   | 29.75     | 1768.45        | 96             |

### Key Insights

* **High spenders with recent activity** are the most loyal.
* **Customers with low engagement and low monetary value** are at risk of churn.
* Targeted campaigns for **at-risk and new customers** can improve retention.

### Deliverables

* **Jupyter Notebook** with full code and analysis.
* **Trained predictive models** (`.pkl` files).
* **PowerPoint presentation** summarizing findings: `/content/Customer_Segmentation_Report.pptx`.
* **Segmented customer CSV**: `customer_segments.csv`.

---

## Recommendations

1. Reward **Loyal High Spenders** with exclusive offers and loyalty programs.
2. Launch **personalized campaigns** to reactivate **at-risk customers**.
3. Encourage **new customers** to upgrade services through targeted promotions.
4. Focus on improving **online security and tech support** as they influence churn.

---

## Project Duration

Estimated 40 hours:

| Task                                     | Hours |
| ---------------------------------------- | ----- |
| Data Understanding & EDA                 | 8     |
| Data Preprocessing & Feature Engineering | 10    |
| Model Building & Training                | 12    |
| Model Evaluation & Interpretation        | 6     |
| Documentation & Presentation             | 4     |

---
