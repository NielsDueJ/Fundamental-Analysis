# Fundamental Analysis README

This script performs fundamental analysis on a specified stock ticker using various financial data and visualization techniques. The script leverages data from Yahoo Finance, Financial Modeling Prep, and NewsAPI to provide a comprehensive overview of the company's financial health, recent performance, and relevant news. Below is a description of the key functionalities of the script. I do not rely on fundamentals when I invest, but they are interesting to look at.

### Importing Necessary Packages

The script begins by importing essential packages such as `yfinance`, `matplotlib`, `seaborn`, `pandas`, and others required for data fetching, manipulation, and visualization.

### Suppressing Warning Messages

To keep the output clean, the script suppresses future warning messages.

### Fetching Competitors

The function `get_competitors(ticker, fmp_api_key)` retrieves a list of competitor companies within the same industry using the Financial Modeling Prep API. It fetches the sector and industry information for the given ticker from Yahoo Finance and then retrieves competitors based on the industry.

### Financial Ratios Calculation

The function `get_financial_ratios(ticker)` fetches the financial data of the specified ticker from Yahoo Finance and calculates key financial ratios:
- P/E Ratio
- Operating Cash Flow
- Free Cash Flow
- EBITDA

These ratios provide insights into the company's profitability, liquidity, and cash flow situation.

### Plotting Historical Stock Prices

Two types of charts are generated to visualize historical stock prices:
1. **Moving Average and Bollinger Bands**: `plot_moving_avg_bollinger(hist, ticker)` plots the closing prices along with 20-day moving average and Bollinger Bands, helping to analyze stock price trends and volatility.
2. **Candlestick Chart**: `plot_candlestick(hist, ticker)` creates a candlestick chart to represent daily price movements, useful for technical analysis.

### Fetching Latest News

The function `get_latest_news(ticker, news_api_key)` uses the NewsAPI to fetch the latest news articles related to the specified ticker. It retrieves the top 5 relevant articles to provide the latest updates and market sentiment about the company.

### Comparing Financial Ratios with Peers

The function `compare_with_peers(ticker, fmp_api_key)` compares the financial ratios of the specified company with its peers. It retrieves competitor data and their respective financial ratios, allowing for a comparative analysis.

### Performing the Analysis

The main function `perform_analysis(ticker, fmp_api_key, news_api_key)` orchestrates the entire analysis by:
1. Fetching and displaying financial ratios.
2. Plotting historical stock prices with moving averages and Bollinger Bands.
3. Generating a candlestick chart.
4. Printing the latest news articles.
5. Comparing the company's financial ratios with those of its peers.

### Usage

To perform the analysis, the script requires:
- A stock ticker symbol (e.g., "AAPL" for Apple Inc.).
- API keys for Financial Modeling Prep and NewsAPI.

Replace the placeholder values for the API keys and the ticker symbol, and call the `perform_analysis` function with the required parameters to execute the analysis.
