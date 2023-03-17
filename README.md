# Simple-Analysis-of-ACF-and-PACF-plots
Simple Analysis of Calculation of AutoCorrelationFunction and Partial AutoCorrelationFunction with plots and code for the widely available datasets: AirPassangers.csv and daily-min-temperatures.csv

## What does this NoteBook contain ?
- Plots and reviews the partial autocorrelation function for a time series.
- Visualize the difference between autocorrelation and partial autocorrelation functions for time series analysis.

## ACF (Auto Correlation Function)
Auto Correlation function takes into consideration of all the past observations irrespective of its effect on the future or present time period. It calculates the correlation between the t and (t-k) time period. It includes all the lags or intervals between t and (t-k) time periods. Correlation is always calculated using the Pearson Correlation formula.

## PACF(Partial Correlation Function)
The PACF determines the partial correlation between time period t and t-k. It doesn’t take into consideration all the time lags between t and t-k. For e.g. let's assume that today's stock price may be dependent on 3 days prior stock price but it might not take into consideration yesterday's stock price closure. Hence we consider only the time lags having a direct impact on future time period by neglecting the insignificant time lags in between the two-time slots t and t-k.

### How to differentiate when to use ACF and PACF?
Let's take an example of **sweets sale and income generated in a village over a year.**
- Under the assumption that every 2 months there is a festival in the village, we take out
- the historical data of sweets sale and income generated for 12 months. 

If we plot the time (in months) then we can observe that when it comes to calculating the sweets sale we are
interested in only alternate months as the sale of sweets increases every two months. But
if we are to consider the income generated next month then we have to take into
consideration all the 12 months of last year.

So in the above situation, we will use ACF to find out the income generated in the future
but we will be using PACF to find out the sweets sold in the next month.

PACF = to find the sweets sold next month

ACF  = to find the income generated in future



#### Durbin-Watson test
The test gives an output ranging from 0 to 4. The autocorrelation will be

- Closer to 0: Stronger and positive
- Middle: Low
- Closer to 4: Negative

#### Ljung–Box test
It is also known as the modified Box-Pierce, Ljung–Box Q test, Box test, or Portmanteau
test. It tests for the absence of serial autocorrelation for a given lag “k.” In addition, it
tests for randomness and independence. If the autocorrelations of the residuals are very
small, the model is fine; that is, the model does not exhibit a significant lack of fit.
