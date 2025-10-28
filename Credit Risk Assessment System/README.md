# 💳 Credit Risk Analysis Using LightGBM  

## 🧠 Project Overview  
This project focuses on **Credit Risk Prediction** — determining whether a customer will default on their next payment using financial and behavioral data.  
The workflow covers **data preprocessing, feature engineering, model training, and evaluation** to support smarter and data-driven lending decisions.  

By analyzing financial features such as **total bills, payments, and credit limits**, the model helps financial institutions identify risky borrowers while minimizing missed opportunities.  

---

## ⚙️ Step 1: Data Preprocessing & Feature Engineering  

### 🧩 Summary of Steps  
This notebook performs the following key steps for preparing the dataset:  

1. **Setting up the Environment**  
   - Imports required libraries: `numpy`, `pandas`, `zipfile`, `StandardScaler`, `train_test_split`.  

2. **Loading the Dataset**  
   - Unzips and loads `credit_risk_dataset.zip`.  
   - Reads `credit_data.csv` into a Pandas DataFrame.  

3. **Data Preprocessing**  
   - Confirms no missing values and checks data types.  
   - Drops the unnecessary `'ID'` column.  
   - Applies **feature scaling** using `StandardScaler` on `'BILL_AMT'` and `'PAY_AMT'` columns.  

4. **Feature Engineering**  
   - Creates new, informative features:  
     - `TOTAL_BILL_AMT` → Total of all bill amounts.  
     - `TOTAL_PAY_AMT` → Total of all payments.  
     - `PAY_BILL_RATIO` → Ratio of total payment to total bill.  
     - `AVG_PAY_DELAY` → Average payment delay (mean of PAY_0 to PAY_6).  
   - Removes original raw columns for cleaner modeling.  

5. **Data Splitting**  
   - Splits data into **features (X)** and **target (y)** (`default.payment.next.month`).  
   - Uses an 80/20 **train-test split** with stratification for balanced target representation.  

6. **Exporting the Processed Data**  
   - Saves the cleaned and engineered dataset as `lendingclub_processed.csv`.  

---

## 🤖 Step 2: Model Building & Evaluation  

### 📊 Model Evaluation Summary  
- The **LightGBM** model outperformed other models, achieving:  
  - **Accuracy:** ~80.5%  
  - **AUC-ROC:** 0.764 ✅  
- This indicates strong predictive power and balance between true and false positives.  

### 🔑 Key Feature Insights  
- **Most Influential Features:**  
  - `TOTAL_BILL_AMT` 💰  
  - `PAY_BILL_RATIO` 📉  
  - `TOTAL_PAY_AMT` 💵  
- **Moderate Contributors:**  
  - `AGE` 👤  
  - `LIMIT_BAL` 💳  
- The model learns heavily from repayment and spending behavior — aligning with financial logic.  

### 💡 Lending Decision Simulation  
Using a **default threshold of 0.5** probability:  
- ✅ ~70% applicants approved.  
- ⚠️ ~20% of approved customers may default.  
- ❌ ~15% rejected applicants were actually safe (missed opportunities).  

**Threshold Tuning:**  
- Lower threshold (e.g., 0.4): More approvals ➕ higher risk.  
- Higher threshold (e.g., 0.6): Fewer defaults ➖ lower revenue.  

Choose based on business goals:  
- **Risk-Averse Strategy:** Minimize defaults.  
- **Growth Strategy:** Accept more applicants, tolerate higher risk.  

---

## ⚖️ Risks & Considerations  
- 📉 Model depends on **historical data** — may lose accuracy with economic changes.  
- 🧩 **Fairness issues** may arise if certain groups are underrepresented.  
- 🔁 Requires **continuous monitoring** and periodic retraining for sustained performance.  

---

## 📦 Files in This Project  

| File | Description |
|------|--------------|
| `Project_3.1_(a).ipynb` | Handles data cleaning, scaling, and feature engineering |
| `Project_3.1_(b).ipynb` | Trains LightGBM model, evaluates performance, and simulates lending decisions |

---

## 🏁 Conclusion  
This project demonstrates how **machine learning can support smarter lending decisions** by assessing credit risk using behavioral and financial insights.  
The **LightGBM model** provides a strong foundation for credit scoring systems — balancing accuracy, interpretability, and business flexibility.  

---

## 🌟 Author  
👤 **Muhammad Umer**  
📬 _Connect on LInkedIn: https://www.linkedin.com/in/muhammad-umer-b39171337/_  
📂 Explore this repo for more AI/ML projects and insights!  

---

## 🧩 Tech Stack  
**Languages & Libraries:** Python 🐍 | Pandas 🐼 | NumPy 🔢 | LightGBM ⚡ | Scikit-learn 🧮  
**Techniques:** Feature Engineering ⚙️ | Model Evaluation 📊 | Data Preprocessing 🧼  

---
