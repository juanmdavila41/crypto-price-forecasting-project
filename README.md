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

## Conclutions

- The results obtained in the cryptocurrency price forecasting project reveal that, while a certain level of prediction has been achieved, there are significant challenges affecting the model's accuracy. It is observed that the Mean Absolute Error (MAE) and Mean Absolute Percentage Error (MAPE) are notably high for Bitcoin (BTC) and Ethereum (ETH), suggesting that the predictions are imprecise and have a considerable margin of error.

- The low coverage in cross-validation indicates that the model is not adequately capturing the uncertainty in the predictions, suggesting the need to improve the model's robustness. Additionally, the consistency in the predicted errors, as reflected in the similarity between MAE and RMSE, indicates that the errors are predictable but persistent.

- One possible explanation for the higher volatility in Bitcoin and Ethereum could be related to their prominence in the cryptocurrency market. Being the most famous and widely traded cryptocurrencies, they are likely subject to greater speculation and price fluctuations driven by market demand and perception. On the other hand, Cardano (ADA), although exhibiting a more stable performance according to error metrics, could benefit from lower speculation and volatility compared to BTC and ETH.

- It is important to note that the values of the results may be affected by the lack of historical news data and the lack of precision in sentiment scoring. The limited availability of historical headline data and sentiment precision could be key factors contributing to the lack of accuracy in the predictions. To improve the model's accuracy, it would be necessary to have a greater amount of historical headline data and to adjust sentiment precision based on event temporality.