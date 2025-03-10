# **COVID-19 Prediction Using LSTM**
This project is aimed at predicting the number of COVID-19 cases in Malaysia using deep learning. The model is built using Long Short-Term Memory (LSTM) networks, a type of Recurrent Neural Network (RNN) ideal for time series prediction. The goal of the model is to predict daily new COVID-19 cases based on the previous 30 days of data.

## Project Overview
The COVID-19 pandemic, which began in late 2019, led to widespread loss of lives and posed a challenge for countries worldwide. Predicting future cases can help governments take timely action, such as imposing or lifting travel restrictions or lockdowns. This project focuses on building a deep learning model to predict COVID-19 cases using Malaysia's historical data over the past 30 days.

### Objectives
1. Data Preparation: The first step involves preparing the dataset for model training, including data cleaning and windowing the past 30 days of data for prediction.
2. LSTM Model: Implement a Long Short-Term Memory (LSTM) model to predict daily COVID-19 cases.
3. Evaluation and Optimization: Use MLflow to track experiments and fine-tune the model for better performance.
4. Prediction: Use the best model to make predictions on test data.
5. Visualization: Plot graphs comparing the model's predictions with actual COVID-19 cases.

## Requirements
Python 3.12
TensorFlow/Keras
MLflow
NumPy
pandas
Matplotlib/Seaborn

## Data Preparation
1. We use a time_series_helper to perform data windowing for creating sliding windows of the last 30 days of data to be used for training the model. The dataset should contain the historical number of daily COVID-19 cases for Malaysia.

2. The data is split into 30-day input windows, and the corresponding output is the number of new cases on the next day (offset of 1). This allows the model to make daily predictions based on the previous 30 days.

## Model Architecture
![alt text](image.png)

## Data Training
Training the Model and use MLflow to track experiments and log training metrics.

## Data perfomrnace
The model's performance is evaluated using metrics like Mean Squared Error (MSE) and Mean Absolute Error(MAE). The best-performing model is saved and used for predictions on the test dataset.
![alt text](image-2.png)

## Results
After training the model, predictions are made on the test dataset. A plot is generated comparing the predicted daily cases with the actual values.
![alt text](image-1.png)

## Conclusion
This project demonstrates how deep learning models, specifically LSTM networks, can be applied to predict future COVID-19 cases. The model's predictions can assist in decision-making processes, such as imposing travel bans or preparing healthcare facilities. However, the model is not performing well and need to do more tuning to improve it performance.

## Credit
https://github.com/MoH-Malaysia/covid19-public