# Defensive-Alpha: Systematic Low-Volatility Momentum

A systematic equity trading strategy designed for the NSE 200 universe.

## Overview
This strategy implements a **Defensive Smart Beta** approach to equity trading. It focuses on identifying stable, upward-trending assets within the Indian market to generate consistent returns while minimizing portfolio variance.

---

## Strategy Logic
The model follows a four-step selection and weighting process:

1.  **Universe Filtering**: The strategy targets the **Top 200 stocks** by Market Capitalization to ensure high liquidity.
2.  **Trend Filter (Momentum)**: Only stocks trading above their **50-day Simple Moving Average (SMA)** are eligible for selection.
3.  **Volatility Selection**: From the filtered list, the **30 stocks with the lowest 3-month rolling volatility** are selected.
4.  **Portfolio Weighting**: Capital is allocated using an **Inverse-Volatility** approach, giving higher weights to the most stable assets.

---

## Technical Details
* **Rebalancing**: The portfolio is rebalanced on a **monthly basis**.
* **Transaction Costs**: Accounts for a **0.268% friction** (including brokerage, STT, and slippage) on every trade.
* **Execution Logic**: Implements **T+1 execution** and integer-only share constraints to reflect real-market conditions.
* **Initial Capital**: ₹50,00,000.

---

## Performance
* **Compound Annual Growth Rate (CAGR)**: ~9.48%.

---

## Dependencies
The implementation is written in Python and requires the following libraries:
* `pandas`
* `numpy`
* `matplotlib`

## Usage
To run the strategy and view the equity curve, execute the `volatility_strat.ipynb` notebook. Ensure your data file (`nse_final.csv`) is in the same directory as the script.
