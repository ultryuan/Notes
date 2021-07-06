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

# Long-Short-Term Memory (LSTM)
LSTM is a form of RNN recurrent neural networks.

As opposed to the feed forward network. RNN remembers the past
![[Pasted image 20210623150459.png]]

LSTM has forget gate, input gate and output gate
![[Pasted image 20210623151803.png]]

![[Pasted image 20210623151820.png]]

## In Keras

``` python
from keras.layers import LSTM
from keras.models import Sequential

model = Sequential()

model.add(LSTM(units=50, return_sequences=True, input_shape=(X_train.shape[1], 1)))
model.add(Dropout(0.2))
```
units: how many units of LSTM you want in the layer? (perhaps memory slots? how many previous data in the sequence to take into account?)
![[Pasted image 20210623152027.png]]

## Bidirectional LSTM
to do 
## ConvLSTM
to do 
