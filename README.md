# sp500_prediction

Simple project of trying to recreate the movement of the S&P500 index.

As we know, S&P500 index is calculated as:

<a href="https://www.codecogs.com/eqnedit.php?latex=S\&P500&space;=&space;\sum_{ticker}{\frac{price_{ticker}&space;*&space;quantity_{ticker}}{divisor}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?S\&P500&space;=&space;\sum_{ticker}{\frac{price_{ticker}&space;*&space;quantity_{ticker}}{divisor}}" title="S\&P500 = \sum_{ticker}{\frac{price_{ticker} * quantity_{ticker}}{divisor}}" /></a>

## Problem description

Since the divisor is unknown, we tried to calculate the influence of every single ticker to the final projection.
First we used equal weights and later we tried calculating the weight as the ratio of the respective ticker's number of shares and the total number of shares.

Second approach gave us 25% better results when the squared errors are measured.

## Possible improvements

Since the list of the tickers used in the calculation of the SP500 index changes regularly, one can try finding the data of those changes for the respected intervals, 
and include that information in the calculation of weights, which would probably bring us even closer to the real S&P500 values.
