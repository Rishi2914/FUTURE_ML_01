# 📊 Sales Forecasting Dashboard — Retail Analytics
### Future Interns | Machine Learning Internship 2026 | Task 1

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?style=flat&logo=googlecolab&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=flat&logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---

## 🗂️ Project Overview

A predictive analytics project for retail sales forecasting using **Machine Learning regression models** and **Matplotlib** visualizations, built entirely in **Google Colab**. The system analyzes 3 years of historical Superstore sales data (2021–2023), trains Linear Regression and Random Forest models, and delivers a 6-month forward forecast with confidence intervals — all presented through a multi-panel business dashboard generated in Python.

---

## 🎯 Objective

Build an end-to-end forecasting pipeline that helps retail businesses:
- Predict future monthly sales with quantified uncertainty
- Identify seasonal trends and demand patterns
- Make data-driven inventory and staffing decisions
- Present insights in a format accessible to non-technical stakeholders

---

## 🛠️ Technologies Used

| Layer | Tools |
|---|---|
| **Language** | Python 3.8+ |
| **Data Processing** | Pandas, NumPy |
| **Machine Learning** | Scikit-learn (Linear Regression, Random Forest) |
| **Visualization** | Matplotlib, Seaborn |
| **Development** | Google Colab |
| **Version Control** | GitHub |
| **Dataset** | Superstore Sales Dataset (2021–2023) |

---

## 📁 Project Structure

```
FUTURE_ML_01/
│
├── data/
│   ├── historical_sales.csv        # Monthly aggregated sales + features
│   ├── model_predictions.csv       # Actual vs LR vs RF on test set
│   ├── forecast.csv                # 6-month forward forecast
│   ├── metrics.csv                 # MAE, RMSE, R², MAPE scores
│   ├── feature_importance.csv      # Random Forest feature importances
│   └── monthly_summary.csv         # Year-over-year summary stats
│
├── notebooks/
│   └── FUTURE_ML_01.ipynb          # Full pipeline: cleaning → features → training → forecast
│
├── outputs/
│   ├── chart1_historical_sales.png
│   ├── chart2_model_predictions.png
│   ├── chart3_forecast.png
│   └── chart4_metrics_features.png
│
└── README.md
```

---

## 📊 Key Features

- ✅ Data cleaning, aggregation, and time-based feature engineering
- ✅ 14 engineered features including lag values, rolling statistics, and cyclical encoding
- ✅ Two ML models trained and compared: Linear Regression vs Random Forest
- ✅ Chronological train/test split (no data leakage)
- ✅ 6-month iterative forecast with ±10% confidence band
- ✅ 5-panel Matplotlib dashboard with business-ready visuals
- ✅ Actionable business recommendations from forecast output

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)

1. Open [Google Colab](https://colab.research.google.com)
2. Upload `FUTURE_ML_01.ipynb` or open it directly from GitHub
3. Run all cells — the notebook installs dependencies automatically
4. Download the generated charts from the Colab files panel

### Option 2 — Local

**Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn requests
```

**Clone and run**
```bash
git clone https://github.com/Rishi2914/FUTURE_ML_01.git
cd FUTURE_ML_01
python notebooks/FUTURE_ML_01.py
```

---

## 🔍 Feature Engineering

| Feature | Description |
|---|---|
| `month_idx` | Global time index — captures long-term trend |
| `sin_month` / `cos_month` | Cyclical month encoding — captures seasonality |
| `lag_1`, `lag_3`, `lag_12` | Sales 1, 3, and 12 months ago |
| `rolling_mean_3` / `rolling_mean_6` | 3 and 6 month moving averages |
| `rolling_std_3` | Sales volatility over last 3 months |
| `is_q4` / `is_december` | Holiday period flags |
| `mom_growth` | Month-over-month % change |

---

## 📊 Model Performance

| Model | MAE | RMSE | R² | MAPE |
|---|---|---|---|---|
| Linear Regression | $1,006 | $1,355 | 0.953 | 1.7% |
| Random Forest | $3,425 | $4,367 | 0.512 | 5.9% |

> **Best Model: Linear Regression** (R² = 0.953, MAPE = 1.7%)
>
> Linear Regression outperformed Random Forest on this dataset due to the strong linear trend in the data. The `lag_12` feature (sales from the same month last year) was by far the most important predictor at **90.2% importance** in the Random Forest model.

---

## 🔍 Key Insights

- **Strong upward trend** — Monthly sales grew consistently from ~$40k (Jan 2021) to ~$70k (Jan 2024)
- **Clear Q4 seasonality** — December spikes visible across all years; January follows with a dip
- **Stable 6-month forecast** — RF predicts $60.1k → $60.6k/month for Jan–Jun 2024 with tight confidence bands
- **lag_12 dominates** — Same-month-last-year is the strongest signal at 90.2% RF feature importance
- **Linear model wins** — The data's linear growth structure favours LR over tree-based methods at this dataset size

---

## 🎓 Business Recommendations

1. **Stock up inventory** 2–3 months before Q4 to avoid supply shortages during the holiday peak
2. **Run targeted promotions** during February–April (historically the weakest quarter)
3. **Use the lower forecast bound** for conservative budget planning (~$54k/month lower bound)
4. **Track actuals vs forecast** monthly — if deviation exceeds 10%, retrain the model with fresh data
5. **Upward trend confirmed** — forecast of ~$60k/month suggests continued growth; consider expanding SKUs

---

## 📸 Dashboard Screenshots

### Panel 1 — Historical Monthly Sales (2021–2023)
![Historical Sales](outputs/chart1_historical_sales.png)

### Panel 2 — Model Predictions vs Actual Sales (Test Set)
![Model Predictions](outputs/chart2_model_predictions.png)

### Panel 3 — 6-Month Sales Forecast (Jan–Jun 2024)
![Forecast](outputs/chart3_forecast.png)

### Panel 4 — Model Metrics & Feature Importances
![Metrics and Features](outputs/chart4_metrics_features.png)

---

## 👨‍💻 Author

**Rishikesh Reddy Arjula**
- 🎓 Internship: Future Interns — Machine Learning Track
- 📅 Year: 2026
- 🐙 GitHub: [Rishi2914](https://github.com/Rishi2914)
- 🔗 LinkedIn: [rishikesh-reddy-arjula](https://www.linkedin.com/in/rishikesh-reddy-arjula-259652264/)

---

## 📝 License

This project was built for educational and internship purposes as part of the **Future Interns Machine Learning Program**.

---

*If you found this project helpful, consider giving it a ⭐ on GitHub!*
