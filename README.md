# ML-For-Algorithmic-Trading

This strategy ranks three stocks in the portfolio to hold a long position in, and three stocks to hold a short position in every week.

This is for educational purposes only.

We implement this strategy on 20 US stocks.

These are the features used in training:
- 1, 5 and 20-day returns
- Price relative to 10 and 50 day moving average
- 14-day Relative Strength Index
- 20-day volatility
- 20-day volatility
- Volume relative to 20-day average
The features were standardised and ridge regression was applied to avoid overfitting.

The label is each stock's 5-day forward return minus the avaerage return of the portfolio. This removes the market's overall move, so the model only has to rank stocks against each other, not predict market direction.

How to run:
1. Create a new Python project on QuantConnect. (https://www.quantconnect.com)
2. Paste the contents of `main.py` into the project.
3. Set the backtest dates in `initialize` and run a backtest.
