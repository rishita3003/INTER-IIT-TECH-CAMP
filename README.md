# INTER-IIT-TECH-CAMP Project
The Quantitative Problem Statement (Quant PS) developed for the Inter IIT Tech Camp at IIT Guwahati focused on exploring and implementing the Pair Trading Strategy. This strategy is an integral part of statistical arbitrage and is widely utilized in quantitative finance due to its efficacy and theoretical backing.

## Overview
The INTER-IIT-TECH-CAMP project focuses on the Quantitative Problem Statement (Quant PS) released for the Inter IIT Tech Camp hosted by IIT Guwahati, emphasizing the Pair Trading Strategy. This strategy is a key component of financial engineering and quantitative finance.

## Key Concepts Implemented
This project involves practical implementations of various sophisticated concepts within the realm of statistical arbitrage. Here are some of the key areas covered:

- **Statistical Arbitrage**: Utilizing price inefficiencies between paired stocks to secure profits.
- **Kalman Filter**: A mathematical algorithm to estimate hidden states from inaccurate measurements, crucial for predicting stock price movements accurately.
- **CAGR (Compound Annual Growth Rate)**: Represents the mean annual growth rate of an investment over a specified time period, adjusted for compounding.
- **Z-Score**: A statistical measurement describing the number of standard deviations a data point is from the mean population.
- **Sharpe Ratio**: Indicates the average return minus the risk-free return divided by the standard deviation of return on an investment.
- **P-Value Comparisons**: Assess the strength of the evidence against the null hypothesis, helping in the validation of the stock pairs selected for trading.

## Practical Applications
The practical applications demonstrated in this project include:

- **Cointegration Comparison**: Analyzing different pairs of stocks to evaluate their cointegration, which is essential for identifying pairs most likely to revert to the mean.
- **Selection of Reliable Trading Pairs**: Using the statistical tools and concepts implemented to choose the best pairs that potentially reduce risk and increase profitability.

The repository includes Jupyter Notebooks that detail these implementations, providing a hands-on approach to learning and understanding these complex concepts.

## Pair Trading Strategy Implementation Pipeline
 **Step 1: Setup and data Retrieval :**
 '''bash
  !pip install yfinance pandas_ta pykalman
  import yfinance as yf
  import pandas as pd
  import matplotlib.pyplot as plt
  import seaborn as sns
  from pykalman import KalmanFilter
  from statsmodels.tsa.stattools import coint
  import warnings
  warnings.filterwarnings('ignore')

**Step 2: Load data :**
Load the data of the stocks from their stock tickers and download the data.

**Step 3: Visualize data**
The stock data is visualized to understand trends and behaviors of different stocks over time.

**Step 4: Identifying Cointegrated Pairs :**
Pairs of stocks that exhibit a statistical relationship are identified using the cointegration test. These stocks would then be used in the pairs trading strategy.

**Step 5: Kalman Filter Application :**
The Kalman Filter is used to estimate the hidden state of pairs and refine the trading signals.This is basically applied to make the signals more accurate by updating the hedge ratio from time to time and not assuming it to be static always.

**Step 6: Strategy Implementation and Backtesting :**
The trading strategy is implemented by generating signals based on the z-score of the spread between pairs and backtesting these signals to assess potential profitability.
Assigning -1 and +1 as the Z-scores and also marking the long and short positions of the stocks.

**Results Visualtion :**
The performance of the trading strategy is visualized to evaluate the effectiveness of pair trading.
  '''bash
  for result in results:
      plt.figure(figsize=(12, 6))
      plt.plot(result['cumulative returns'])
      plt.title('Cumulative Returns for Pair {}'.format(result['pair']))
      plt.show()


This pipeline encapsulates the complete workflow from data handling to final performance visualization, providing a robust framework for exploring and implementing Pair Trading strategies using Python and financial data APIs.
 
 

## Getting Involved
Contributions to this project are more than welcome. Feel free to fork the repository, make proposed changes, and submit pull requests. Let's collaborate to enhance this resource and help it grow!
