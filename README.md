# Backtesting Framework

## Overview
This framework is designed for backtesting trading strategies. It computes strategy returns, applies transaction costs, and evaluates key performance metrics like Sharpe Ratio, Sortino Ratio, and Volatility. The framework also visualizes cumulative returns for the strategy and the underlying asset.

---

## Key Features
1. **Position-Based Strategy Returns**:
   - Calculates returns based on positions and underlying asset price changes.
   - Includes a configurable lag to avoid lookahead bias.

2. **Transaction Costs**:
   - Deducts transaction costs (configurable percentage) based on position changes.

3. **Performance Metrics**:
   - **Whole Period Metrics**:
     - Sharpe Ratio
     - Sortino Ratio
     - Volatility
   - **Rolling Metrics**:
     - Rolling Sharpe Ratio
     - Rolling Sortino Ratio
     - Rolling Volatility

4. **Visualization**:
   - Plots cumulative returns for both the strategy and the underlying asset.

---

## Project Structure
- **main.py**: Entry point for the framework.
- **utils.py**: Contains core functions for data validation, return calculations, performance metrics, and plotting.
- **config.py**: Centralized configuration file for all essential parameters.

---

## Usage
1. Prepare your input data as a DataFrame with the following columns:
   - `Date`: The date for each observation (YYYY-MM-DD format).
   - `Price`: The price of the underlying asset.
   - `Position`: The position size (float) indicating the strategy's exposure.

2. Update the `CONFIG` file as needed:
   - `date_format`: Format of the date column (default is `%Y-%m-%d`).
   - `lag`: Number of periods to lag positions (default is `1`).
   - `transaction_cost`: Transaction costs as a percentage (default is `0.001`).
   - `rolling_window`: Rolling window size for performance metrics (default is `20`).

3. Run `main.py` to execute the backtest and view the results:
   - Strategy returns and transaction costs.
   - Whole period and rolling performance metrics.
   - A plot of cumulative returns.

---
