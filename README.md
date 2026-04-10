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
Metrics: `Mean Absolute Error (MAE)` and `Root Mean Squared Error (RMSE)



Architectural Rationalization
The architectural logic follows a hierarchical processing pipeline designed for optimal feature extraction and temporal modeling. Initially, three 1D-Convolutional layers act as automated filters to identify local spatial patterns and reduce market noise within the raw OHLCV data. These features are then passed to a stacked configuration of three LSTM layers, each with 200 units, which are utilized to capture complex, long-term dependencies while mitigating the vanishing gradient problem. To overcome the traditional memory bottleneck of LSTMs, a bespoke Bahdanau-style Attention layer was implemented from scratch using the Keras Backend. This mechanism dynamically assigns probabilistic weights to critical historical timesteps, ensuring the model prioritizes high-impact events that influence future price pivots.

Technical Implementation & Rigor
Technical rigor is maintained through a specialized multi-step vector-output approach, which predicts the entire 7-day forecast horizon simultaneously to minimize recursive error accumulation. To ensure model stability and generalization, the training process incorporates aggressive dropout regularization, early stopping, and a dynamic learning rate reduction strategy. These safeguards are essential for managing a high-capacity model with over 1.0 million trainable parameters. Furthermore, the preprocessing pipeline utilizes independent dual-scaling logic to prevent data leakage, ensuring that the features and targets are transformed without cross-contamination.

Results and Performance Metrics
Empirical results demonstrate the effectiveness of this hybrid approach, with the model achieving a high degree of precision evidenced by a Mean Absolute Error (MAE) of approximately 0.007 (scaled data) and a low Root Mean Squared Error (RMSE). The training and validation loss curves exhibit smooth convergence over 100 epochs, validating the model’s ability to successfully filter volatility and learn underlying market trends. This framework is designed to be asset-agnostic, providing a scalable foundation for quantitative research and tactical decision support in various financial domains.
