# House Prices Prediction
> 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges you to predict the final price of each home.

## Content
* [Target](#Target)
* [Steps](#Steps)
* [Final result](#Final-result)
* [Output](#Output)

## Target
**Train the model to predict the final price of each home.**

## Steps
- pre-processing is done (duplicates, missing values, types of data)
- Models were trained and predicted with default parameters and additionally using different sets of hyperparameters.
- the best model was selected based on the results of the RMSE metric

## Final result
| Regressors          | RMSE_mean | RMSE_std |
|---------------------|:---------:|:--------:|
| Linear_Reg.         |  0.134931 | 0.031700 |
| Bayesian_Ridge_Reg. |  0.125599 | 0.024922 |
| LGBM_Reg.           |  0.131588 | 0.020140 |
| SVR                 |  0.278757 | 0.022400 |
| Dec_Tree_Reg.       |  0.205279 | 0.028678 |
| Random_Forest_Reg.  |  0.139848 | 0.023283 |
| XGB_Reg.            |  0.130372 | 0.018754 |
| Grad_Boost_Reg.     |  0.128550 | 0.019008 |
| Cat_Boost_Reg.      |  0.118256 | 0.018838 |
| Stacked_Reg.        |  0.118947 | 0.020697 |

## Conclusion
The best model Cat Boost.
On test get 0.12
Top 13% submission

