# Air Quality in Nairobi – PM2.5 Forecasting

This project analyzes air quality data from Nairobi and builds time series models to forecast PM2.5 concentrations using low-cost sensor data.

## What I did

- Downloaded and cleaned air quality data from Kaggle (“Air Quality in Nairobi” by Peter Kamau, CC BY 4.0).
- Resampled raw sensor readings to **hourly** PM2.5 and PM10 time series.
- Performed exploratory data analysis (EDA):
  - Plotted PM2.5 over time.
  - Analyzed daily patterns (average PM2.5 by hour of day).
- Engineered features:
  - Lag features: `pm25_lag1` … `pm25_lag6`
  - Rolling means (3h and 6h)
  - Time features: `hour`, `dayofweek`, `month`
- Built and evaluated models:
  - **Baseline** (naive: predict next hour = last hour)
  - **Linear Regression**
  - **Random Forest** (non-linear autoregression)

## Key results

- Baseline MAE: ~3.06 µg/m³, RMSE: ~4.55 µg/m³  
- Random Forest MAE: ~1.36 µg/m³, RMSE: ~2.32 µg/m³, R²: ~0.91

PM2.5 is highly autocorrelated: past values and time-of-day features are strong predictors.

## Files

- `Nairobi air-quality.ipynb` – Main notebook with full analysis.
- `README.md` – This file.
- `.gitignore` – Python template.
- `LICENSE` – MIT License.

## How to run

1. Install dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn kagglehub
```

2. Clone the repo and open the notebook:

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
jupyter notebook "Nairobi air-quality.ipynb"
```

3. Run the cells from top to bottom.

## About me

I’m a data science / data engineering student based in Nairobi, focused on time series, machine learning, and end-to-end data projects.

- LinkedIn: (add your URL)
- Email: (optional)
