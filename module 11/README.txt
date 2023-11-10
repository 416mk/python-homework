Module-11-Challenge
In this repository you will find a .ipynb file named forecasting_net_prophet.ipynb, in this file we are tasked with analysing the company's financial and user data in clever ways to help the company grow. We want to find out if the ability to predict search traffic can translate into the ability to successfully trade the stock.

Part 1 Find Unusual Patterns in Hourly Google Search Traffic
We will Read the search data into a DataFrame. Then slice the data to just the month of May 2020.
Use hvPlot to visualise the results.

Part 2 Mine the Search Traffic Data for Seasonality
We will group the hourly search data to plot the average traffic by the day of the week (for example, Monday vs. Friday). We will then use hvPlot to visualise this traffic as a heatmap. We will then group the search data by the week of the year. While answering: Does the search traffic tend to increase during the winter holiday period (Weeks 40 through 52)? We will also answer the question: Does any day-of-week effect that we observed concentrate in just a few hours of that day?.

Part 3 Relate the Search Traffic to Stock Price Patterns
In this part we will read in and plot the stock price data. Concatenate the stock price data to the search data in a single DataFrame. We will then slice the data to just the first half of 2020 (2020-01 to 2020-06 in the DataFrame). Use hvPlot to plot the data. To answer the question : Do both time series indicate a common trend that’s consistent with this narrative? We will then Create a new column in the DataFrame named “Lagged Search Trends” that offsets, or shifts, the search traffic by one hour. Create two additional columns: “Stock Volatility”, which holds an exponentially weighted four-hour rolling average of the company’s stock volatility. “Hourly Stock Return”, which holds the percentage of change in the company stock price on an hourly basis. We will then review the time series correlation, and answer the following question: Does a predictable relationship exist between the lagged search traffic and the stock volatility or between the lagged search traffic and the stock price returns?

Part 4 Create a Time Series Model by Using Prophet
Well start off by setting up the Google Search data for a Prophet forecasting model. We will then estimate the model and plot the forecast. While answering the question : How's the near-term forecast for the popularity of MercadoLibre? We will then plot three individual time series components of the model to answer the following questions: What time of day exhibits the greatest popularity? Which day of the week gets the most search traffic? What's the lowest point for search traffic in the calendar year?

Part 5 Forecast the Revenue by Using Time Series Models
In this section we will read in the daily historical sales (that is, revenue) figures, and then apply a Prophet model to the data. Interpret the model output to identify any seasonal patterns in the company revenue. For example, what are the peak revenue days? (Mondays? Fridays? Something else?). Produce a sales forecast for the finance group. Give them a number for the expected total sales in the next quarter. Include the best- and worst-case scenarios to help them make better plans.

End of Module 11

MICK CHARBONNEAU-DINELLE
10/9/23
INSPIRATION FROM FELLOW CLASSMATES AND CHATGPT, ASWELL AS BLACKBOX.IO THESE 3 SOURCES WERE USED IN ENTIRETY FOR THIS PROJECT.