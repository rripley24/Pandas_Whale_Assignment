# Whale Portfolio

### Rich Ripley

---

![Stock Portfolio](https://www.usnews.com/dims4/USNEWS/1df4729/2147483647/thumbnail/970x647/quality/85/?url=http%3A%2F%2Fmedia.beam.usnews.com%2Fc1%2F9c%2Faba74afe4d5abd5830e3b4548f3d%2F160506-investing-stock.jpg)


## Background

The investment division of Harold's company has been investing in algorithmic trading strategies. Some of the investment managers love them, some hate them, but they all think their way is best.

You just learned these quantitative analysis techniques with Python and Pandas, so Harold has come to you with a challenge—to help him determine which portfolio is performing the best across many areas: volatility, returns, risk, and Sharpe ratios.

You will need to create a tool (an analysis notebook) that analyzes and visualizes the major metrics of the portfolios across all of these areas, and determine which portfolio outperformed the others. You will be given the historical daily returns of several portfolios: some from the firm's algorithmic portfolios, some that represent the portfolios of famous "whale" investors like Warren Buffett, and some from the big hedge and mutual funds. You will then use this analysis to create a custom portfolio of stocks and compare its performance to that of the other portfolios, as well as the larger market (S&P 500).


## Tasks:

1 - Read in returns data

2 - Determine Success of each portfolio 

3 - Choose and evaluate a custom Portfolio


## Read in Data:

First, read and clean several CSV files for analysis. The CSV files include whale portfolio returns, algorithmic trading portfolio returns, and S&P 500 historical prices. Use the Whale Analysis Starter Code to complete the following steps:

Use Pandas to read in each of the CSV files as a DataFrame. Be sure to convert the dates to a DateTimeIndex.

Detect and remove null values.

Remove dollar signs from the numeric values and convert the data types as needed.

The whale portfolios and algorithmic portfolio CSV files contain daily returns, but the S&P 500 CSV file contains closing prices. Convert the S&P 500 closing prices to daily returns.

Join Whale Returns, Algorithmic Returns, and the S&P 500 Returns into a single DataFrame with columns for each portfolio's returns.

## Conduct Quantitative Analysis

Analyze the data to see if any of the portfolios outperform the stock market (i.e., the S&P 500).

### Performance Analysis

Calculate and plot cumulative returns. Does any portfolio outperform the S&P 500?
Risk Analysis

Create a box plot for each of the returns. Which box has the largest spread? Which has the smallest spread?

Calculate the standard deviation for each portfolio. Which portfolios are riskier than the S&P 500?

Calculate the annualized standard deviation (252 trading days).

### Rolling Statistics

Plot the rolling standard deviation of the various portfolios along with the rolling standard deviation of the S&P 500 using a 21 day rolling window. Does the risk increase for each of the portfolios at the same time risk increases in the S&P?

Construct a correlation table for the algorithmic, whale, and S&P 500 returns. Which returns most closely mimic the S&P?

Choose one portfolio and plot a rolling beta between that portfolio's returns and S&P 500 returns. Does the portfolio seem sensitive to movements in the S&P 500?

An alternative way to calculate a rolling window is to take the exponentially weighted moving average. This is like a moving window average, but it assigns greater importance to more recent observations. Try calculating the ewm with a 21 day half-life.

### Plot Sharpe Ratios

Investment managers and their institutional investors look at the return-to-risk ratio, not just the returns. (After all, if you have two portfolios that each offer a 10% return, yet one is lower risk, you would invest in the lower-risk portfolio, right?)

Using the daily returns, calculate and visualize the Sharpe ratios using a bar plot.

Determine whether the algorithmic strategies outperform both the market (S&P 500) and the whales portfolios.

### Create Custom Portfolio

Harold is ecstatic that you were able to help him prove that the algorithmic trading portfolios are doing so well compared to the market and whales' portfolios. However, now you are wondering whether you can choose your own portfolio that performs just as well as the algorithmic portfolios. Investigate by doing the following:

Visit Google Sheets and use the in-built Google Finance function to choose 3-5 stocks for your own portfolio (we chose: NVDA, TSLA, NFLX). 

Download the data as CSV files and calculate the portfolio returns.

Calculate the returns for each stock.

Using those returns, calculate the weighted returns for your entire portfolio assuming an equal number of shares for each stock.

Add your portfolio returns to the DataFrame with the other portfolios and rerun the analysis. How does your portfolio fair?

## Conclusion: 

Judging by the sharpe ratio graph, it appears that the best performing assets (for risk) are NFLX, NVDA, the Algo 1 portfolio, and Berkshire Hathaway. TSLA is still a very volatile option, but does perform better than some of the other funds and the S&P 500. Inevitably, top performers will change over time, and these charts will be worth monitoring moving forward. 