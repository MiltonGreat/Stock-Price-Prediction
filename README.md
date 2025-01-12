# Stock Price Prediction Using LSTM

### Problem Statement

Predicting stock price movements is crucial for traders and investors seeking to optimize their trading strategies. However, transforming predictions into profitable strategies remains challenging due to market volatility, transaction costs, and unpredictable market fluctuations.

### Solution Approach

This project leverages a Long Short-Term Memory (LSTM) neural network to forecast stock price movements. The goal is to capture temporal dependencies within the stock price time series, specifically focusing on predicting PayPal (PYPL) stock price fluctuations.

### ## Dataset Information

The project uses the yfinance library to download historical stock price data for PayPal from January 1, 2015, to January 1, 2023, including:

- Open, high, low, close (OHLC) prices
- Trading volumes

### Methods

- Data Preprocessing: Prices are normalized using MinMaxScaler, and the dataset is split into training and testing sets.
- Model: An LSTM neural network is used to capture temporal dependencies and predict future stock prices.
- Performance Evaluation: The model is evaluated using Mean Squared Error (MSE) and Mean Absolute Error (MAE) to assess prediction accuracy.
- Backtesting Strategy: A basic trading strategy is simulated based on the model's predictions to assess profitability.

### Results

The LSTM model showed strong correlation between predicted and actual stock prices with minimal error rates.

Model Accuracy:

- Mean Absolute Error (MAE): 6.77 (average deviation from actual closing prices).
- R-squared (R²): 0.97 (indicating that the model explains 97% of the variance in stock prices).

Trading Strategy:

- The backtesting simulation showed a loss of approximately $118.62 from an initial balance of $10,000, highlighting the challenges of trading strategies based solely on price predictions.
- Despite accurate price predictions, the simplistic strategy failed to generate profits due to transaction costs and market noise.

### Key Insights

- LSTM Model Performance: The LSTM model is effective for predicting stock price trends, but additional optimizations are needed to ensure profitability in trading scenarios.

- Challenges in Trading Strategy: The backtesting results show that trading strategies based solely on price predictions may not be profitable without more refined strategies and proper risk management.

- Risk Management: This project highlights the importance of incorporating transaction costs and market volatility when developing a trading strategy.

### Evaluation Metrics

    MAE: The mean absolute error is approximately $6.77, meaning the model's predictions are, on average, $6.77 away from the actual closing prices.
    R²: The R² value of approximately 0.97 shows that the model explains 97% of the variance in stock prices.

### Backtesting Strategy

    Initial Balance: $10,000
    Result: A loss of approximately $118.62, suggesting the need for a more sophisticated strategy that accounts for market conditions and transaction costs.

### Future Directions

- Advanced Trading Strategies: Incorporate more sophisticated trading logic and include transaction costs to refine the profitability of the model.
- Feature Engineering: Add more technical indicators (e.g., moving averages, RSI) to improve prediction accuracy.
- Model Enhancement: Experiment with different LSTM architectures, such as bidirectional LSTMs or other machine learning algorithms, to improve forecasting.
- Backtesting in Diverse Market Conditions: Perform further backtesting across various market conditions to assess the robustness of the trading strategy.
