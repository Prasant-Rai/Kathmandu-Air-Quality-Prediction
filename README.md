# Kathmandu Air Quality Prediction using LSTM

## Overview
Kathmandu faces severe air quality challenges due to traffic congestion, construction activity, seasonal weather patterns, and its bowl-shaped topography that traps pollutants.  
This project focuses on forecasting **hourly PM2.5 concentrations** using a Long Short-Term Memory (LSTM) neural network to capture temporal dependencies in air pollution data.

---

## Problem Statement
Air quality forecasting is inherently difficult due to strong seasonality, sudden pollution spikes, and non-linear behavior driven by both human activity and meteorological conditions.  
The objective of this project is to build a time-series forecasting model that can predict short-term PM2.5 levels in Kathmandu to support public health awareness and urban planning initiatives.

---

## Data Description
- **Source**: US Embassy Kathmandu Air Quality Sensor  
- **Time Period**: 2017–2021  
- **Frequency**: Hourly  
- **Total Records**: 60,779  

### Target Variables
- PM2.5 (µg/m³)    

### Key Challenges
- Missing and inconsistent readings  
- Strong seasonal and diurnal patterns  
- High volatility and sudden pollution spikes  

---

## Methodology

### Data Preprocessing and Feature Engineering
- Handling missing values  
- Timestamp parsing and alignment  
- Creation of time-based features (hour of day, day of week, seasonal indicators)  
- Sequence generation using a 60-hour lookback window for LSTM input  

### Exploratory Data Analysis
- Analysis of hourly, daily, and seasonal pollution trends  
- Identification of peak pollution periods  
- Visualization of long-term pollution behavior using interactive plots  

### Modeling
- Model: Long Short-Term Memory (LSTM)  
- Framework: Keras (TensorFlow backend)  
- Separate models trained for PM2.5  
- Designed to capture both short-term fluctuations and long-term temporal patterns  

### Evaluation Strategy
As this is a regression-based time series problem, model performance was evaluated using:
- Mean Absolute Error (MAE)  
- Root Mean Squared Error (MSE)  
- R² Score  

Model results were compared against a naive persistence baseline to assess predictive improvement.

---

## Results

| Metric | PM2.5 | 
|------|------|
| R² Score | 0.34 | 
| RMSE | 15.38 | 
| MAE | 9.78 | 

### Interpretation
Air pollution levels in Kathmandu are influenced by complex and often unpredictable external factors. Despite this, the LSTM model successfully captures temporal trends and outperforms naive baseline approaches, particularly for PM2.5 prediction.

---

## Key Insights
- Peak PM2.5 concentrations occur during winter mornings between 8 AM and 10 AM  
- Pollution severity shows strong seasonal dependence    

---

## Tech Stack
- Python  
- Pandas, NumPy  
- Keras (LSTM), Scikit-learn  
- Plotly  
- Jupyter Notebook  

---

## Future Work
- Integration of meteorological variables such as wind speed, temperature, and humidity  
- Hybrid modeling approaches combining LSTM with tree-based models  
- Deployment of a real-time monitoring dashboard using Streamlit  
- Clustering of pollution patterns to identify recurring pollution regimes  

---

## Conclusion
This project presents an end-to-end experimental pipeline for time-series air quality forecasting using real-world environmental data. It demonstrates practical data science skills in preprocessing, modeling, evaluation, and insight generation, and provides a strong foundation for further development toward real-world deployment.

---

## Author
Prasant Rai  
Aspiring Data Scientist  

