# Multi-timeframe Backtest Comparison VectorBt And Backtrader-
Multi-time-frame Backtest Comparison VectorBt And Backtrader 
## Backtest Strategy

This is a multi-timeframe moving average crossover strategy

We use 3 Timeframes data:
1. Timeframe 0: 1 min close data
2. Timeframe 1: 5 min close data
3. Timeframe 2: 15 min close data

Further, we use 3 moving averages in all three timeframes:
1. Fast SMA
2. Medium SMA
3. Slow SMA

Entry and Exit Conditions
*   Long Trades
  *   Entry Conditions:
      *   If in time frame 2, fast_sma > medium_sma > slow_sma and 
      *   In time frame 1, fast_sma > medium_sma > slow_sma
      *   In time frame 0, fast_sma > medium_sma > slow_sma
  *   Exit Conditions:
      *   In time frame 1, fast_sma crosses below medium_sma 
*   Short Trades
  *   Entry Conditions:
      *   If in time frame 2, fast_sma < medium_sma < slow_sma and 
      *   In time frame 1, fast_sma < medium_sma < slow_sma
      *   In time frame 0, fast_sma < medium_sma < slow_sma
  *   Exit Conditions:
      *   In time frame 1, fast_sma crosses above medium_sma 

