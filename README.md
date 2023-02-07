# Predicting-which-stocks-will-beat-SPY-with-TA
- In this project, I create 3 models: 1 linear regression model, 1 time series model and 1 ensemble model. They will all predict which stocks of the S&amp;P100 will beat SPY by at least 10% in 1 year. The models will be trained with stock price, simple moving averages and candle sticks represented mathematically. 
## Title: "Predicting Outperforming S&P 500 Stocks using Close Price and Technical Analysis Indicators"
## Introduction:
- The S&P 100 index is considered to be by some the gold standard benchmark for the stock market performance in the United States. However, not all stocks in the index perform equally well. Some stocks will inevitable outperform others. In this project, 3 machine learning models will be build. They will use stock price and technical analysis indicators to predict which stocks in the S&P 100 will beat the index by 10% or more in one year. By identifying these outperforming stocks, investors can potentially achieve higher returns.
## Data collection:
- Information of all stocks in the S&P 100 will be collected in the past 5 years. Looking at all of the stocks of the S&P500 may be too much data for a home computer to handle. Specifically, we will collect close price, moving averages and candel sticks represented mathematically.
## Choice of model:
- There are 3 popular machine learning models for stock prediction:
- Time-series models
- Regression models
- Ensemble methods
- All 3 types of models shall be explored, specifically a prophet time series model, a Support Vector Regression (SVR) model and a random forest model.
- Time-series models, such as ARIMA or SARIMA, are useful for stock prediction as they are well-suited for predicting values based on historical patterns in time-series data. There is no reason why Prophet was used specifically.
- SVR was chosen over linear regression because it has 2 advantages over linear regression in stock prediction.
- Non-linearity: stock performance can be influenced by a large number of factors, some of which may not have a linear relationship. SVR can handle non-linear relationships between inputs and outputs better than linear regression.
- Outlier handling: SVR is less sensitive to outliers than linear regression, which will exist for sure in the stock market. With SVR, there is a lower chance that outliers will ruin the model.
- Ensemble methods such as random forest and gradient boosting are useful for stock prediction due to their ability to capture complex non-linear relationships and handle high-dimensional data.
- In practice, it is common to use a combination of these methods or to experiment with different models to find the one that provides the best results for a given stock or market.
## Prediction
- The models will work despite using TA indicators instead of business fundamentals because simple moving averages and candle sticks measure a stocks momentum, and it is well known that stocks that go up tend to keep going up and stocks going down tend to continue to go down.
- The ensemble model will most likely perform the best. This is because time-series models and regression models unfortunately have some limitations when it comes to handling high-dimensional and complex data. Time-series models assume that the future will follow a similar pattern as the past, and may struggle when that is not the case. Regression models on the other hand assume a linear relationship between the features and the target, and may not capture non-linear relationships in the data.
- Ensemble methods can overcome these limitations by combining the predictions of multiple models to find non-linear and non-cyclical relationships between the features and the target. They also have the advantage of combining the predictions from multiple weak models to produce a more accurate and robust prediction. For these reasons, ensemble methods are effective in handling high-dimensional and complex data like stock movements.
## Results
- Time-series model:
- Stocks that beat SPY and when:
[('AAPL', '2019-12-31'), ('ACN', '2019-12-31'), ('ADBE', '2019-12-31'), ('AMD', '2019-12-31'), ('AMT', '2019-12-31'), ('BAC', '2019-12-31'), ('C', '2019-12-31'), ('CHTR', '2019-12-31'), ('COST', '2019-12-31'), ('DHR', '2019-12-31'), ('GE', '2019-12-31'), ('GS', '2019-12-31'), ('JPM', '2019-12-31'), ('LMT', '2019-12-31'), ('MA', '2019-12-31'), ('MDLZ', '2019-12-31'), ('META', '2019-12-31'), ('MSFT', '2019-12-31'), ('NEE', '2019-12-31'), ('NVDA', '2019-12-31'), ('QCOM', '2019-12-31'), ('RTX', '2019-12-31'), ('SO', '2019-12-31'), ('T', '2019-12-31'), ('TGT', '2019-12-31'), ('TMO', '2019-12-31'), ('V', '2019-12-31'), ('AMZN', '2020-12-31'), ('AVGO', '2020-12-31'), ('BLK', '2020-12-31'), ('CRM', '2020-12-31'), ('FDX', '2020-12-31'), ('GOOG', '2020-12-31'), ('GOOGL', '2020-12-31'), ('LLY', '2020-12-31'), ('LOW', '2020-12-31'), ('MS', '2020-12-31'), ('NFLX', '2020-12-31'), ('NKE', '2020-12-31'), ('PYPL', '2020-12-31'), ('TMUS', '2020-12-31'), ('TSLA', '2020-12-31'), ('TXN', '2020-12-31'), ('UPS', '2020-12-31'), ('AIG', '2021-12-31'), ('COF', '2021-12-31'), ('COP', '2021-12-31'), ('CSCO', '2021-12-31'), ('CVS', '2021-12-31'), ('CVX', '2021-12-31'), ('F', '2021-12-31'), ('GD', '2021-12-31'), ('GM', '2021-12-31'), ('HD', '2021-12-31'), ('PFE', '2021-12-31'), ('SCHW', '2021-12-31'), ('SPG', '2021-12-31'), ('UNH', '2021-12-31'), ('WFC', '2021-12-31'), ('XOM', '2021-12-31'), ('ABBV', '2022-12-30'), ('AMGN', '2022-12-30'), ('BA', '2022-12-30'), ('BMY', '2022-12-30'), ('BRK-B', '2022-12-30'), ('CAT', '2022-12-30'), ('CL', '2022-12-30'), ('DUK', '2022-12-30'), ('EMR', '2022-12-30'), ('EXC', '2022-12-30'), ('GILD', '2022-12-30'), ('HON', '2022-12-30'), ('IBM', '2022-12-30'), ('JNJ', '2022-12-30'), ('KHC', '2022-12-30'), ('KO', '2022-12-30'), ('LIN', '2022-12-30'), ('MCD', '2022-12-30'), ('MET', '2022-12-30'), ('MO', '2022-12-30'), ('MRK', '2022-12-30'), ('ORCL', '2022-12-30'), ('PEP', '2022-12-30'), ('PG', '2022-12-30'), ('PM', '2022-12-30'), ('WMT', '2022-12-30')]

