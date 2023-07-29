# NASDAQ Price Prediction With Machine Learning
This repository contains a machine learning project implemented in Python that aims to predict the price for NASDAQ using historical stock data. The project achieved an impressive accuracy of 79.5% in predicting the stock price movement.

# Project Overview
The project begins by utilizing the yfinance library to fetch daily stock price data for NASDAQ (^IXIC) from Yahoo Finance. The historical data is loaded and visualized to gain insights into the stock's behavior over time.

# Data Preprocessing
Before training the machine learning model, the data is preprocessed to enhance the prediction process. The unnecessary columns "Dividends" and "Stock Splits" are removed as they are irrelevant for price prediction. The "Close" column values are shifted one step behind to create the "price_tomorrow" column, which will serve as the target variable for the prediction.

# Machine Learning Model
The project employs the RandomForestClassifier, a popular ensemble machine learning algorithm, with 1000 estimators and a minimum sample split of 100. The model is trained on the selected predictors, namely "Close," "Volume," "Open," "High," and "Low," to forecast whether the stock price will increase or decrease (binary classification).

# Model Evaluation
The model's accuracy is assessed using the precision score on a test set of the last 100 data points. The precision score measures the ratio of correct positive predictions to the total positive predictions, giving us valuable insights into the model's performance.

# Backtesting
The repository also includes backtesting functionality to evaluate the model's performance over multiple periods. The backtesting function iterates through the data, updating the training and test sets, and generates predictions for each period. The results are stored and analyzed to assess the model's consistency across different timeframes.

# Improved Model with Probability Thresholding
In addition to the initial model, an improved version is implemented using the 'predict_proba' method of the RandomForestClassifier. This provides probability scores for each prediction, which are then thresholded at 0.5 to obtain binary predictions. This enhancement helps fine-tune the model's accuracy and reliability.

# Model Accuracy
After thorough evaluation, the final model's accuracy on the test data is calculated to be model_accuracy%. This indicates how well the model can predict the movement of NASDAQ's stock price based on the selected features.

Feel free to explore the code and replicate the experiments to understand the process better and improve the model further.
