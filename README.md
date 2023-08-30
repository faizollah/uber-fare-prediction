# Uber Fare Prediction
Predicting Uber fares using a deep learning model.

## Overview
This project aims to predict Uber fares based on various features using a deep neural network. The model was built using TensorFlow and Keras, and hyperparameters were tuned using Keras Tuner.

## Dataset
The dataset used for this project can be found on Kaggle: [Uber Fares Dataset](https://www.kaggle.com/datasets/yasserh/uber-fares-dataset).

## Features:
- pickup_datetime: The timestamp indicating when the ride started.
- pickup_longitude: Longitude coordinate of the pickup location.
- pickup_latitude: Latitude coordinate of the pickup location.
- dropoff_longitude: Longitude coordinate of the dropoff location.
- dropoff_latitude: Latitude coordinate of the dropoff location.
- passenger_count: Number of passengers for the ride.
- ... (and other relevant features)

## Target:
- fare_amount: The fare amount for the ride (in USD).

## Model Architecture
The deep learning model consists of multiple dense layers with varying units. The architecture was determined based on hyperparameter tuning results.

- Input Layer: 110 units, Swish activation, 10% dropout
- Hidden Layers:
    - 1st: 65 units, Swish activation, 20% dropout
    - 2nd: 80 units, Swish activation, 40% dropout
    - 3rd: 80 units, Swish activation, 20% dropout
    - 4th: 70 units, Swish activation, 20% dropout
    - 5th: 100 units, Swish activation, 30% dropout
- Output Layer: 1 unit (for regression)
The model uses the Adam optimizer with a learning rate of ~0.000672 and a weight decay of ~3.64e-05.

## Results
The model achieved promising results on the validation set, with further potential for improvement through more extensive hyperparameter tuning, feature engineering, and other advanced techniques.
