# Bitcoin Price Prediction Using Recurrent Neural Networks (RNN)

## Project Overview
This project predicts the closing price of Bitcoin using a Recurrent Neural Network (RNN). We utilized a dataset of daily Bitcoin prices from Kaggle and implemented time-series forecasting techniques to predict future price trends.

## Data Preprocessing & Feature Engineering
- **Data Selection:** Extracted key features like `close` (closing price) and `volume_usd` (transaction volume).
- **Feature Engineering:** Created lag features for 7 and 30 days, and computed rolling averages.
- **Data Normalization:** Scaled data using MinMaxScaler to range between 0 and 1.
- **Train-Test Split:** 80:20 ratio.

## Model Architecture
We used an RNN-based model with the following layers:
- **Input Layer:** Takes historical price and volume data.
- **RNN Layers:** Tested with 1 and 2 hidden layers.
- **Fully Connected Layer:** Outputs the predicted closing price.
- **Loss Function:** Mean Squared Error (MSE).
- **Optimizer:** Adam optimizer
