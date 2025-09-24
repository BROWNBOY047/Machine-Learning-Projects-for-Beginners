# 🏡 Boston Housing Price Prediction

This project demonstrates how to clean data and train a Linear Regression model to predict house prices using the famous Boston Housing dataset.

---

## 📂 Project Structure

* Assignment\_1.1a.ipynb → Data cleaning (handling missing values, outliers, saving cleaned dataset)
* Assignment\_1.1b.ipynb → Model training and evaluation using Linear Regression
* boston\_cleaned.csv → The cleaned dataset ready for modeling
* README.md → Project documentation

---

## 📊 Dataset Information

The dataset contains information about housing in Boston such as crime rate, number of rooms, property tax rate, and median house value.

* Features: 13 numerical attributes (e.g., crime rate, rooms, distance to employment centers)
* Target: Median value of owner-occupied homes (MEDV)

The original dataset is available in two places:

* UCI Machine Learning Repository
* Scikit-learn’s built-in datasets (can be loaded directly without downloading manually)

---

## 🧹 Data Cleaning (Assignment 1.1a)

Steps performed:

1. Inspected data types, missing values, and outliers
2. Handled missing values if present
3. Detected and treated outliers
4. Saved the cleaned dataset as boston\_cleaned.csv

---

## 🤖 Model Training (Assignment 1.1b)

* Split data into features (X) and target (y)
* Performed train/test split using scikit-learn
* Trained a Linear Regression model
* Evaluated using:

  * Mean Squared Error (MSE)
  * Mean Absolute Error (MAE)
  * Root Mean Squared Error (RMSE)
  * Mean Absolute Percentage Error (MAPE)

---

## 📌 Results & Significance

* Metrics were calculated and compared
* Each metric’s meaning was explained (for example, MAE as the average prediction error in house prices)

---

## 🚀 How to Run

1. Clone the repository
2. Navigate into the project folder
3. Open the notebooks in Jupyter Notebook or Google Colab

---

## 🙌 Acknowledgments

* Dataset originally from the UCI Machine Learning Repository
* Also available in scikit-learn’s dataset library

---

✨ This project is beginner-friendly and demonstrates the full ML workflow:
**Data Cleaning → Feature Preparation → Model Training → Evaluation**

---
