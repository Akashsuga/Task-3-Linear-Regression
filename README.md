# Task-3-Linear-Regression
# Housing Price Prediction – Linear Regression

This project applies both Simple and Multiple Linear Regression to predict house prices using features such as area, number of bedrooms, and furnishing status.

---

## Dataset Overview

- Filename: Housing.csv
- Features: area, bedrooms, bathrooms, furnishingstatus, mainroad, guestroom, basement, hotwaterheating, airconditioning, parking, etc.

---

## Goals

- Perform Simple Linear Regression using area → price
- Perform Multiple Linear Regression using all features
- Evaluate and visualize model performance
- Derive insights, patterns, and detect anomalies

---

## Tools Used

- Python 
- Pandas, NumPy
- scikit-learn
- Seaborn, Matplotlib

---

## 1. Simple Linear Regression (area → price)

We model the relationship between the house area and its price.

📊 Scatter Plot: Area vs Price with Regression Line
![Area Vs Price (SLR)](https://github.com/user-attachments/assets/75cece48-8e77-4e61-a463-913cbdba5260)

🟢 Insight:

- There is a clear positive linear trend: larger area → higher price.
- The regression line fits the data reasonably well.

🔶 Pattern:

- Most points cluster around the line.
- Some variability exists for the same area range.

❗ Anomalies:

- A few points lie far above or below the regression line.
- Possible causes: premium location, renovation, or data entry issues.

📈 Evaluation:

- MAE, MSE, and R² are printed in the script output.
- R² is moderate, which is expected since only one variable is used.

---

## 2. Multiple Linear Regression (All Features)

This model incorporates all numeric and encoded categorical variables.

📊 Correlation Matrix
![Correlation Matrix](https://github.com/user-attachments/assets/f5e94b3d-9bb4-4b66-a05a-c464bfda7538)

🟢 Insight:

- Area shows a strong positive correlation with price.
- Furnishing status and air conditioning also contribute positively.
- Some features (e.g., guestroom, hotwaterheating) are weakly correlated individually but useful in combination.

🔶 Pattern:

- Most features have low correlation with each other — no severe multicollinearity detected.

❗ Anomalies:

- No immediate correlation-based anomalies, but low-contribution features may introduce noise.

📊 Actual vs Predicted Plot
![Actual Vs Predicted (MLR](https://github.com/user-attachments/assets/f05d1f1e-ef6d-47d1-a81b-caab99fcaeea)

🟢 Insight:

- Predictions align well with actual prices — points are close to the diagonal.

🔶 Pattern:

- Best performance is seen for mid-range prices.
- Underprediction on some high-priced houses.

❗ Anomalies:

- Outliers appear for some luxury homes: predicted price much lower than actual.

📊 Residuals Distribution Plot
![Residuals Distribution](https://github.com/user-attachments/assets/f7ef56ae-1f1c-4b7a-b80e-eccd00ca2e73)

🟢 Insight:

- Residuals are approximately normally distributed, centered near 0.

🔶 Pattern:

- Slight right-skew: some predictions underestimate actual values.

❗ Anomalies:

- A few large residuals (>2 standard deviations) indicate the presence of influential points.

---

## 4. Key Learnings

- Area is the most significant driver of price, but other features add valuable context.
- Linear regression works well when assumptions (normality, linearity, independence) are met.
- Visualizations help identify outliers and improve feature selection.

---

## 
├── Housing.csv
├── House Price Prediction.py
├── README.md
└── (You can include a screenshots/ folder with plot images)
