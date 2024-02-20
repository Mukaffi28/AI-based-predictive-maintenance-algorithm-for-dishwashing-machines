# Predictive Maintenance AI Algorithm

## Overview
This project focuses on developing an AI-based predictive maintenance algorithm for dishwashing machines. The algorithm utilizes a provided dataset containing temperature and vibration sensor readings under different health conditions: good, moderate, and bad. The primary objective is to create an accurate model capable of predicting when a dishwashing machine will require maintenance based on the sensor data.

## Dataset

The dataset consists of temperature and vibration sensor readings categorized into three health conditions:

- **Good:** Normal operating conditions.
- **Moderate:** Conditions indicating potential issues that may lead to maintenance.
- **Bad:** Critical conditions requiring immediate maintenance.

## Data Preprocessing

### Handling Missing Values

#### Temperature Sensor
- Apply median imputation to handle missing values in temperature sensor readings.

#### Vibration Sensor
- Apply forward fill to handle missing values in vibration sensor readings. Fill missing values with the values from the previous row.

### Health Conditions Labeling
Label health conditions based on specific criteria:
*   **Good:** if (Temperature is within the range of 15 to 70 degrees and Vibration falls between 300 and 7500)
*   **Bad:** if (Temperature is below 10 or above 70) or (Vibration is below 150 or above 7900)
*   **Moderate:** otherwise categorized as Moderate.


