# Hospitality-Employee

### Summary and Recommendations

#### 1. Overview

This project uses ARIMA-based time series forecasting techniques to predict the number of hospitality employees for a period of one year into the future. The dataset (hosp_employees.csv) contains monthly records of the number of hospitality employees, and the goal is to build a predictive model using SARIMA (Seasonal AutoRegressive Integrated Moving Average).

By analyzing historical data, we can generate forecasts and provide insights into future trends in the number of hospitality employees.

#### 2. Data

The dataset (hosp_employees.csv) consists of the following:

- Date: Monthly time stamps from 1990 to 2018.
- Employees: The number of hospitality employees for each corresponding mon

#### 3. Modeling Approach

1. Data Preparation: 

  - The time series data is loaded, and the frequency is set to 'MS' (Month Start) to ensure the data is treated as monthly.
    A seasonal decomposition is performed to visualize the trend, seasonality, and residual components.
    
2. Stationarity Testing:

- ADF Test (Augmented Dickey-Fuller) and KPSS Test are used to check for stationarity. The ADF result suggests that the data is non-stationary and requires differencing for model building.
  
3. Model Selection:

- Auto ARIMA is used to automatically identify the optimal parameters for the ARIMA model, considering seasonal components (SARIMA).

4. SARIMA Model:

- A SARIMA model is trained on the training data, leaving the last 12 months as test data.
- The model is then evaluated using the Root Mean Squared Error (RMSE).

5. Forecasting:

  - The model forecasts employee counts for the next 12 months, and a comparison between predicted and actual values is plotted.

#### 5. Data Visualization

- Athlete Participation Over Time: Bar plot showing the number of athletes participating in each Olympic game from 1896 to 2016.
- Male vs. Female Representation: Bar plot comparing male and female athlete representation over time.
- Top 20 Athletes by Medals: Horizontal bar plot showing the top athletes with the most Olympic medals.
- Top 10 Countries by Medals: Bar plot showing the top 10 countries with the highest total medal counts.
- Age Distribution: Box plot showing the distribution of athlete ages over time.
- Top Events by Gender: Bar plots showing the top Summer and Winter Olympic events by male and female athlete participation.

#### 6. Key Findings
      
- Stationarity: The data was found to be non-stationary based on both the ADF and KPSS tests, meaning differencing was required before modeling.

- SARIMA Model Performance: The SARIMA model captured both the seasonal and non-seasonal patterns in the data. The p-values for the non-seasonal and seasonal autoregressive and moving average terms show significance, except for the seasonal AR(12) term, which suggests its impact may be minimal.

- Prediction and Forecast: The forecast showed a continuation of the seasonal pattern, following the trend observed in historical data.
  
#### 7.  Source

https://www.kaggle.com/datasets/gabrielsantello/hospitality-employees-time-series-dataset
