# 📊 Telco Customer Churn Prediction using Machine Learning

This project predicts **customer churn** using the popular **Telco Customer Churn dataset**.  
It involves data preprocessing, feature engineering, model training, and performance comparison across multiple ML algorithms.

---

## 📁 Project Structure

- **Part A – Data Preprocessing & Encoding**
- **Part B – Model Training & Evaluation**

---

## 🚀 Part A: Data Preprocessing

### 🔹 Step 1: Load Dataset
- Loaded the **Telco Customer Churn dataset** into a pandas DataFrame.
- Dataset shape: **7043 rows × 21 columns**

### 🔹 Step 2: Inspect Dataset
- Used `df.info()` and `df.head()` to explore data.
- Found a mix of **categorical** and **numerical** features.
- Dropped `customerID` as it’s just an identifier.

**Key features:**
- Categorical: `InternetService`, `Contract`, `PaymentMethod`, etc.
- Numerical: `SeniorCitizen`, `tenure`, `MonthlyCharges`, `TotalCharges`

### 🔹 Step 3: Handle Missing Values
- Initially no missing values.
- After converting `TotalCharges` from object → float, **11 missing values** appeared (blank rows).
- Dropped those rows.
- Final dataset shape: **7032 rows × 21 columns**

### 🔹 Step 4: Encode Categorical Variables
- Binary columns (e.g., `gender`, `Partner`, `Dependents`, `Churn`) encoded using **LabelEncoder** / mapping.
- Multi-class columns encoded using **One-Hot Encoding (`pd.get_dummies`)**.
- Dropped low-importance column `gender`.

✅ **Final encoded dataset shape:** `7032 × 40`  
All features are now **numerical (int64)** and ready for modeling.

---

## 🤖 Part B: Model Training & Evaluation

### 🔹 Models Trained
1. Logistic Regression  
2. Decision Tree  
3. Random Forest  
4. Gradient Boosting  
5. Support Vector Machine (SVM)  
6. MLP Neural Network

### 🔹 Workflow
- Loaded the **encoded dataset (telco_encoded.csv)**  
- Split into **training** and **testing** sets  
- Trained all models  
- Generated **evaluation metrics:**
  - Accuracy  
  - Classification Report  
  - ROC-AUC Score  


### 🏆 Best Model
The **MLP Neural Network** achieved the **best overall performance** and was selected as the final model.

---

## 📈 Technologies Used
- Python 🐍  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib / Seaborn  
- Jupyter Notebook  

---


## 🧩 Next Steps
- Hyperparameter tuning for MLP  
- Model explainability (e.g., SHAP, LIME)  
- Flask/Streamlit app deployment  

---

## 👨‍💻 Author
**Muhammad Umer**  
B.S. Computer Science – Machine Learning & Data Science Enthusiast  
📧 https://www.linkedin.com/in/muhammad-umer-b39171337/

---

## ⭐ If you find this project useful
Don’t forget to **star 🌟** the repository and share your feedback!

---

