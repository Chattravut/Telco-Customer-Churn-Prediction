# 📞 Telco Customer Churn Prediction

## 📌 Project Overview
Customer retention is one of the key challenges in the telecommunication industry. This project aims to analyze customer behavior and build a Machine Learning model to **predict customer churn** (whether a customer will leave or stay).

By identifying at-risk customers early, businesses can proactively implement retention strategies, such as offering targeted promotions or contract modifications.

## 🛠 Tools & Technologies
* **Language:** Python 3.x
* **Data Manipulation:** Pandas, NumPy
* **Database Simulation:** SQLite, SQL
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn (Random Forest Classifier)

---

## 📊 Key Steps & Methodology

### 1. SQL Data Extraction
Instead of loading the CSV directly, I simulated a real-world scenario by importing the data into a **SQLite database**.
* Wrote **SQL queries** to filter high-value customers and specific contract types.
* Extracted the processed data into a Pandas DataFrame for analysis.

### 2. Exploratory Data Analysis (EDA)
Visualized the data to find patterns and correlations.
* **Insight 1:** Customers with **"Month-to-month" contracts** have a significantly higher churn rate compared to those with 1-year or 2-year contracts.
* **Insight 2:** There is a strong correlation between **High Monthly Charges** and Churn probability.
* **Insight 3:** New customers (low tenure) are the most vulnerable to churning.

### 3. Machine Learning Modeling
* **Preprocessing:** Handled missing values, removed unneeded columns (ID), and performed **One-Hot Encoding** for categorical variables.
* **Model Selection:** Implemented **Random Forest Classifier** due to its ability to handle complex interactions and feature importance analysis.
* **Data Splitting:** 80% Training / 20% Testing.

### 4. Model Evaluation
Given the business context, I focused on **Recall** alongside Accuracy.
* **Why Recall?** In churn prediction, False Negatives (predicting a customer will stay when they actually leave) are more costly than False Positives. We want to capture as many potential churners as possible.

---

## 📈 Results & Business Recommendations

Based on the Feature Importance analysis from the Random Forest model, the top drivers of churn are:
1.  **Contract Type (Month-to-month)**
2.  **Monthly Charges**
3.  **Tenure**

### 💡 Strategic Recommendations:
* **Promote Long-term Contracts:** Offer incentives (e.g., a discount on the first 3 months) for customers willing to switch from a month-to-month to a 1-year contract.
* **Target High-Value Groups:** Customers paying >$70/month are sensitive. A dedicated support line or loyalty perks could reduce their churn rate.
* **Onboarding Care:** Since low-tenure customers leave easily, improve the onboarding experience during the first 6 months.


