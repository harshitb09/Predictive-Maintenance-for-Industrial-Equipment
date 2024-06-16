# Predictive Maintenance for Industrial Equipment

## Project Overview

This project aims to develop a predictive maintenance model to forecast equipment failures in an industrial setting. By leveraging historical sensor data, the model helps reduce downtime, optimize maintenance schedules, and lower maintenance costs.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Collection](#data-collection)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Model Building](#model-building)
- [Model Evaluation](#model-evaluation)
- [Deployment](#deployment)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Data Collection

The dataset comprises sensor readings from industrial equipment, including:
- Temperature
- Pressure
- Vibration

Additionally, historical maintenance records are used to label the data with equipment failure events.

## Data Preprocessing

Data preprocessing steps include:
- Handling missing values and outliers
- Feature engineering (e.g., rolling averages, lag features)
- Splitting data into training and testing sets

## Exploratory Data Analysis (EDA)

EDA involves:
- Visualizing data patterns and correlations
- Identifying significant features
- Detecting seasonality and trends

## Model Building

A Random Forest classifier is used to predict equipment failures. Key steps:
- Hyperparameter tuning using GridSearchCV
- Training the model with optimized parameters

## Model Evaluation

The model is evaluated using:
- Classification Report (precision, recall, F1-score)
- Confusion Matrix
- ROC AUC Score

## Deployment

The model is deployed as a web service using Flask. The API accepts sensor data inputs and returns failure predictions.

### Flask API

- Endpoint: `/predict`
- Method: `POST`
- Input: JSON with sensor readings
- Output: JSON with prediction and probability

## Usage

1. **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/predictive-maintenance.git
    cd predictive-maintenance
    ```

2. **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Flask app:**

    ```bash
    python app.py
    ```

4. **Make a prediction:**

    Send a POST request to the `/predict` endpoint with the following JSON format:

    ```json
    {
        "temperature": 70,
        "pressure": 30,
        "vibration": 5,
        "temp_avg_5": 68,
        "vibration_lag_1": 4.8
    }
    ```

## Dependencies

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- Flask
- joblib

Install all dependencies using `pip install -r requirements.txt`.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

