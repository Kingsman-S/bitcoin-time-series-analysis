# bitcoin-time-series-analysis
ime series analysis of Bitcoin prices using AR models, including log return transformation, stationarity testing (ADF), ACF/PACF analysis, and short-term forecasting.

##Project Overview

This project focuses on analyzing and forecasting Bitcoin price movements using time series modeling techniques. The study utilizes historical data of Bitcoin prices and applies AutoRegressive (AR) models to understand patterns in log returns and generate short-term forecasts.

#Objectives
To analyze Bitcoin price behavior using time series techniques
To check stationarity of returns using statistical tests
To model the data using AR(1) and AR(2) models
To compare models using Akaike Information Criterion (AIC)
To forecast future returns.

#Dataset
Source: Yahoo Finance
Ticker: BTC-USD
Duration: Last 5 years
Feature used: Closing Price.

##Methodology

1. Data Collection
Data is fetched using the yfinance library.
Closing prices are extracted for analysis.
2. Data Transformation
Log returns are calculated to stabilize variance:
Log Return=log(Pt−1​Pt​​)

4. Stationarity Check
Augmented Dickey-Fuller (ADF) test is applied.
If p-value < 0.05, the series is considered stationary.
5. ACF & PACF Analysis
ACF (AutoCorrelation Function) and PACF (Partial AutoCorrelation Function) plots are used to identify appropriate lag values.
6. Model Building
Two models are fitted:
AR(1)
AR(2)
7. Model Evaluation
Models are compared using Akaike Information Criterion (AIC):
AIC=2k−2ln(L)
Lower AIC indicates a better model.
7. Forecasting
The best model (based on AIC) is used to forecast the next 5 time steps.

##Libraries Used
yfinance – Data collection
pandas, numpy – Data manipulation
statsmodels – Time series modeling
matplotlib – Visualization.

##Results
Log returns were found to be stationary based on ADF test.
AR models successfully captured short-term dependencies.
AIC comparison helped in selecting the better model.
Forecast values provide insight into short-term market movement.
