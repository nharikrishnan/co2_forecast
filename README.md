# Forecasting atmospheric co2 levels
The CO2 levels dataset in statsmodels contains records of atmospheric carbon dioxide measured directly from continuous Air Samples at Mauna Lao Observatory, Hawaii, USA from 1952 to 2014.<br>
The notebooks provided, gives an overview of how forecasting is done using the following method:
1. Holt-winters exponential smoothing
2. Arima
3. SARIMA

### Holt-winter(triple exponential smoothing)
Holt-winter exponential smoothing is a powerful forecasting method that can be used when the time series has both trend and seasonal components. There are 2 variations of holt-winters, one is the Additive method and the other one is the Multiplicative method.

In holt-winter forecasting, exponential smoothing is applied to the trend component, seasonal component and the level. Finally the forecast could be a additive or multiplicative.
If you want to know more about the mathematical part behind holt-winters, I highly recommend going through this <a href = https://grisha.org/blog/2016/01/29/triple-exponential-smoothing-forecasting> https://grisha.org/blog/2016/01/29/triple-exponential-smoothing-forecasting/</a>

### Arima(Auto regressive integrated moving average)
Arima model forecasts based on the auto-correlation in the data. It is combined of 3 parts, and 3 parameter one for each part:
1. Auto regressive
2. integrated(differencing)
2. Moving average

The differencing is done to make the time series stationary. The autoregressive term and moving average term can be found using ACF and PACF plots. After fitting the model, a residual analysis can be performed to tune the parameters.

### Seasonal SARIMA(Seasonal autoregressive integrated moving average model)
SARIMA is an extenstion of the normal ARIMA model, with a seasonal component. There are six parameter for seasonal arima, order(p, d, q) and seasonal order(P, D, Q).
These parameters can be found, similar to how it's done for ARIMA
