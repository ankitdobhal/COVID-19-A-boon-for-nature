# Moving Average Model #

A moving average model is used for forecasting future values. Rather than using past values of the forecast variable in a regression, it uses the past forecast errors in a regression like model.

X<sub>t</sub> = Z<sub>t</sub> + θ<sub>1</sub>Z<sub>t-1</sub> + θ<sub>2</sub>Z<sub>t-2</sub> + ... + \Theta<sub>q</sub>Z<sub>t-q</sub>

where Z<sub>t</sub> is the noise. 

We refer this as an MA(q) model, a Moving Average model of order q.

## Example ##
Let's take an example of stock price of a company. X<sub>t</sub> is stock price of the company. Each daily announcement of the company is modelled as a noise. And let’s say these announcements are effecting the stock price and effect of the daily announcements (noises Z<sub>t</sub>) on the stock price(X<sub>t</sub>) might last 2 days.

Stock price is a linear combination of the noises that affects it.

X<sub>t</sub> = Z<sub>t</sub> + θ<sub>1</sub>Z<sub>t-1</sub> + θ<sub>2</sub>Z<sub>t-2</sub>


θ<sub>1</sub>, θ<sub>2</sub> = Weights of the announcements from yesterday and the day before.
This is a Moving Average Model of order 2 - MA(2)