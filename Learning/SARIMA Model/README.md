# Seasonal Autoregressive Integrated Moving Average (SARIMA) Model

Autoregressive Integrated Moving Average, or ARIMA, is one of the most widely used forecasting methods for univariate time series data forecasting.

Although the method can handle data with a trend, it does not support time series with a seasonal component.

An extension to ARIMA that supports the direct modeling of the seasonal component of the series is called **SARIMA**.

***Seasonal Autoregressive Integrated Moving Average***, ***SARIMA*** or ***Seasonal ARIMA***, is an extension of ARIMA that explicitly supports univariate time series data with a seasonal component.

It adds three new hyperparameters to specify the *autoregression (AR)*, *differencing (I)* and *moving average (MA)* for the seasonal component of the series, as well as an additional parameter for the period of the seasonality. It is written as follows:

`ARIMA (p,d,q) (P,D,Q)`<sub>`m`</sub>

where `(p,d,q)` = Non-seasonal(or trends) part of the model

`(P,D,Q)` = Seasonal part of the model

and <sub>`m`</sub> = number of time steps for a single seasonal period.

The seasonal part of the model consists of terms that are similar to the non-seasonal components of the model, but involve backshifts of the seasonal period. 

For example, an ARIMA `(1,1,1)(1,1,1)`<sub>`4`</sub> model (without a constant) is for quarterly data (m = 4), and can be written as
    
`(1−ϕ`<sub>`1`</sub>`B) (1−Φ`<sub>`1`</sub>`B`<sup>`4`</sup>`)(1−B)(1−B`<sup>`4`</sup>`)y`<sub>`t`</sub>` = (1+θ`<sub>`1`</sub>`B) (1+Θ`<sub>`1`</sub>`B`<sup>`4`</sup>`)ε`<sub>`t`</sub>.

The additional seasonal terms are simply multiplied by the non-seasonal terms.