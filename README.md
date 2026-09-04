# Retail Sales Time Series Forecasting

A time series forecasting project comparing simple baseline methods for predicting monthly retail sales.

The goal was to establish a reliable benchmark before evaluating more complex forecasting models.

## Project Objective

The project compares three forecasting approaches:

- Naive Forecast
- Seasonal Naive Forecast
- 3-Month Moving Average

The final 12 months of the dataset were reserved as a test period.

Forecasts were generated chronologically to avoid using future information.

## Dataset

The dataset contains:

- 108 monthly observations
- January 2017 to December 2025
- 96 months used for training
- 12 months used for testing

The target variable is monthly retail sales.

## Forecasting Methods

### Naive Forecast

Uses the previous month's actual sales as the next month's forecast.

### Seasonal Naive

Uses sales from the same month one year earlier.

### 3-Month Moving Average

Uses the average sales from the previous three months.

## Evaluation Metrics

The forecasting methods were evaluated using:

- MAE — Mean Absolute Error
- RMSE — Root Mean Squared Error
- MAPE — Mean Absolute Percentage Error

## Results

| Model | MAE | RMSE | MAPE |
|---|---:|---:|---:|
| Naive | $10,890.42 | $16,169.73 | 11.90% |
| Seasonal Naive | $4,815.83 | $5,329.12 | 4.83% |
| 3-Month Moving Average | $13,194.31 | $16,621.83 | 13.99% |

## Best Baseline

Seasonal Naive produced the strongest overall forecasting performance.

Its MAE of approximately $4,816 means that monthly forecasts differed from actual sales by about $4,816 on average during the test period.

## Key Findings

- Seasonal Naive produced the lowest MAE, RMSE, and MAPE.
- Annual seasonality was an important pattern in the sales data.
- The Seasonal Naive forecast followed seasonal peaks more closely than the other baseline methods.
- The 3-Month Moving Average smoothed short-term variation but missed important seasonal peaks.
- A more advanced forecasting model should outperform the Seasonal Naive baseline before its additional complexity is justified.

## Limitation

Seasonal Naive assumes that seasonal patterns repeat from one year to the next.

It may not adapt well to:

- Structural changes
- Promotions
- Unusual events
- Sudden changes in consumer behaviour

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Time Series Analysis
- Forecast Evaluation
- Jupyter Notebook

## Notebook

The complete analysis is available in:

`Baseline_Timeseries_Forecasting.ipynb`

## Portfolio

This project is part of my Data Science portfolio:

https://flortr3.github.io/
