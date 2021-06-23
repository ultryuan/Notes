# Random Stuff
__Time Series__: a series of data points indexed in time order.

In terms of intelligence: the before data is the input, the after data is the output.

Most traditional models require the time series to be __stationary__. 

__Stationary__: statistical properties such as mean, variance, and serial correlation are consatnt over time. 
![[Pasted image 20210622113217.png]]

## 3 approaches that I know of
__ARIMA__ good for data that shows non-stationarity
__Fully connected neural network__ regular deep learning 
__Recurrent Neural Networks RNN(LSTM)__ works well with sequences / timeseries.

# Tools
python libraries such as _statsmodels_ and _pmdarima_ can extract stationarity, trends, and seasonality from timeseries. 
# ARIMA
ARIMA is a model for time series forcasting. It is specified by three order parameters: p, d, q
__AR(_p_) Autoregression__ - use of the past values in the regression equation for the time series

__I(_d_) Integration__ - uses differencing observations (subtracting observations from observations from the previous time step) in order to make time series stationary.

__MA(_q_) Moving Average__ - depicts error of the model as a combination of previous error terms. The order q represents the number of terms to be include in the model. 

## ARIMA Flavors
ARIMA
__SARIMA__: seaonal ARIMA
__SARIMAX__: seasonal ARIMA with exogenous variables
__Pyramid Auto_ARIMA__: helps us to identify the most optimal parameters for an ARIMA model and returns a fitted ARIMA model.

## Sample Codes
### [Intro to time series exploring dataset using python](https://github.com/bnsreenu/python_for_microscopists/blob/master/162-Intro_to_time_series_exploring_dataset_using_python.py)
ARIMA, trend, seasonality. statsmodels

### [Using ARIMA](https://github.com/bnsreenu/python_for_microscopists/blob/master/163-Intro_to_time_series_Forecasting_using_ARIMA.py)
pmdarima
