# Auto Regressive Model
AutoRegressive model is a linear model which can predict something based on past values of the same thing.

It is based on the idea that current value of the series, Xt , 
can be explained as a linear combination of p past values, Xt−1, Xt−2, . . . , Xt−p, together with a random error in the same series. AR(p), is of the form,

<b><i> Xt = φ1Xt−1 + φ2Xt−2 + · · · + φpXt−p + 𝜀 </i></b>

where Xt is <b>stationary</b> (whose statistical properties such as mean, autocorrelation etc are all constant over time) and φ1, φ2, . . . , φp (φp can not be zero) are model parameters.
The hyperparameter p represents the length of the <b>“direct look back”</b> in the series and 𝜀 is the white noise.

## More Insights

Here, Xt is the value of the variable X, for which we want our prediction at the time t (current time).So, Xt depends on Xt-1,the previous time period.Again, Xt-1 depends on Xt-2 
and it goes down to Xt-p. This is how we predict the value of Xt based on previous values of it.

For an example, stock price for today will depend on the stock price of yesterday & will continue according to autoregression process & based on those values we will be able to do 
some precised predictions.