- Stocks the model predicted would beat SPY:
[('AAPL', '2019-12-31'), ('ABT', '2019-12-31'), ('ACN', '2019-12-31'), ('ADBE', '2019-12-31'), ('AMD', '2019-12-31'), ('AMGN', '2019-12-31'), ('AMT', '2019-12-31'), ('AVGO', '2019-12-31'), ('AXP', '2019-12-31'), ('BAC', '2019-12-31'), ('BLK', '2019-12-31'), ('BMY', '2019-12-31'), ('C', '2019-12-31'), ('CHTR', '2019-12-31'), ('CMCSA', '2019-12-31'), ('COF', '2019-12-31'), ('COST', '2019-12-31'), ('DHR', '2019-12-31'), ('DIS', '2019-12-31'), ('GE', '2019-12-31'), ('GOOG', '2019-12-31'), ('GOOGL', '2019-12-31'), ('GS', '2019-12-31'), ('HD', '2019-12-31'), ('HON', '2019-12-31'), ('INTC', '2019-12-31'), ('JPM', '2019-12-31'), ('KO', '2019-12-31'), ('LIN', '2019-12-31'), ('LLY', '2019-12-31'), ('LMT', '2019-12-31'), ('LOW', '2019-12-31'), ('MA', '2019-12-31'), ('MDLZ', '2019-12-31'), ('MDT', '2019-12-31'), ('META', '2019-12-31'), ('MRK', '2019-12-31'), ('MS', '2019-12-31'), ('MSFT', '2019-12-31'), ('NEE', '2019-12-31'), ('NKE', '2019-12-31'), ('NVDA', '2019-12-31'), ('PEP', '2019-12-31'), ('PG', '2019-12-31'), ('PYPL', '2019-12-31'), ('QCOM', '2019-12-31'), ('RTX', '2019-12-31'), ('SBUX', '2019-12-31'), ('SO', '2019-12-31'), ('SPY', '2019-12-31'), ('T', '2019-12-31'), ('TGT', '2019-12-31'), ('TMO', '2019-12-31'), ('TMUS', '2019-12-31'), ('TSLA', '2019-12-31'), ('TXN', '2019-12-31'), ('V', '2019-12-31'), ('WMT', '2019-12-31'), ('AMZN', '2020-12-31'), ('CAT', '2020-12-31'), ('CRM', '2020-12-31'), ('FDX', '2020-12-31'), ('GM', '2020-12-31'), ('NFLX', '2020-12-31'), ('UNH', '2020-12-31'), ('UPS', '2020-12-31'), ('ABBV', '2021-12-31'), ('AIG', '2021-12-31'), ('BK', '2021-12-31'), ('BRK-B', '2021-12-31'), ('COP', '2021-12-31'), ('CVS', '2021-12-31'), ('CVX', '2021-12-31'), ('EXC', '2021-12-31'), ('F', '2021-12-31'), ('GD', '2021-12-31'), ('MET', '2021-12-31'), ('ORCL', '2021-12-31'), ('PFE', '2021-12-31'), ('SCHW', '2021-12-31'), ('SPG', '2021-12-31'), ('WFC', '2021-12-31'), ('XOM', '2021-12-31')]

