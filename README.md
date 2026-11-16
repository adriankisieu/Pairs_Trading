# Pairs_Trading
Pairs trading strategy using 1-minute stock data, cointegration, and z-score mean reversion with backtesting and risk management.

# Pairs Trading Strategy

A quantitative pairs trading strategy using 1-minute historical stock data to identify and trade mean-reversion opportunities.

## Overview

The strategy analyzes eight stock pairs using cointegration and rolling z-scores to identify significant price divergences. It opens market-neutral-style long-short positions when spreads deviate from their historical relationships and exits when they revert toward the mean or trigger a stop-loss.

## Strategy

- **Data:** Databento 1-minute OHLCV data
- **Entry:** Spread z-score reaches ±3.0
- **Take profit:** Z-score returns to ±0.25
- **Stop-loss:** Z-score reaches ±4.5 or the hard-loss threshold
- **Model:** 252-day training window, retrained quarterly
- **Holding period:** No fixed limit; overnight positions allowed

## Backtesting

The notebook includes historical backtesting with modeled transaction costs, slippage, commissions, and short borrowing costs.

It also includes leverage sensitivity testing, portfolio performance analysis, and comparisons of rolling z-score calculations.

## Technologies

Python, Pandas, NumPy, Statsmodels, Matplotlib, Databento

## Limitations

Results are based on historical simulations. Execution costs are estimated, and dividends, corporate actions, and margin requirements are not fully modeled.

**For research and educational purposes only. No live trading.**
