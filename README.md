
# 🎬 OTT Subscription Customer Churn Analytics

An end-to-end Python & SQL churn analysis pipeline built on 1,000+ subscriber records. This project integrates relational database querying (SQLite), feature engineering, exploratory data analysis (EDA), and data visualizations to quantify churn risk and highlight actionable retention strategies for subscription-based OTT platforms.

---

## 📌 Executive Summary & Key Metrics

* **Overall Churn Rate:** **32.42%** (67.58% Retention Rate across 1,021 subscribers)
* **Average Revenue Per User (ARPU):** **$59.58 / month**
* **Average Customer Tenure:** **471 days** (~15.7 months)
* **Total Revenue at Risk (Churn Loss):** **$19,523.70**
* **Support Escalation Rate:** **11.07%** of overall customer interactions

---

## 📊 Key Findings & Business Insights

### 1. Subscription Plan Dynamics
* **Basic Tier:** Highest churn rate at **33.77%** (302 users, generating $8,935.70 revenue).
* **Standard Tier:** Represents the largest subscriber base with 495 users ($29,658.10 revenue) and a **31.92%** churn rate.
* **Premium Tier:** Highest ARPU subscriber group with 224 users ($22,236.00 revenue) and the lowest churn rate at **31.70%**.

### 2. Geographic Segmentation
* **High-Risk Regions:** **Karnataka (40.00%)**, **Delhi (36.59%)**, and **Meghalaya (35.04%)** show the highest cancellation rates.
* **Low-Risk Regions:** **Uttar Pradesh (23.14%)** and **Rajasthan (28.69%)** demonstrate stronger long-term retention.

### 3. Customer Service Impact & Escalations
* Average support ticket density is **0.37 complaints per user**.
* Escalations show a slightly negative linear correlation (**-0.0576**) with churn, indicating that direct support resolutions help stabilize high-risk accounts.

---

## 🛠️ Tech Stack & Methodology

* **Database & Querying:** SQLite3 (Schema setup, table joins across customer demographics, subscriptions, and support complaints)
* **Data Wrangling:** Pandas, NumPy (Date transformations, standardization, missing value handling, duplicate handling)
* **Feature Engineering:**
  * `churn_flag` (Binary indicator for cancellation date presence)
  * `tenure_days` (Calculated duration from subscription start to cancellation/current date)
  * `churn_risk` (Segmented into Low, Medium, and High based on predictive churn scoring)
  * `escalations_binary` (Numerical mapping for correlation testing)
* **Data Visualization:** Matplotlib, Seaborn

---

## 📂 Repository Structure

```text
├── Monthly_cancellation_trends.png
├── churn_by_plan_types_gender_accross_risk_factors.png
├── churn_rate_by_plan_type.png
├── churn_rate_by_state.png
├── churn_risk_factor_and_corelations.png
├── churn_anlysis.ipynb
├── exported_churn_data.csv
└── README.md
