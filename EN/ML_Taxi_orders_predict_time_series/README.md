# Forecasting taxi orders
> Based on historical data, build a model for a taxi company that can predict demand for the next hour. The company's goal is to plan for the need to attract additional drivers.

## Content
* [Target](#Target)
* [Steps](#Steps)
* [Libraries](#Libraries)
* [Final result](#Final-result)
* [Output](#Output)

## Target
**Train a model to predict a taxi for the next hour**

## Steps
- checked the missing values, duplicates
- analysis was carried out to determine trends by hours during the day and by day
- trained and predicted models with default parameters and additionally using different sets of hyperparameters
- the best model was selected according to the results of the RMSE metric

## Libraries
- Models: CatBoostRegressor, LinearRegression, RandomForestRegressor
- matplotlib, seaborn, pandas, sklearn, numpy, statsmodels

## Final result
| Model | RMSE |
|:--------------------------------:|:---------:|
| Linear Regression | 30.716686 |
| RandomForestRegressor | 32.326298 |
| RandomForestRegressor_tuned | 31.329871 |
| CatBoostRegressor | 30.226653 |
| CatBoostRegressor_tuned | 30.651896 |
| CatBoostRegressor_test | 46.718390 |
| LinearRegression_test | 41.740070 |

## Conclusion
LinearRegression The best model with an RMSE score of 41 on the test set, a score below the target of 48.
Based on this, the general recommendation is:
To solve the problem of predicting the demand for a taxi an hour ahead, use the LinearRegression model.
