# electricity_prediction
Forecasting electricity production and supply using ARIMA, SARIMA, SARIMAX, LSTM

🔋 Electricity Production and Supply Prediction

This repository contains a complete MSc Data Science project focused on forecasting electricity production and supply using a combination of statistical and deep learning models. The project includes data preprocessing, merging, dimensionality reduction (PCA), and model implementation for time series forecasting.

📌 Problem Statement

Accurate forecasting of electricity production is essential for ensuring balance between demand and supply. Traditional models often fail to handle external variables like weather conditions and complex non-linear trends. This project aims to build robust models that improve prediction accuracy by integrating both statistical and deep learning approaches.

🎯 Objectives

- To forecast electricity production using different models: ARIMA, SARIMA, SARIMAX, LSTM, and DNN
- To include weather data as external features to improve forecasting performance
- To compare model performance using standard regression metrics (MAE, MSE, RMSE)
- To reduce feature dimensionality using PCA

📊 Dataset
## 📂 Dataset
Two datasets were used:

The dataset includes daily electricity production and weather parameters, which were merged and preprocessed for modeling.

Electricity Data: Daily energy supply/production data
Weather Data: Corresponding daily weather data (temperature, humidity, wind, etc.)
📌 The dataset was sourced from Kaggle: [🔗 [Electricity Generation & Supply Data – Kaggle]((https://www.kaggle.com/datasets/jeanmidev/smart-meters-in-london?select=weather_hourly_darksky.csv))]

⚙️ Project Workflow
🔹 1. Data Preprocessing
    - Loaded 112 individual CSVs and concatenated into one unified DataFrame.
    - Cleaned null values: median imputation for high-null columns; dropped rows with sparse missing data.
    - Outlier detection and removal using IQR method.
    - Date column set as the index (datetime format).
🔹 2. Weather Data Cleaning
    - Cleaned and encoded weather dataset.
    - Extracted relevant date/time features.
    - One-hot encoding for categorical weather variables.
    - Merged with energy dataset on day column.
🔹 3. Dimensionality Reduction
    - Applied Principal Component Analysis (PCA) to reduce feature count from 37 to 17.
    - PCA enhanced efficiency and minimized overfitting in DL models.


🧠 Models Implemented
  🔸 ARIMA
    - Classical time series model for non-seasonal data
    - Requires data stationarity: handled with differencing
  🔸 SARIMA
    - Extension of ARIMA for seasonal data
    - Parameters include seasonal order (P, D, Q, s)
  🔸 SARIMAX
    - SARIMA + eXogenous variables
    - Performed best among statistical models
  🔸 LSTM (Long Short-Term Memory)
    - Sequence-based RNN model used to handle long-term dependencies
    - Trained on scaled data with 30-step time windows


📈 Evaluation Metrics
    Each model was evaluated using:
      - MAE (Mean Absolute Error)
      - MSE (Mean Squared Error)
      - RMSE (Root Mean Squared Error)

📌 Best Performance:
    Statistical: SARIMAX
    Deep Learning: DNN

📁 Repository Contents
File
Description
Energy_Final.ipynb
  - Preprocessing of electricity data
Weather_Final.ipynb
  - Weather dataset cleaning and encoding
Final_Data.ipynb
  - Merging energy & weather data
PCA.ipynb
  - PCA for dimensionality reduction
ARIMA.ipynb
  - ARIMA model implementation
SARIMA.ipynb
  - SARIMA model implementation
SARIMAX.ipynb
  - SARIMAX model using weather variables
LSTM.ipynb
  - LSTM deep learning model

Electricity_Prediction_Presentation.pptx
  - Final presentation slides

Electricity_Dissertation_Report.pdf
- Final project dissertation report


🎓 Author
Bolem Siva Rama Lalitha Lakshmi
MSc Data Science
GITAM University


💡 Future Scope
  - Explore hybrid models like ARIMA-LSTM
  - Include more external variables like demand, pricing, or holidays
  - Deploy models using web dashboards (Streamlit / Flask)
  - Use attention-based models for better long-term predictions
  - Implementing lag analysis
