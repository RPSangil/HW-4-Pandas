# HW-4-Pandas
**Unit 4 - A Whale Off the Port(folio)**

## Table of Contents
- [The Scenario](#The-Scenario)
- [Navigating the GitHub](#Navigating-the-GitHub)
- [Important Notice](#Important-Notice)
- [Quantative Analysis](#Introduction)
    * [Performance](#Performance)
    * [Risk Analysis](#risk-analysis)
        * [Rolling Statistics](#rolling-statistics)
    * [Sharpe Ratios](#sharpe-ratios)
- [Reference List](#Reference-List)

## The Scenario

Harold's company has been investing in algorithmic trading strategies. Some of the investment managers love them, some hate them, but they all think their way is best.

You just learned these quantitative analysis techniques with Python and Pandas, so Harold has come to you with a challenge—to help him determine which portfolio is performing the best across multiple areas: volatility, returns, risk, and Sharpe ratios.

You need to create a tool (an analysis notebook) that analyzes and visualizes the major metrics of the portfolios across all of these areas, and determine which portfolio outperformed the others. You will be given the historical daily returns of several portfolios: some from the firm's algorithmic portfolios, some that represent the portfolios of famous "whale" investors like Warren Buffett, and some from the big hedge and mutual funds. You will then use this analysis to create a custom portfolio of stocks and compare its performance to that of the other portfolios, as well as the larger market (S&P 500 Index).

[Back to Table of Contents](#Table-of-Contents)

## Navigating the GitHub

In the Images folder, you will find a collection of the plots made using the code.

The following was provided at the beginging of the assessment and can be found in the Starter_code folder:

- [Whale Analysis Starter Notebook](https://github.com/RaelynSangil/HW-4-Pandas/blob/cd27f814bbf8a07f856ce0acc4ae6bda3f37f7f4/Starter_Code/whale_analysis.ipynb) - Starter code given.
- [Resources](https://github.com/RaelynSangil/HW-4-Pandas/tree/main/Starter_Code/Resources) - Resources given for analysis.

In the Worked_Code folder you will find:

- [Whale Analysis](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Worked_Code/whale_analysis.ipynb) - Contains images of all the plots created in the ipynb files.
- [Resources](https://github.com/RaelynSangil/HW-4-Pandas/tree/main/Starter_Code/Resources) - Resources given for analysis.

[Back to Table of Contents](#Table-of-Contents)

## Important Notice

1. Please view this github in `Day Theme - Light Default` so that headers and axises on the plots show.

[Back to Table of Contents](#Table-of-Contents)

## Quantative Analysis

This section performance and risk has been visualised.

### Performance

Below are the Daily Returns for each portfolio.

<ins> Daily Returns: Whale </ins>
![Daily Returns: Whale](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Daily_Returns_Whale.png)

<ins> Daily Returns: Algorithms </ins>
![Daily Returns: Algorithms](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Daily_Returns_Algorithms.png)

<ins> Daily Returns: S&P 500 </ins>
![Daily Returns: S&P 500](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Daily_Returns_S&P500.png)

<ins> Daily Returns: Combined </ins>
![Daily Returns: Combined](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Daily_Returns_Combined.png)

Below are the Cumulative Returns for each portfolio.

<ins> Cumulative Returns: Whale </ins>
![Cumulative Returns: Whale](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Cumulative_Returns_Whale.png)

<ins> Cumulative Returns: Algorithms </ins>
![Cumulative Returns: Algorithms](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Daily_Returns_Algorithms.png)

<ins> Cumulative Returns: S&P 500 </ins>
![Cumulative Returns: S&P 500](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Cumulative_Returns_S&P500.png)

<ins> Cumulative Returns: Combined </ins>
![Cumulative Returns: Combined](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Cumulative_Returns_Combined.png)

### Risk Analysis

<ins> Risk Distribution: Whale </ins>
![Risk Distribution: Whale](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Risk_Distribution_Whale.png)

<ins> Risk Distribution: Algorithms </ins>
![Risk Distribution: Algorithms](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Risk_Distribution_Algorithms.png)

<ins> Risk Distribution: S&P 500 </ins>
![Risk Distribution: S&P 500](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Risk_Distribution_S&P500.png)

The portfolios with a higher standard deviation of the S&P 500 (0.00857) are riskier. Therefore, Algo 1, Algo 2, SOROS FUND MANAGEMENT LLC, TIGER GLOBAL MANAGEMENT LLC and BERKSHIRE HATHAWAY INC are riskier investments.

#### Rolling Statistics

Risk can change over time. The below section visualises a risk with varying windows.

<ins> Rolling Standard Deviation: Combined (21 day window) </ins>
![Rolling Standard Deviation: Combined (21 day window)](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Rolling_Standard_Deviation_Combined-21%20day%20window.png)

<ins> Beta Trend </ins>
![Beta Trend](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/Beta_Trend.png)

An alternative way to calculate a rolling window is to take the exponentially weighted moving average. This is like a moving window average, but it assigns greater importance to more recent observations.

<ins> EWM: Combined </ins>
![EWM: Combined ](https://github.com/RPSangil/HW-4-Pandas/blob/183c616a74d84ee578739180e8b48d7b80abf065/Images/EWM_Combined.png)

### Sharpe Ratios

In reality, investment managers and thier institutional investors look at the ratio of return-to-risk, and not just returns alone. Sharpe Ratio is used to help investors understand the return of an investment compared to its risk. The ratio is the average return earned in excess of the risk-free rate per unit of volatility or total risk. Volatility is a measure of the price fluctuations of an asset or portfolio.

- The Sharpe ratio adjusts a portfolio’s past performance—or expected future performance—for the excess risk that was taken by the investor.
- A high Sharpe ratio is good when compared to similar portfolios or funds with lower returns.
- The Sharpe ratio has several weaknesses, including an assumption that investment returns are normally distributed. [<sup>1</sup>](#reference-list)

<ins> Sharpe Ratios </ins>
![Sharpe Ratios](https://github.com/RPSangil/HW-4-Pandas/blob/548c15d1396c72ed46b044c9316988fe7c1c5613/Images/Sharpe_Ratios.PNG)

The Algorithmic strategies have overall better risk measures than the other portfolios. Looking at returns, Algo 1 had the well out performed the others. Overall, the algorithmic strategies did outperform the other portfolios.

[Back to Table of Contents](#Table-of-Contents)

# Reference List
- [<sup>1</sup> https://www.investopedia.com/terms/s/sharperatio.asp](https://www.investopedia.com/terms/s/sharperatio.asp)

[Back to Table of Contents](#Table-of-Contents)