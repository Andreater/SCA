# SCA
Supply Chain Analytics (SCA) is a forecast project where we used real world data to predict the demand of each SKU in the next 10 days. A docker image of this project was deployed for each warehouse to help reduce burden on logistics. The aim of the project was two-folded: automatically scale the stock replenishment based on the demand and reduce the lead-time in deliveries for customers.

## About forecasting
We used a core pack of 12 forecasting model based on AI/ML. Each day 2 years of data are used for retraining, and the last seven days are used for hold out cross-validation. Then we select a best-fitting model based on RMSE and forecast error and refit data to obtain forecasts in a 10 days horizon. Seasonality is computed by decomposing the time series using a Fourier transform, then it is automatically fitted as predictor. Currently, the project does not support other exogenous features.

## Disclaimer
To avoid data leaks I'm not sharing any code or config file with sensible informations. This means that I'm not uploading data on db structure and variables, and all the data in the dashboard were pseudo-randomized or anonymized. This is the public repo for showcase purposes.
