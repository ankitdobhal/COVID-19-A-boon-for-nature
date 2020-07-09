# Augmented Dickey-Fuller Test

When performing time series analysis, most statistical forecasting methods assume that the time series is approximately stationaryThe Augmented Dickey-Fuller Test is a well known
statistical test that can help determine if your time series is stationary. 

## Stationary Vs Non Stationary Time Series

In a stationary time series, statistical properties such as mean and variance are constant over time. In a non-stationary series, these properties are dependent on time.

## ADF-Test

The Augmented Dickey-Fuller test is a type of statistical test called a <b>unit root test</b>.Unit roots are a cause for non-stationarity, the ADF test will test if unit root 
is present.

> A time series is stationary if a single shift in time doesn’t change the time series statistical properties, in which case unit root does not exist.

The Null and Alternate hypothesis of the Augmented Dickey-Fuller test is defined as follows:

* Null Hypothesis states there is the presence of a unit root.
* Alternate Hypothesis states there is no unit root. In other words, Stationarity exists.
 
We interpret the result using the <b>p-value</b> from the test. A p-value below a threshold (such as 5% or 1%) suggests we reject the null hypothesis (stationary), otherwise a p-value 
above the threshold suggests we fail to reject the null hypothesis (non-stationary).

* <b> p-value > 0.05 </b> : Fail to reject the null hypothesis (H0), the data has a unit root and is <b>non-stationary</b>.
* <b> p-value <= 0.05 </b> : Reject the null hypothesis (H0), the data does not have a unit root and is <b>stationary</b>.
