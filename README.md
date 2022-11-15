# Managing-Time-Series-Financial-Data-With-Pandas

Using Pandas and Yfinance module to run time series analysis on Financial Data from Yahoo Finance

Stocks analyzed: Microsoft,Coca-Cola Co, IBM , Walt Disney Co, Boeing, Apple
NYSE Tickers: MSFT, KO, IBM, DIS, BA, AAPL

Run the following command to pip install the yfinance module: !pip install yfinance

.tail(), .head(), .info() pandas method to observe last five and initial five rows and the .info() method to view the general characteristics of the stock data

![image](https://user-images.githubusercontent.com/113868226/202024509-c43008c6-1726-40b7-9640-5c096af9230b.png)

![image](https://user-images.githubusercontent.com/113868226/202024550-520eb3b6-ce67-400e-9cdf-5811fc391c04.png)


.to_flat_index() Convert a MultiIndex to an Index of Tuples containing the level values

Plotting the Stock Price Volatility Trend (2010-2019)

![image](https://user-images.githubusercontent.com/113868226/202024778-2092c815-ef1f-470c-8471-15a739d0cfa1.png)


Normalizing Time Series to a Base Value (100) to get a better output of data consistency

norm = close.div(close.iloc[0]).mul(100)

![image](https://user-images.githubusercontent.com/113868226/202025146-874296d2-708a-4552-88e7-a663ee330671.png)


 Shifting the index by desired number of periods with an optional time frequency and resampling 
 
 i) aapl.shift(periods = 1)
 ii) aapl["pct_change"] = aapl.AAPL.div(aapl.lag1).sub(1).mul(100)
 iii) aapl.AAPL.resample("BM").last().pct_change(periods =1).mul(100)
 
 Measuring Stock Perfromance with MEAN Return and Standard Deviation of Returns to measure Volatility/Risk
 
![image](https://user-images.githubusercontent.com/113868226/202025965-def214e9-a7a6-440e-87eb-781a237920ab.png)
 
![image](https://user-images.githubusercontent.com/113868226/202026214-3543cf0a-27d4-4b68-8777-cbc8df719cff.png)

![image](https://user-images.githubusercontent.com/113868226/202026166-1ecce53d-eb8f-4d2a-8b97-28fe09927a62.png)

Calculating Covariance and Correlation between the pricing volatility associated with the stocks

ret.cov()

![image](https://user-images.githubusercontent.com/113868226/202026607-8eaeed21-3286-4a5a-bf44-aed6022b040f.png)

ret.corr()

![image](https://user-images.githubusercontent.com/113868226/202026656-10b1ede7-7daf-4750-8e9e-d37e673604bb.png)

Using seaborn module to plot the Heat Map

![image](https://user-images.githubusercontent.com/113868226/202026708-b1b74c2f-ac77-43e6-bd4d-e0c12da4b3e2.png)



 
 