- Regression model
- Stocks that beat SPY from 2021-12-31 to 2022-12-31:
['GE', 'GM', 'CSCO', 'BA', 'GILD', 'BMY', 'CVS', 'COP', 'CRM', 'BKNG', 'CL', 'DOW', 'CHTR', 'XOM', 'CMCSA', 'DUK', 'AXP', 'EMR', 'EXC', 'BAC', 'F', 'COF', 'C', 'DIS', 'CVX', 'AMZN', 'NVDA', 'ADBE', 'ORCL', 'PFE', 'PM', 'PYPL', 'QCOM', 'RTX', 'SBUX', 'SCHW', 'SO', 'WFC', 'ABT', 'T', 'TGT', 'TMUS', 'TSLA', 'WBA', 'TXN', 'UPS', 'USB', 'AAPL', 'SPG', 'NKE', 'NEE', 'GOOGL', 'HON', 'INTC', 'JPM', 'KHC', 'WMT', 'KO', 'LLY', 'VZ', 'MS', 'AIG', 'MRK', 'MO', 'GOOG', 'META', 'AMD', 'MDT', 'MDLZ', 'BK', 'MET']

- Stocks that the model predicted would beat SPY from 2021-12-31 to 2022-12-31:
['ABBV', 'AMGN', 'BA', 'BMY', 'BRK-B', 'CAT', 'CL', 'DUK', 'EMR', 'EXC', 'GILD', 'HON', 'IBM', 'JNJ', 'KHC', 'KO', 'LIN', 'MCD', 'MET', 'MO', 'MRK', 'ORCL', 'PEP', 'PG', 'PM', 'WMT']

- Ensemble method
## Overcoming difficulties
- Information could not be collected until BRK.B was replaced with BRK-B in the tickers list.
- Originally, the mid price (average of daily high and daily low) was to be used instead of the close for smoother data. But a regular home computer would already require multiple hours to collect the data that was to be collected, and so close price was used to reduce work load by as much as possible.
- Monthly data was collected from pandas_ta because daily data took too long.
- It was discovered that yfinance could quickly collect daily data, but by then all the features were already calculated with monthly data from pandas_ta. However, the daily data from yfinance was useful in building the time series model.
- Instructions on how to build a time series trained with multiple features could not be found. So daily close price was used as the only feature.
- The SVR model would not work initially. This was because Date needed to be converted into a meaningful number and Ticker which was not a number needed to be dropped.
- The SVR model needed a Y, the future 1 year close price, but manually adding the future price of over 6000 rows of data was too much work to do. The future close price could not be the current close price shifted 12 rows down because the df had 101 stocks not just 1 stock. So a function was made to creates two new columns: - - - Future_1_year_close and Ticker2. It then populates them with the values from the Close and Ticker columns shifted 12 rows down, and if Ticker and Ticker2 was not equal, Future_1_year_close will be set to NaN. NaN would then be dropped.
## Future direction
- Backtest theses machine learning models with equal weighted portfolios. Find out if the ensemble model really did perform the best.
