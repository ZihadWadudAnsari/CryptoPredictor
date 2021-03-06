The purpose of this project was to provide relevant calculated data and machine learning models to forecast future prices with real-time live data.

This project is split into two subsections the first is based on data analysis of the live reaction market which operates by interacting with 
the Alternative.me Crypto Fear & Greed Index API and PyTrends the Unofficial API for Google Trends. From these two API call it provides the user
with the live last 30 days average (mean) value. This is helpful for the user to understand the current state of reaction to market prices.
Lastly to complete the analysis, a graph is produced to show the relationships between the Fear & Greed Index value and the "Bitcoin" search term
value however for this to happen a data pipeline had to be constructed this is because the live data from the PyTrends API were few days late to
update. The data pipeline utilises ETL operations to automatically get the data from the APIs, clean the data, store into a Pandas dataframe and then to
push to the AWS MySQL cloud database to be queried.

The second subsection is the machine learning models, I utilised the yfinance Unofficial API for Yahoo Finance to access the real-time data.
The first model is a forecasting machine learning model using time series analysis via the Prophet library to predict the future bitcoin prices based on
the timeline of the particular extracted data. The second model is a linear regression model via ScikitLearn Linear Regression library using the same 
extracted data to display the trend line (Linear Regression line) of the specified crypto.

Languages:
- Python
- MySQL

APIs:
- Alternative.me Crypto Fear & Greed Index API
- PyTrends the Unofficial API for Google Trends
- yfinance Unofficial API for Yahoo Finance

Services:
- AWS RDS for MySQL Cloud Database

Libraries:
- Pymysql
- Pandas
- Scikit-learn
- Facebook Prophet
- Matplotlib
