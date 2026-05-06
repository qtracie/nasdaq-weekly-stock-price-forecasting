# nasdaq-weekly-stock-price-forecasting
Time series forecasting project for weekly NASDAQ stock prices using ARIMA/ARIMAX and human-adjusted predictions.
# NASDAQ Weekly Stock Price Forecasting

## Project Objective

This project forecasts weekly end prices of selected NASDAQ-listed stocks. The goal is to generate two types of forecasts for each company:

1. A model-based forecast generated using statistical and machine learning models.
2. A human-adjusted forecast that incorporates market insights, intuition, and external factors.

The better-performing forecast will be considered for final evaluation once actual future prices become available.

## Companies Included

The project includes the following NASDAQ-listed companies:

- Adobe (ADBE)
- Apple (AAPL)
- NVIDIA (NVDA)
- Amazon (AMZN)
- AstraZeneca (AZN)
- Starbucks (SBUX)
- Tesla (TSLA)
- United Airlines (UAL)
- Warner Music Group (WMG)
- Wendy's (WEN)
- American Airlines (AAL)

## Methodology

### Model-Based Forecasting

The model-based forecasting approach uses Auto-ARIMA / ARIMAX to forecast weekly closing prices.

Key steps:

- Collected 5-year historical stock data using `yfinance`
- Converted daily stock prices into weekly Friday closing prices
- Added external market indicators:
  - NASDAQ Composite Index
  - S&P 500 Index
- Split the data into 80% training and 20% testing sets
- Evaluated model performance using MAE and MSE
- Refit the model on the full dataset
- Forecasted weekly prices for the next five weeks

### Human-Adjusted Forecasting

The human-adjusted forecast incorporates additional market intuition and external factors.

Factors considered include:

- Moving average indicators
- Open, high, low, close, and volume data
- Oil price shocks
- Regional instability and geopolitical risk
- Randomized volatility adjustments
- Risk categorization by stock

## Files in This Repository

| File | Description |
|---|---|
| `OPIM_5671_Term_Project_1.ipynb` | Main notebook containing data collection, modeling, forecasting, and evaluation |
| `OPIM_5671_Term_Project_01_Forecasts.xlsx` | Final forecast results submitted for the project |
| `OPIM_5671_Time_Series_Forecasting.pptx` | Presentation slides summarizing the project |
| `requirements.txt` | Python packages required to run the notebook |

## Key Insights

- Statistical models provide consistent, data-driven forecasts.
- Forecast accuracy varies depending on stock volatility.
- Market-wide factors such as NASDAQ and S&P 500 movements influence many stocks simultaneously.
- Human-adjusted forecasts can help reflect real-world market uncertainty that may not be fully captured by the model.

## Tools Used

- Python
- yfinance
- pandas
- Auto-ARIMA / ARIMAX
- XGBoost
- Excel
- PowerPoint
