# Bayesian-Changepoint-Detection
Welcome! 

This project seeks to implement the online Bayesian changepoint detection algorithm, the top performer of the univariate time series changepoint algorithm discussed in this paper:https://arxiv.org/abs/2003.06222.

This algorithm is implemented and applied to two time series data originating from the data set, the first one is where the stock price closes each day, where we model the predictive distribution by a normal with unknown mean and known variance. The prior is chosen to be another normal distribution to use conjugacy and avoid performing numerical integration. The plot produced contains a confidence interval of estimation given the data set $x^{l}$, and the rough probability of where a changepoint is the most likely.

The second time series is the rate of change of stock prices, $close[i]/close[i-1] - 1$, this is referenced in the original paper (https://arxiv.org/abs/0710.3742) where the method is first proposed. This time series is modeled by picking predictive distribution to have mean 0 and unknown variance, whereas the inverse variance (precision) is set to have gamma prior. As in the previous case, a plot showing the most probable changepoints is provided.

This project, as well as some of the codes (especially parts on plotting and numerical stability）, is inspired by this series of blogs introducing the changepoint detection method as well as the example given using artificially generated data.


