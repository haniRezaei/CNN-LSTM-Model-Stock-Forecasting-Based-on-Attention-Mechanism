# Project Overview

This project develops a hybrid deep learning model for stock price forecasting by combining Convolutional Neural Networks (CNN), Long Short-Term Memory (LSTM) networks, and an attention mechanism. The goal is to predict the next 7 days of closing prices using the previous 60 days of historical OHLCV data.

Financial time series are typically noisy, non-linear, and influenced by both short-term fluctuations and long-term dependencies. Traditional statistical models often struggle to capture these complex patterns. To address this, the proposed model integrates multiple deep learning components, each designed to handle a specific aspect of the data.

# Model Architecture

The model follows a sequential processing pipeline:

# CNN layers are used first to extract local patterns and reduce noise in the input data.
# LSTM layers are then applied to capture long-term temporal dependencies in the time series.
# An attention mechanism is added to assign importance to different time steps, allowing the model to focus on the most relevant past observations.
# A dense output layer produces a 7-day forecast of future closing prices.


# Methodology

The model uses a multi-step forecasting approach, predicting all 7 future values simultaneously. This reduces error accumulation compared to recursive one-step predictions.

To improve generalization and training stability, several techniques are applied:

Dropout regularization
Early stopping
Learning rate reduction

In addition, the preprocessing pipeline uses separate scaling for input features and target values to avoid data leakage.

# Performance Evaluation

Model performance is evaluated using:

Mean Squared Error (MSE) as the loss function
Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)

The model achieves low prediction error and shows stable convergence during training, indicating its ability to capture underlying trends despite market noise.

# Conclusion

This hybrid CNN–LSTM–Attention framework provides an effective and flexible approach for stock price forecasting. It can be applied to different financial assets and offers a strong foundation for further research and practical decision-making.
