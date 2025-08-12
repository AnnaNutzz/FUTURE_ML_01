# FUTURE_ML_01

# Sales Forecasting with Prophet & Power BI

## 📌 Project Overview
This project demonstrates the process of **forecasting future sales** using the Facebook Prophet time series model and visualizing the results in **Power BI**.  
It covers:
- Data cleaning & preprocessing in Python
- Time series forecasting using Prophet
- Exporting forecast data to CSV
- Building interactive Power BI dashboards for actual vs forecasted sales, including evaluation metrics

---

## 🛠️ Tech Stack
- **Python** (Pandas, Prophet, scikit-learn)
- **Power BI**
- **Pandas** for data manipulation
- **Prophet** for time series forecasting
- **Scikit-learn** for evaluation metrics

---

## 📂 Project Structure
├── mock_kaggle.csv # Raw dataset
├── FUTURE_ML_01.ipynb # Python script for forecasting
├── FUTURE_ML_01_PBi.pbix # Power BI dashboard file
├── sales_actual_forecast.csv # Forecast results for Power BI
└── README.md # Project documentation

---

## 📊 Features
- **90-day forecast** with yearly, weekly, and custom monthly seasonality.
- Evaluation using:
  - **Mean Absolute Error (MAE)**
  - **Root Mean Square Error (RMSE)**
- Clear separation of actual vs. forecast values in Power BI visuals.
- Exported CSV ready for direct import into Power BI.

---

The workflow includes:
1. Data cleaning and preprocessing.
2. Building a forecasting model with Prophet.
3. Exporting the forecast results to CSV.
4. Creating a Power BI dashboard to visualize:
   - Historical sales
   - Forecasted sales
   - Forecast accuracy metrics (MAE & RMSE)
   - Yearly and monthly breakdowns

---

## 🐞 Common Issues & Fixes

### 1. `Missing column provided to 'parse_dates': 'date'`
**Cause:** CSV file did not have a column named exactly `"date"`.  
**Fix:** Checked actual column names with `print(df.columns)` and used the correct one (`"data"`).

---

### 2. `Error tokenizing data. C error: Expected 1 fields in line 4, saw 6`
**Cause:** CSV had commas inside quoted strings.  
**Fix:** Used:
```python
pd.read_csv("mock_kaggle.csv", encoding="latin1", sep=",", quotechar='"')
```

---

## 🛠️ Setup & Usage
1. **Install dependencies**
   ```bash
   pip install pandas prophet scikit-learn
   ```
