# Customer Churn Predictor

This project is a **Customer Churn Prediction** web application built with **Streamlit** and **TensorFlow**. It allows users to input customer details and predicts the likelihood of that customer churning (i.e., leaving the service).

## Project Overview

Customer churn prediction is a common problem in business analytics, where companies want to identify customers likely to stop using their service. This helps in proactive retention strategies.

This app leverages a pre-trained deep learning model to predict churn probability based on various customer features like age, gender, geography, account balance, and more.

## Features

- Interactive user interface built with Streamlit for easy data input.
- Uses TensorFlow Keras model (`model.h5`) trained on customer data.
- Encodes categorical features like Gender and Geography using pre-fitted label and one-hot encoders.
- Scales numeric features using a saved scaler (`scaler.pkl`).
- Provides a churn probability score and a simple interpretation of the result.
- Supports multiple input features:
  - Geography (country)
  - Gender
  - Age
  - Balance
  - Credit Score
  - Estimated Salary
  - Tenure with the company
  - Number of Products used
  - Credit Card ownership
  - Active membership status

## How It Works

1. The user selects or inputs customer attributes on the sidebar.
2. Categorical variables are transformed using saved encoders.
3. Numeric variables are scaled for model compatibility.
4. The pre-trained model predicts the churn probability.
5. The app displays the probability and indicates whether the customer is likely to churn based on a 0.5 threshold.

## Getting Started

### Requirements

- Python 3.7+
- TensorFlow
- Streamlit
- scikit-learn
- pandas
- numpy
- pickle (for loading encoders and scaler)

### Running the App

1. Clone the repository.
2. Place the following files in the root directory:
   - `model.h5` (your trained Keras model)
   - `label_encoder_gender.pkl` (label encoder for gender)
   - `onehot_encoder_geo.pkl` (one-hot encoder for geography)
   - `scaler.pkl` (feature scaler)
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
