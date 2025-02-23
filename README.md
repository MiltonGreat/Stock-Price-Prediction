# Stock Price Prediction using LSTM for PayPal (PYPL)

### Problem Statement

Predicting stock price movements is crucial for traders and investors aiming to optimize their trading strategies. However, transforming predictions into profitable trading strategies remains challenging due to factors such as market volatility, transaction costs, and unpredictable fluctuations in the market.

### Solution Approach

This project leverages a Long Short-Term Memory (LSTM) neural network to forecast PayPal's (PYPL) stock price fluctuations. The objective is to capture temporal dependencies within the stock price time series data, providing a model capable of predicting future price trends.

### Dataset Information

The project uses the yfinance library to download historical stock price data for PayPal from January 1, 2015, to January 1, 2023, including:

- Open, high, low, close (OHLC) prices
- Trading volumes

### Methods

- Data Preprocessing: Prices are normalized using MinMaxScaler, and the dataset is split into training and testing sets.
- Model: An LSTM neural network is used to capture temporal dependencies and predict future stock prices.
- Performance Evaluation: The model is evaluated using Mean Squared Error (MSE) and Mean Absolute Error (MAE) to assess prediction accuracy.
- Backtesting Strategy: A basic trading strategy is simulated based on the model's predictions to assess profitability.

### Results

The LSTM model showed a high correlation between predicted and actual stock prices, with minimal error rates, although the basic backtesting strategy didn't yield a profit.

### Model Accuracy:

- Mean Absolute Error (MAE): 7.81 (average deviation from actual closing prices).
- R-squared (R²): 0.96 (indicating that the model explains 97% of the variance in stock prices).

Trading Strategy:

- The backtesting simulation showed a final balance of $62.28 was achieved from an initial balance of $10,000, highlighting the challenges of trading strategies based solely on price predictions.
- This result suggests a modest profit, indicating that the model can generate positive returns, although the trading strategy is quite simplistic.

### Key Insights

- LSTM Model Performance: The LSTM model performs well in predicting stock price trends, with high accuracy (R² of 0.96). However, improvements are needed in the trading strategy for better profitability.

- Challenges in Trading Strategy: The backtesting results reveal that a simple buy/sell strategy based purely on price predictions can be vulnerable to transaction costs, market volatility, and noise, which can erode profits.

- Risk Management: The project underscores the need for more sophisticated risk management techniques when designing trading strategies. Factors like transaction fees and market conditions should be carefully incorporated.

### Evaluation Metrics

- MAE: The mean absolute error is approximately $7.81, meaning the model's predictions are, on average, $7.81 away from the actual closing prices.
- R²: The R² value of approximately 0.96 shows that the model explains 97% of the variance in stock prices.

### Backtesting Strategy

- Initial Balance: $10,000
- Result: A loss of approximately $62.28, suggesting the need for a more sophisticated strategy that accounts for market conditions and transaction costs.

### Future Directions

- Advanced Trading Strategies: Incorporate more sophisticated trading logic and include transaction costs to refine the profitability of the model.
- Feature Engineering: Add more technical indicators (e.g., moving averages, RSI) to improve prediction accuracy.
- Model Enhancement: Experiment with different LSTM architectures, such as bidirectional LSTMs or other machine learning algorithms, to improve forecasting.
- Backtesting in Diverse Market Conditions: Perform further backtesting across various market conditions to assess the robustness of the trading strategy.
