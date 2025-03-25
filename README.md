# WeatherTrendForecasting-PMAcceleratorAssignment

# Global Weather Forecasting Project Report

## 1. Introduction

**Project Overview:**

This project involves forecasting global weather conditions using various analytical and machine learning techniques. The analysis spans from data cleaning and exploratory data analysis (EDA) to advanced forecasting using multiple models and anomaly detection.

**Company's Mission:**

“By making industry-leading tools and education available to individuals from all backgrounds, we level the playing field for future PM leaders. This is the PM Accelerator motto, as we grant aspiring and experienced PMs what they need most – Access. We introduce you to industry leaders, surround you with the right PM ecosystem, and discover the new world of AI product management skills.”

**Purpose of the Report:**

The report covers both basic and advanced assessments including data cleaning & preprocessing, EDA, model building for time series forecasting, and unique analyses (such as climate, environmental impact, feature importance, and spatial analysis). The goal is to showcase a comprehensive approach to handling, analyzing, and forecasting global weather data.

## 2. Data Cleaning & Preprocessing

### 2.1 Data Acquisition and Initial Inspection

**Data Source:** GlobalWeatherRepository.csv

**Initial Steps:**
- Imported libraries and installed dependencies.
- Loaded the dataset and inspected its structure with `.info()` and `.describe()`.
- Converted date columns (e.g., `last_updated`) into datetime format.

### 2.2 Handling Missing Values and Outliers

**Missing Values:**
- Counted null values in each column and identified specific dates with missing data.
- Applied manual corrections for identified missing dates (e.g., copying previous day’s values).

**Outlier Considerations:**
- Outlier handling : In this dataset every value was considered important, so no data points were removed.

### 2.3 Feature Engineering and Data Transformation

**Column Selection:**
- Kept essential columns and removed duplicate/redundant features (e.g., converting Fahrenheit to Celsius).

**Encoding:**
- Applied label encoding for categorical features (e.g., `condition_text` and `wind_direction`).

**Normalization:**
- Applied scaling techniques where necessary for model readiness.

## 3. Exploratory Data Analysis (EDA)

### 3.1 Trend Analysis

**Temperature Trends:**
- Daily average temperature was calculated over the time period.
- A line plot with a horizontal line representing the overall average was generated.

**Humidity Trends:**
- Similar analysis as temperature with daily averages and overall mean.

**Wind Speed and Wind Direction Trends:**
- Analyzed trends in wind speed (kph) and wind degree (direction).

**Precipitation Trends:**
- Evaluated daily precipitation levels with overall average annotations.

**Air Quality Trends:**
- Visualizations include trends for Carbon Monoxide, Nitrogen Dioxide, Ozone, and other pollutants.

**Cloud Formation Trends:**
- Analyzed the trend in cloud cover over time.

### 3.2 Spatial Analysis

**Global Distribution:**
- A scatter geo-plot visualized the global temperature distribution using latitude and longitude.

## 4. Model Building and Forecasting

### 4.1 Basic Forecasting Model (XGBoost)

**Data Preparation:**
- Created a time-series dataset using resampled daily averages.
- Split data into training and testing sets.

**Model Building:**
- Trained an XGBoost regression model to predict `temperature_celsius`.
- Evaluated model performance using metrics such as Mean Squared Error (MSE) and Root Mean Squared Error (RMSE).

### 4.2 Time Series Forecasting using ARIMA and SARIMA

**Stationarity Testing:**
- Performed the Dickey-Fuller test to check stationarity.
- Applied differencing to make the time series stationary.

**ARIMA Forecasting:**
- Built and evaluated an ARIMA model on the differenced data.

**SARIMA Forecasting:**
- Constructed and evaluated a SARIMA model with seasonal components.

### 4.3 Forecasting with Facebook Prophet

**Model Implementation:**
- Prepared the dataset as required by Prophet.
- Generated a future forecast and plotted the results.

## 5. Advanced Assessment

### 5.1 Advanced Exploratory Data Analysis

**Anomaly Detection:**
- Implemented Isolation Forest to detect anomalies in temperature data.
- Generated plots to highlight the detected anomalies.

### 5.2 Forecasting with Multiple Models and Ensemble Techniques

**Model Comparison:**
- Compared performance across different forecasting models (XGBoost, ARIMA, SARIMA, Prophet).
- Considered ensemble approaches to improve forecast accuracy.

### 5.3 Unique Analyses

**Climate Analysis:**
- Studied long-term climate patterns across various regions.

**Environmental Impact:**
- Analyzed the relationship between air quality metrics and weather conditions.

**Feature Importance:**
- Assessed feature importance using an ExtraTreesClassifier.
- Visualized the feature importance rankings.

**Spatial Analysis of Weather Conditions:**
- Explored geographical differences in weather conditions using spatial plots.

## 6. Conclusion

**Key Findings:**

- **Data Cleaning & Preprocessing:** Successfully handled missing values and refined features for robust analysis.
- **EDA Insights:** Trends across temperature, humidity, wind speed, and air quality reveal significant patterns that guide model building.
- **Model Performance:** Forecasting models (XGBoost, ARIMA, SARIMA, Prophet) demonstrated varying levels of accuracy, with ensemble methods showing promise for improved predictions.
- **Advanced Analyses:** Anomaly detection and spatial analysis provided additional layers of insight into regional and environmental impacts.

**Final Note:**

The project demonstrates a comprehensive workflow from data preprocessing to advanced forecasting and spatial analysis, in alignment with the company’s mission to empower future PM leaders through access to cutting-edge tools and insights.
