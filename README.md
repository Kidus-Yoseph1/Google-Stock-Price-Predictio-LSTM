# Google Stock Price Prediction with LSTM

## Description
This project, implemented in the  Notebook, uses a **Recurrent Neural Network (RNN)** with **Long Short-Term Memory (LSTM)** layers to predict Google stock prices based on historical data. The notebook processes historical stock price data, builds and trains an LSTM model, and visualizes the predicted stock prices compared to actual prices.

## Notebook Content
- **Data Preprocessing**:
  - Loads Google stock price data from `Google_Stock_Price_Train.csv`.
  - Scales the "Open" price using MinMaxScaler to a [0, 1] range.
  - Creates sequences of 60 timesteps as input and the next timestep as output.
- **Model Architecture**:
  - A sequential RNN with four LSTM layers (50 units each), each followed by 20% dropout for regularization.
  - A dense output layer to predict the next stock price.
- **Training**:
  - Trains the model using the Adam optimizer and mean squared error (MSE) loss for 100 epochs with a batch size of 32.
- **Visualization**:
  - Plots the actual Google stock prices (red) against the predicted prices (blue) using Matplotlib.

## Dataset
- **Training Data**: `Google_Stock_Price_Train.csv` (1258 records, using the "Open" price).
- **Test Data**: Assumes `Google_Stock_Price_Test.csv` for predictions (not included in the notebook).

## Notes
- The notebook assumes test data processing and prediction code, which is not fully included.
- The model uses only the "Open" price, limiting its predictive power.
