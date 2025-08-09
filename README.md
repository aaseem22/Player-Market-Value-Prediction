# ⚽ Football Player Market Value Prediction

This project predicts the **market value of football players** using a **machine learning model** trained on in-game statistics from a comprehensive dataset.  

It follows a complete **ML pipeline** — from **data cleaning** and **feature engineering** to **model training**, **evaluation**, and **deployment readiness**.

---

## 📋 Key Features

- **Data Cleaning** – Handles messy data formats like `"70+1"` and currency values like `"€4.1M"`.
- **Feature Engineering** – Transforms raw data into meaningful numerical features, including one-hot encoding for categorical variables.
- **Predictive Modeling** – Uses `RandomForestRegressor` to capture complex relationships between player attributes and market value.
- **Model Evaluation** – Evaluates performance with **R²** and **MAE**.
- **Feature Importance Analysis** – Identifies the most influential attributes on player value.

---

## 🛠 Tech Stack

- **Data Manipulation**: `pandas`, `numpy`
- **Machine Learning**: `scikit-learn`
- **Visualization**: `matplotlib`, `seaborn`
  
---

## ⚙️ How It Works

### 1. Load Data
Reads `players_3120.csv`.

### 2. Preprocess Data
Cleans and converts all attributes and currency values to numerical format. Missing values are filled using column medians.

### 3. Scale Features
Standardizes numerical features using `StandardScaler`.

### 4. Train Model
Splits the dataset into train/test sets and trains a `RandomForestRegressor`.

### 5. Evaluate Model
Makes predictions on test data and calculates **R²** and **MAE**.

### 6. Save Artifacts
Exports `model.pkl` and `scaler.pkl` for deployment.

---

## 📊 Model Performance

- **R² Score**: **0.99**  
  > Explains 99% of variance in player market values — near-perfect fit.
- **Mean Absolute Error (MAE)**: ~**€730,000**  
  > On average, predictions are within €730k of the actual market value.
