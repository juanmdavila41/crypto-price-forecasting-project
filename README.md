# Crypto Price Forecasting Project
## Overview
This repository contains code for a crypto price forecasting project. The project aims to predict the price of various cryptocurrencies using historical price data and sentiment analysis of news articles.

## Usage
1. Scraping Crypto News and Calculating Sentiment
The first step involves scraping news articles related to cryptocurrencies and calculating sentiment scores for each article using VADER (Valence Aware Dictionary and sEntiment Reasoner). The code for this step is provided in crypto_news_sentiment.ipynb. Here's how it works:

 - Scrapes news articles from CoinTelegraph website for specified cryptocurrencies.
 - Calculates sentiment scores for each article using VADER.
 - Saves the combined data of news headlines, dates, sentiment scores, and corresponding cryptocurrencies to a CSV file.
 
2. Downloading Historical Crypto Price Data
The second step is to download historical price data for cryptocurrencies from Yahoo Finance. This data will be used for training the forecasting models. The code for this step is provided in crypto_price_data.ipynb. Here's what it does:

 - Downloads historical price data for specified cryptocurrencies from Yahoo Finance API.
 - Merges the price data with the sentiment data obtained from the previous step based on date and cryptocurrency code.
 - Saves the combined data to a CSV file for further analysis.

3. Forecasting Crypto Prices with Prophet and Sentiment
The final step involves forecasting future prices of cryptocurrencies using the historical price data and sentiment scores. The code for this step is provided in crypto_price_forecasting.ipynb. Here's how it works:

 - Loads the combined data of historical price and sentiment scores.
 - Prepares the data for training Prophet models by handling missing values and sorting by date.
 - Configures Prophet models with sentiment scores as regressors.
 - Fits Prophet models to the data and forecasts future prices.
 - Visualizes the forecasted prices for the last month using matplotlib.

