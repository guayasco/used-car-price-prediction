# 🚗 Used Car Price Prediction

Machine learning project to predict used car prices using regression and gradient boosting models, with a focus on balancing accuracy, training cost, and inference speed for real-world applications.

---

## 📌 Project Overview

This project simulates a pricing engine for a used car marketplace, where accurate and fast price estimation is critical for:

- Sellers listing vehicles competitively  
- Buyers evaluating fair market value  
- Platforms providing real-time pricing suggestions  

The objective is to build a model that captures complex relationships between vehicle attributes and price while remaining efficient enough for practical use.

---

## 📊 Problem

Used car prices are influenced by multiple interacting factors such as age, mileage, condition, and brand.

Key challenges:
- Non-linear depreciation patterns  
- Missing or inconsistent vehicle data  
- High-cardinality categorical features  

The goal is to develop a regression model that:
- Maximizes predictive performance  
- Handles imperfect real-world data  
- Maintains reasonable training and inference times  

---

## 📁 Data

The dataset consists of historical used car listings, including:

- Vehicle specifications (year, mileage, engine, etc.)  
- Model and configuration details  
- Historical pricing data  

---

## ⚙️ Approach

### 1. Data Preprocessing

- Handled missing values with consideration for **informational signal** rather than blindly removing data  
- Cleaned inconsistent entries and prepared features for modeling  
- Encoded categorical variables for compatibility with different models  

---

### 2. Feature Engineering

- Derived features such as **vehicle age** from registration year  
- Preserved missing values in key features when they showed correlation with price  
- Structured data to allow tree-based models to capture non-linear relationships  

---

### 3. Modeling

Trained and compared multiple models:

- Linear Regression (baseline)  
- Decision Tree  
- Random Forest  
- CatBoost  
- LightGBM  

Focus was placed on both **performance** and **computational efficiency**.

---

### 4. Evaluation

Models were evaluated using:

- **RMSE (Root Mean Squared Error)**  
- **R² Score**

Additionally, models were compared on:

- Training time  
- Prediction speed  

---

## 📈 Results

| Model            | RMSE    | R²    |
|------------------|--------:|------:|
| Linear Regression| 2618.26 | 0.646 |
| Decision Tree    | 1853.43 | 0.823 |
| Random Forest    | 1721.57 | 0.847 |
| CatBoost         | 1630.24 | 0.863 |
| LightGBM         | 1562.65 | 0.874 |

✅ **Best Model: LightGBM**

- Lowest RMSE  
- Highest R²  
- Strong balance between accuracy and efficiency  

LightGBM reduced RMSE by ~40% compared to the linear baseline, justifying the use of a more complex model.

---

## 🔍 Key Insights

- **Vehicle age and mileage** are the strongest predictors, with clear non-linear depreciation patterns  
- Missing values in condition-related features can carry **predictive signal** and should not always be removed  
- Tree-based models significantly outperform linear models by capturing feature interactions  
- Gradient boosting methods (LightGBM, CatBoost) provide the best balance between accuracy and computational cost  

---

## 🧰 Tech Stack

- Python  
- Pandas / NumPy  
- Scikit-learn  
- CatBoost  
- LightGBM  

---

## 🚀 How to Run

```bash
git clone https://github.com/guayasco/used-car-price-prediction.git
cd used-car-price-prediction
jupyter notebook notebook.ipynb
