# ☀️ Sunspot Activity Forecasting

A time-series forecasting project that predicts monthly mean sunspot numbers using classical ML and statistical models. The dataset covers **272 years of solar activity** (January 1749 – January 2021), making it one of the longest continuous scientific records available.

---

## 📌 Problem Statement

Sunspot activity follows an approximately **11-year solar cycle** and directly influences space weather, satellite operations, radio communications, and power grid stability. Accurate forecasting of sunspot numbers helps anticipate periods of high solar activity.

---

## 📊 Dataset

| Property       | Detail                                      |
|----------------|---------------------------------------------|
| Source         | `Sunspots.csv` (included in repo)           |
| Coverage       | January 1749 – January 2021                 |
| Frequency      | Monthly                                     |
| Target Variable| Monthly Mean Total Sunspot Number           |
| Total Records  | ~3,265 monthly observations                 |

---

## 🧠 Models Used

| Model          | Type                  | Approach                          |
|----------------|-----------------------|-----------------------------------|
| Decision Tree  | ML Regressor          | Lagged features as predictors     |
| XGBoost        | Gradient Boosting     | Lagged features as predictors     |
| ARIMA          | Statistical           | Hyperparameter-tuned (p, d, q)    |

**Feature Engineering:** Lagged sunspot values (t-1, t-2, ..., t-n) are used as input features for the ML models to capture temporal dependencies.

**Train/Test Split:** 80% training / 20% testing (chronological split — no shuffling).

---

## 📈 Results

All models are evaluated using **Mean Absolute Error (MAE)** against a naive baseline (predicting the training mean).

| Model         | MAE       |
|---------------|-----------|
| Baseline      | —         |
| Decision Tree | —         |
| XGBoost       | —         |
| ARIMA         | —         |

> 📓 Full results, plots, and model comparisons are in [`sun_spot.ipynb`](./sun_spot.ipynb).

---

## 🗂️ Project Structure

```
.
├── sun_spot.ipynb   # Full analysis: EDA, preprocessing, modeling, evaluation
├── Sunspots.csv     # Monthly sunspot dataset (1749–2021)
└── README.md
```

---

## ⚙️ Setup

### 1. Clone the repository

```bash
git clone https://github.com/elsayedghoonaim/sun-spot-forcasting.git
cd sun-spot-forcasting
```

### 2. Install dependencies

```bash
pip install numpy pandas matplotlib scikit-learn xgboost statsmodels jupyter
```

### 3. Run the notebook

```bash
jupyter notebook sun_spot.ipynb
```

---

## 🔭 Applications

- Space weather forecasting
- Satellite operations planning
- Radio communication disruption prediction
- Power grid risk assessment

---

## 📄 License

MIT License — free to use and build upon.
