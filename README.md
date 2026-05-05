# Used Car Price Prediction

Machine learning project to predict used car prices based on vehicle specifications and historical data, using regression models and gradient boosting techniques.

---

## 📌 Project Type
- Regression / Supervised Machine Learning

---

## 📊 Problem

Accurately estimating the market value of used cars is essential for both buyers and sellers.  
The goal of this project is to build a model that predicts car prices based on technical features, while balancing:

- Prediction accuracy  
- Training time  
- Inference speed  

---

## 📁 Data

The dataset includes historical records of used cars with features such as:

- Vehicle specifications (e.g., engine, mileage, year)
- Model and configuration details
- Historical pricing information

---

## ⚙️ Approach

1. **Data Preprocessing**
   - Handled missing values and inconsistent entries  
   - Encoded categorical variables  
   - Prepared dataset for modeling  

2. **Modeling**
   - Trained and compared multiple regression models:
     - Linear Regression (baseline)
     - Decision Tree
     - Random Forest
     - CatBoost
     - LightGBM  

3. **Evaluation**
   - Metrics used:
     - RMSE (Root Mean Squared Error)
     - R² Score  

4. **Performance vs Efficiency Analysis**
   - Compared models not only on accuracy, but also:
     - Training time  
     - Prediction speed  

---

## 📈 Results

| Model            | RMSE     | R²    |
|------------------|----------|-------|
| Linear Regression| **2618.26** | **0.646** |
| Decision Tree    | **1853.43** | **0.823** |
| Random Forest    | **1721.57** | **0.847** |
| CatBoost         | **1630.24** | **0.863** |
| LightGBM         | **1562.65** | **0.874** |

✅ **Best Model:** LightGBM  
- Lowest RMSE  
- Highest R²  
- Strong balance between accuracy and efficiency  

---

## 🔍 Key Insights

- Tree-based models significantly outperform linear models for this problem  
- Gradient boosting methods (LightGBM, CatBoost) capture complex feature interactions effectively  
- Feature engineering and non-linear modeling are critical for price prediction tasks  
- LightGBM offers the best trade-off between performance and computational efficiency  

---

## 🧰 Tech Stack

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- CatBoost  
- LightGBM  

---

## 🚀 How to Run

1. Clone the repository:
   
   git clone https://github.com/guayasco/used-car-price-prediction.git

2. Install dependencies:

  pip install -r requirements.txt
  
3. Open the notebook:

  jupyter notebook notebook.ipynb
