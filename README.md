# CNN-LSTM-Model-Stock-Forecasting-Based-on-Attention-Mechanism

This project focuses on forecasting stock prices using a hybrid deep learning model that combines Convolutional Neural Networks (CNN), Long Short-Term Memory (LSTM) , and an Attention Mechanism.

The aim is to predict the next 7 days of closing prices based on past trading data.


Financial time series data such as stock prices are non-linear, noisy, and often influenced by short- and long-term dependencies. Traditional methods (e.g., ARIMA) struggle with these patterns.

This project proposes a deep learning solution capable of Capturing short-term patterns using CNN, Modeling long-term dependencies using stacked LSTMs and focus on important timesteps using Attention

- **CNN Layers**: Extract short-term features from historical sequences
- **LSTM Layers**: Capture long-term dependencies in time series
- **Attention Layer**: Focus on relevant time steps dynamically
- **Dense Output Layer**: Predict a 7-day window of future closing prices

Loss Function: `Mean Squared Error (MSE)`  
Metrics: `Mean Absolute Error (MAE)` and `Root Mean Squared Error (RMSE)`
