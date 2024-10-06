# Portfolio Optimization - Markowitz Theory

## Introduction

This project demonstrates the application of **Markowitz's Modern Portfolio Theory** to optimize a portfolio of financial assets. The primary goal is to construct an **efficient frontier** of portfolios that maximizes return for a given level of risk. The project uses historical stock price data, computes the expected returns and covariance matrix of stock returns, simulates numerous portfolios, and identifies the portfolios on the efficient frontier.

## Features

- **Portfolio Simulation**: Generates random portfolio allocations and evaluates their performance in terms of expected returns, risk (volatility), and Sharpe ratio.
- **Efficient Frontier Construction**: Identifies portfolios that offer the maximum return for a given level of risk.
- **Portfolio Cumulative Return**: Calculates the cumulative returns of the selected portfolio over time and compares them to benchmark indexes (e.g., S&P 500, MSCI World).
- **Interactive Visualizations**: Uses Plotly to provide interactive plots for analyzing portfolio performance and the efficient frontier.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/portfolio-optimization.git
   ```
2. Install the required dependencies:
   ```bash
   pip install yfinance plotly mpld3 numpy pandas matplotlib
   ```

## Usage

1. **Load Historical Data**: The project downloads historical stock price data (including dividends) from Yahoo Finance using `yfinance`. You can modify the ticker list in the script to include different assets.
2. **Portfolio Simulation**: The script simulates 10,000 random portfolios and calculates their expected return, risk, and Sharpe ratio.
3. **Efficient Frontier**: The project identifies portfolios that lie on the efficient frontier and visualizes them interactively.
4. **Cumulative Return**: Users can select specific portfolio weights to compute and visualize the cumulative return of the portfolio compared to several indexes.

## Visualizations

- **Return vs. Risk**: Interactive scatter plot showing the relationship between risk and return for each simulated portfolio, color-coded by Sharpe ratio.
- **Efficient Frontier**: An interactive plot highlighting the portfolios on the efficient frontier.
- **Portfolio Performance Over Time**: Line chart comparing the cumulative returns of the selected portfolio to benchmark indexes (e.g., S&P 500, MSCI World, Gold, CAC40).

## Example

```python
ticker_list = ['RI.PA', 'SU.PA', 'OR.PA', 'AI.PA', 'MC.PA', 'CAP.PA', 'SW.PA', 'TTE.PA', 'GC=F', '^GSPC']
data = yf.download(ticker_list, start='2012-01-01', end='2024-05-31')['Close']
```

## Project Structure

- `portfolio_optimization.ipynb`: The main Jupyter notebook containing the code for portfolio optimization and visualization.
- `requirements.txt`: Lists all the dependencies required to run the project.

## References

- [Modern Portfolio Theory (Markowitz)](https://en.wikipedia.org/wiki/Modern_portfolio_theory)
- [yfinance](https://pypi.org/project/yfinance/)
- [Plotly](https://plotly.com/python/)

Feel free to fork and contribute to this project!