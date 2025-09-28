Air Quality Prediction using XGBoost
Project Overview

This project predicts the air quality class (Good, Moderate, Unhealthy, Unhealthy for Sensitive Groups) based on environmental and meteorological factors. It leverages XGBoost, a powerful machine learning algorithm, to classify air quality levels from features such as temperature, humidity, wind speed, atmospheric pressure, UV index, particulate matter (PM2.5 and PM10), and moon illumination.

The model can be used to monitor and forecast air quality, helping individuals and organizations take informed decisions regarding health and safety.

Dataset

The dataset consists of global environmental and air quality measurements.

Key columns used for prediction:

temperature_celsius

humidity

wind_mph

pressure_mb

uv_index

air_quality_PM2.5

air_quality_PM10

moon_illumination

air_quality_class (target variable)

Total columns: 42

Missing values: None

Features Description
Feature	Description
Temperature (°C)	Ambient temperature (0–40°C)
Humidity (%)	Relative humidity (0–100%)
Wind Speed (mph)	Wind speed in miles per hour
Pressure (mb)	Atmospheric pressure (950–1050 mb typical range)
UV Index	UV exposure level (0–11+)
PM2.5	Fine particulate matter concentration (0–500)
PM10	Coarse particulate matter concentration (0–500)
Moon Illumination (%)	Moon visibility (0–100%)
Air Quality Class	Target label: Good, Moderate, Unhealthy, Unhealthy for Sensitive Groups
Data Preprocessing

Dropped unnecessary columns (e.g., air_quality_gb-defra-index).

Selected relevant features for prediction.

Encoded target labels using LabelEncoder.

Split dataset into training and testing sets (80% train, 20% test).

Standardized numerical features using StandardScaler.

Model

Algorithm: XGBoost Classifier (multi:softprob)

Training: On 80% of the dataset with scaled features

Evaluation Metrics: Accuracy, Precision, Recall, F1-score, Confusion Matrix

Performance:

Accuracy: 100% on test data

Confusion matrix shows perfect classification for all classes

Correlation Analysis

Features such as PM2.5 and PM10 are highly correlated with air_quality_us-epa-index.

Other meteorological features (temperature, humidity, wind) have weak to moderate correlation with air quality.

A heatmap is used to visualize correlations between selected features.
