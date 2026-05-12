# Portfolio-Analysis-Engine

## Description
This project develops a comprehensive financial portfolio analysis engine using real-world stock market data. It focuses on understanding historical stock performance, assessing risk and return, optimizing portfolio allocations, and demonstrating the critical role of diversification. The analysis progresses from basic stock comparisons to advanced portfolio optimization techniques, including Sharpe Ratio analysis and correlation assessment, culminating in a robust, data-driven portfolio construction.

## Key Features
-   **Live Market Data Acquisition**: Downloads historical daily closing prices for selected stocks (AAPL, MSFT, GOOGL, AMZN, TSLA, JPM, JNJ) directly from Yahoo Finance using `yfinance`.
-   **Data Wrangling & Preprocessing**: Cleans and transforms raw price data into daily percentage returns, handling missing values.
-   **Volatility Analysis**: Measures and annualizes stock volatility (standard deviation of daily returns) to quantify risk.
-   **Sharpe Ratio Analysis**: Calculates the Sharpe Ratio for individual stocks and portfolios, providing a key metric for risk-adjusted returns.
-   **Portfolio Optimization**: Develops a data-driven approach to assign portfolio weights based on Sharpe Ratios, aiming to maximize risk-adjusted returns.
-   **Backtesting**: Compares portfolio performance across different time periods (e.g., 2022 vs. 2023) to highlight the importance of time-frame sensitivity.
-   **Correlation Analysis**: Examines how different stocks move in relation to each other using correlation matrices and heatmaps.
-   **Diversification Proof**: Demonstrates the benefits of diversification by comparing an all-tech portfolio against a diversified portfolio with stocks from different sectors (e.g., healthcare, banking).
-   **Professional Visualization**: Generates various charts including time series, bar plots, scatter plots, pie charts, and heatmaps to visualize key financial metrics and portfolio allocations.



## Key Findings & Insights
-   **Risk-Adjusted Returns**: Raw stock prices are misleading; daily returns and Sharpe Ratio provide a more accurate picture of performance relative to risk.
-   **Volatility as Risk**: Higher standard deviation of daily returns directly correlates with higher stock risk. Tesla was consistently identified as the most volatile stock.
-   **Sharpe Ratio is Key**: The Sharpe Ratio (`(Return - Risk Free Rate) / Volatility`) is crucial for evaluating whether a stock's return adequately compensates for its risk. A ratio above 1.0 is generally considered good.
-   **Time-Sensitivity of Models**: Portfolio optimization models are highly sensitive to the historical period used for training. A single good or bad year can drastically alter recommended allocations (e.g., Tesla's Sharpe Ratio flipped from highly negative in 2022 to positive in 2023).
-   **Benefits of Diversification**: Incorporating stocks with low or negative correlation (e.g., Johnson & Johnson from healthcare) significantly improves portfolio stability and risk-adjusted returns (Sharpe Ratio), demonstrating how diversification protects against sector-specific downturns.
-   **Portfolio Optimization**: Mathematically deriving weights based on Sharpe Ratios consistently led to portfolios with better risk-adjusted returns compared to arbitrary, 'gut-feeling' allocations.

## Future Work/Improvements
-   **Dynamic Time Windows**: Implement a rolling window analysis for Sharpe Ratio calculations to make the model more adaptive to recent market conditions without being overfit to a single year.
-   **Advanced Optimization**: Explore more sophisticated portfolio optimization techniques, such as Mean-Variance Optimization (Markowitz portfolio theory) to construct efficient frontiers.
-   **Risk Parity**: Investigate risk parity strategies where each asset contributes equally to the total portfolio risk.
-   **Inclusion of Other Asset Classes**: Expand the analysis to include bonds, commodities, or other financial instruments for broader diversification.
-   **Monte Carlo Simulations**: Use Monte Carlo simulations to model future portfolio performance and risk under various scenarios.
-   **API Integration**: Develop a more robust data pipeline for continuous data updates and real-time analysis.

## Technologies Used
-   Python
-   `yfinance` (for stock data)
-   `pandas` (for data manipulation and analysis)
-   `numpy` (for numerical operations)
-   `matplotlib` (for data visualization)
