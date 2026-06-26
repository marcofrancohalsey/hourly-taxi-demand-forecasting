# Taxi demand forecasting using Machine Learning

### Overview

This project develops a machine learning model to forecast taxi demand for the next hour using historical airport taxi request data. The objective is to help Sweet Lift Taxi anticipate periods of high demand and attract more drivers when needed. Root Mean Squared Error (RMSE) is used as the evaluation metric, with a target of keeping the test RMSE below 48.

### Data

The dataset consists of historical taxi requests recorded every 10 minutes. The time series is aggregated into one hour intervals, and time based features are created using the hour of the day, the day of the week, and lag variables to capture daily and weekly demand patterns.

### Methodology

- Aggregate the time series into one hour intervals.
- Perform exploratory time series analysis to identify trends, seasonality, and recurring patterns.
- Create time based features, including hourly, weekly, and lag features.
- Train and compare Linear Regression, Random Forest, LightGBM, and CatBoost regression models.
- Select the final model based on test RMSE.

### Results

- The exploratory analysis identified a recurring weekly demand pattern, leading to the inclusion of a 168 hour lag feature that improved model performance.
- Linear Regression achieved the best generalization performance with a validation RMSE of 31.10 and a test RMSE of 34.94, outperforming all tree based models.
- The final model reduced the prediction error by between 8.92 and 12.47 taxi orders per hour compared with Random Forest, LightGBM, and CatBoost.
- The final RMSE of 34.94 was 27.2% below the required threshold of 48.

### Tools

Python, Pandas, NumPy, Matplotlib, Statsmodels, scikit-learn, LightGBM, CatBoost