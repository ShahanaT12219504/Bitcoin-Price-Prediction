# 📈 Bitcoin Price Prediction Using Machine Learning 🧠💰

## 📝 Overview
This project uses machine learning to predict Bitcoin's closing price based on historical price data. The goal is to assist traders and investors with smarter decisions by forecasting short-term price trends using regression-based models.

## 🎯 Objectives
- Predict Bitcoin closing prices using historical data.
- Apply feature engineering to improve model performance.
- Compare regression models like Linear Regression, SVR, and Random Forest.

## 📚 Dataset
- **Source**: [GeeksforGeeks Bitcoin Dataset](https://media.geeksforgeeks.org/wp-content/uploads/20240917132611/bitcoin.csv)
- **Size**: 2713 rows × 7 columns
- **Features**: `Date`, `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`
- **Engineered Features**:
  - `open-close`: Daily price difference
  - `low-high`: Price range within the day
  - `year`, `month`, `day`: Extracted from `Date`
  - `is_quarter_end`: Boolean flag for quarter-end days

## 🧹 Data Preprocessing
- No missing values 🎉
- Outliers handled using the IQR method, capped at the 99th percentile.
- Feature selection via:
  - Correlation Matrix
  - Recursive Feature Elimination (RFE)
  - Random Forest feature importance

## 🛠️ Tools & Libraries
- Python 🐍
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn` for modeling
- `RandomForestRegressor`, `SVR`, `LinearRegression`

## 🤖 Machine Learning Models
1. **Linear Regression** – For baseline performance
2. **Support Vector Regression (SVR)** – Handles non-linearity
3. **Random Forest Regressor** – Best performer with ensemble magic 🌲

## ⚙️ Model Training
- Dataset split: 80% train / 20% test
- Feature scaling and selection applied
- Hyperparameter tuning with `GridSearchCV`

## 📊 Evaluation Metrics
- **RMSE (Root Mean Squared Error)**
- **R² Score**

| Model               | RMSE     | R² Score |
|--------------------|----------|----------|
| Linear Regression  | 1034.21  | 0.72     |
| SVR                | 612.42   | 0.85     |
| 🏆 Random Forest    | 456.80   | 0.91     |

## ✅ Results & Insights
- **Random Forest** outperformed all models with the lowest RMSE and highest R².
- SVR showed good potential but required careful parameter tuning.
- Linear Regression was the weakest due to multicollinearity issues.

## 🔮 Future Work
- Add external factors like news sentiment and macroeconomic indicators 📈📰
- Try deep learning models like LSTM for time-series prediction 🔁🧠
- Real-time prediction using API integration
