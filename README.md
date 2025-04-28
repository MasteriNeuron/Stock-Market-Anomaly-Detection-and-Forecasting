# 📈 Stock Market Anomaly Detection and Forecasting 🚀
![image](https://github.com/user-attachments/assets/64a8ca85-b622-44ff-81a0-24563abd6718)

Welcome to the NVIDIA (NVDA) Stock Analysis Project! This repository hosts a comprehensive pipeline for detecting anomalies and forecasting stock prices using time series analysis and machine learning. Built with Python, it leverages statistical and ML methods to deliver actionable insights for trading and risk management.

## 📚 Table of Contents
1. [Project Objective](#project-objective)
2. [Time Series and Components](#time-series-and-components)
3. [Anomalies in Time Series](#anomalies-in-time-series)
4. [Handling Anomalies](#handling-anomalies)
5. [Stationary vs. Non-Stationary](#stationary-vs-non-stationary)
6. [Conversion Methods](#conversion-methods)
7. [Dataset Description](#dataset-description)
8. [Workflow](#workflow)
9. [Code Explanations](#code-explanations)
10. [Project Setup](#project-setup)
11. [Future Enhancements](#future-enhancements)
12. [Conclusion](#conclusion)

## Project Objective 🎯
This project analyzes NVIDIA (NVDA) stock data to detect anomalies and forecast prices, combining anomaly detection (Isolation Forest, DBSCAN, LOF) with forecasting models (ARIMA, SARIMA, SARIMAX).

### Key Goals
- 🕵️‍♂️ **Identify anomalies**: Point, contextual, and collective.
- 🤖 **Apply ML for anomaly detection**: Isolation Forest, DBSCAN, LOF.
- 📈 **Preprocess and decompose time series**: Trend, seasonality, residuals.
- ✅ **Ensure stationarity**: ADF tests, ACF/PACF analysis.
- 📅 **Forecast prices**: Evaluate AR, MA, ARIMA, SARIMA, SARIMAX.
- 📊 **Visualize anomalies and forecasts for actionable insights.**

## Understanding Time Series and Its Components 📊

### Time Series Data
Sequential observations with temporal patterns (trends, seasonality, autocorrelation).  
Non-Time Series Data: Observations without temporal order.
![3](https://github.com/user-attachments/assets/1ca4ad09-5908-4489-b000-5b8d006f4525)

### Components
- 📈 **Trend**: Long-term direction.
- 🔄 **Seasonality**: Recurring patterns.
- 🌊 **Cyclical Patterns**: Long-term oscillations.
- ⚡️ **Noise**: Random fluctuations.

## Understanding Anomalies in Time Series Data ⚠️

### Types of Anomalies
- **Point Anomalies**: Isolated outliers (e.g., sudden price spikes).
- **Contextual Anomalies**: Outliers in specific contexts (e.g., intraday irregularities).
- **Collective Anomalies**: Unusual group patterns (e.g., volume surges).

## Handling of Anomalies in Time Series Data 🛠️

### Detection Methods:
- **ML**: Isolation Forest, DBSCAN, Local Outlier Factor (LOF).
- **Statistical**: Z-score, IQR rule.

### Imputation:
- Replace outliers with rolling medians for smoother series.

## Stationary & Non-Stationary Time Series 🔍

### Stationary:
- Constant mean, variance, autocorrelation.

### Non-Stationary:
- Varying mean, variance, or autocorrelation.

### Testing Methods
- 👀 Visual inspection of rolling statistics.
- 📉 **Augmented Dickey-Fuller (ADF)** test.
- 🔬 **KPSS** test.
- 📊 **Variance Ratio** test.

## Conversion Methods 🔄

- ➖ **Differencing**: Removes trends.
- 📏 **Log Transformation**: Stabilizes variance.
- 🔄 **Seasonal Adjustment**: Eliminates seasonal effects.
- 🛠️ **Combination**: Sequential transformations for complex data.

## Dataset Description 📂

- **Source**: Yahoo Finance (NVDA stock).
- **Period**: January 3, 2022 – April 22, 2025.
- **Frequency**: Daily trading data.
- **Features**: Date, Close, High, Low, Open, Volume.
- **Size**: 828 rows, 6 columns, no missing values.

## Workflow ⚙️
1. 🛠️ Set up environment and install libraries.
2. 📥 Retrieve NVDA data via yfinance and store as CSV.
3. 🧹 Preprocess: Clean, format, and index by date.
4. 📊 Conduct EDA: Summary statistics, visualizations.
5. 🔧 Engineer features: Daily returns, volatility.
6. 🕵️‍♂️ Detect anomalies: ML and statistical methods.
7. 📉 Test stationarity and decompose series (STL).
8. 📈 Analyze autocorrelation (ACF, PACF).
9. 🤖 Build and evaluate models: ARIMA, SARIMA, SARIMAX.

## Code Explanations 💻

### Data Retrieval
- Fetch NVDA data with yfinance.

### Preprocessing
- Use pandas for datetime indexing and sorting.

### Anomaly Detection
- Implement Isolation Forest, DBSCAN, LOF, Z-score, and IQR.

### Modeling
- Fit and forecast with ARIMA, SARIMA, SARIMAX using statsmodels.

## Project Setup 🛠️

- **Environment**: Jupyter Notebook or Google Colab.
- **Dependencies**: pandas, numpy, matplotlib, scikit-learn, statsmodels, yfinance.
- **Setup Steps**:
  - Clone the GitHub repository: `git clone <repo-url>`.
  - Install dependencies: `pip install -r requirements.txt`.
  - Run notebooks for analysis and modeling.

## Future Enhancements 🌟

- 🚀 **Advanced Models**: XGBoost, LSTM, or Transformers for forecasting.
- 📡 **Feature Expansion**: Add sentiment analysis (news, X posts) and macroeconomic indicators.
- ⚡️ **Real-Time Detection**: Stream intraday data for online anomaly detection.
- 🔧 **Tuning**: Use time-series cross-validation and Bayesian optimization.
- 📬 **Automation**: Deploy as a Flask/FastAPI service with anomaly alerts.
- 📊 **Backtesting**: Evaluate trading strategies with Sharpe ratio and drawdown metrics.

## Conclusion 🏁
This project establishes a robust pipeline for NVIDIA stock analysis, effectively detecting anomalies and forecasting prices using statistical and ML methods. **ARIMA(1,1,0)** delivers reliable short-term predictions, while anomaly detection enhances trading insights. Future enhancements, including advanced models and real-time deployment, promise to further elevate its practical impact in stock market applications.
