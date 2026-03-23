# 📊 Sales & Demand Forecasting for Businesses
### Future Interns | Machine Learning Internship 2026 | Task 1

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?style=flat&logo=googlecolab&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=flat&logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---

## 🗂️ Project Overview

A predictive analytics project for retail sales forecasting using **Machine Learning regression models** and **Matplotlib** visualizations, built in **Google Colab**. The system analyzes historical sales data, trains Linear Regression and Random Forest models, and delivers a 6-month forward forecast with confidence intervals.

---

## 🎯 Task Requirements Met
✔ **Data Cleaning & Engineering**: Automated handling of missing data and creation of 14 time-based features (lags, rolling means, cyclical encoding).
✔ **Forecasting Models**: Implementation of Linear Regression and Random Forest models.
✔ **Evaluation & Error Analysis**: Comprehensive metrics including MAE, RMSE, R², and MAPE.
✔ **Visual Insights**: Business-ready dashboard showcasing historical trends, model accuracy, and future forecasts.

---

## 🛠️ Technologies Used

| Layer | Tools |
|---|---|
| **Language** | Python 3.8+ |
| **Data Processing** | Pandas, NumPy |
| **Machine Learning** | Scikit-learn (Linear Regression, Random Forest) |
| **Visualization** | Matplotlib, Seaborn |
| **Environment** | Google Colab / Jupyter |

---

## 📁 Project Structure

```
FUTURE_ML_01/
│
├── ML_Task_1.ipynb          # Full pipeline: cleaning → features → training → forecast
├── historical_sales.csv     # Monthly aggregated sales + features
├── model_predictions.csv    # Actual vs predicted values
├── forecast.csv             # 6-month forward forecast
├── metrics.csv              # MAE, RMSE, R², MAPE scores
├── feature_importance.csv   # Random Forest feature rankings
└── README.md
```

---

## 📊 Model Performance (Actual Results)

| Model | MAE | RMSE | R² | MAPE |
|---|---|---|---|---|
| **Linear Regression** | $820.52 | $1,141.75 | **0.964** | **1.46%** |
| Random Forest | $4,354.82 | $6,020.56 | 0.005 | 7.06% |

> **Best Model: Linear Regression**. The strong linear trend in the sales data allowed the regression model to achieve a high R² of 0.964.

---

## 🔍 Key Insights

- **Seasonality**: `lag_12` (sales from the same month last year) is the dominant predictor with **84.8% importance**.
- **Growth Trend**: Clear upward trajectory in sales from 2021 through 2023.
- **Forecast**: Projected revenue for the next 6 months is approximately **$362,800**.

---

## 🚀 How to Run

1. Open `ML_Task_1.ipynb` in [Google Colab](https://colab.research.google.com).
2. Ensure you have the necessary libraries installed: `pip install pandas matplotlib scikit-learn`.
3. Run all cells to process data, train models, and generate the CSV outputs and dashboard.

---

## 👨‍💻 Author

**Rishikesh Reddy Arjula**
- 🎓 Internship: Future Interns — Machine Learning Track
- 📅 Year: 2026
- 🐙 GitHub: [Rishi2914](https://github.com/Rishi2914)
- 🔗 LinkedIn: [Rishikesh Reddy Arjula](https://www.linkedin.com/in/rishikesh-reddy-arjula-259652264/)
- 📧 Email: [reddyrishikesh271@gmail.com](mailto:reddyrishikesh271@gmail.com)

---

## 📝 License

This project was built for educational purposes as part of the **Future Interns Machine Learning Program**.
