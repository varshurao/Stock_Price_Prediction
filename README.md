
# 📈📈 Building a Stock Price Prediction Analytics using Snowflake & Airflow 

## Overview

  This project is an end-to-end pipeline for stock price prediction using historical data from Alpha Vantage APIs. It leverages Apache Airflow for managing the tasks, Snowflake for data storage and prediction and SQL to retrieve and process data.

## Features
1. Data Extraction: Fetches daily stock prices for specified symbols using the Alpha Vantage API.
2. Data Transformation: Processes the raw data for analysis.
3. Data Loading: Inserts the processed data into Snowflake.
4. Model Training: Creates a machine learning model for forecasting stock prices.
5. Prediction: Generates predictions and combines them with actual data.
   
## Technologies Used
- Apache Airflow: For workflow orchestration.
- Snowflake: For data storage and machine learning capabilities.
- Alpha Vantage API: For fetching stock price data.
- Python: Programming language for scripting and data processing.

## Requirements
- Python 3.x
- Apache Airflow
- Snowflake

## To setup my Repo

1. Clone the repository:
			git clone <repository-url>
			cd <repository-directory>
   
3. Install dependencies: pip install -r requirements.txt

3. Set up Airflow: Install and configure Apache Airflow and ensure that Snowflake account is created to connect with Airflow as snowflake_conn

5. API Key: Obtain an Alpha Vantage API key from https://www.alphavantage.co/ and set it as an Airflow variable named alphavantage_apikey

## Usage
- Start your Airflow scheduler and web server.
- Access the Airflow UI
- Trigger the AlphaVantage_Stock_Price_Prediction_Analysis DAG manually or wait for the scheduled runs

## DAG Structure
- extract: Fetches stock data from Alpha Vantage.
- transform: Prepares the fetched data for loading.
- load: Inserts the transformed data into Snowflake.
- train_model: Trains a forecasting model using Snowflake's machine learning capabilities.
- predict: Makes predictions and creates a final output table.
