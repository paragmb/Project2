# Project2 - Natural Gas Forecasting/Scheduling

This machine learning model will help natural gas supplier/scheduler prepare for better inventory controls in future. These kind of machine learning tool can come up with automated forecasting models and allow one person to do the work of multiple data scientists.

---

## Project Overview

Using time series forecasting models, develop a machine learning model to forecast natural gas pricing and consumption based on 10 years of historical data. Further, develop a correlation table (and/or heatmap) which contains the correlations between following variables: natural gas price, natural gas consumption, natural gas exports, storage and ambient temperature.                                                                                                               

The following two time series forecasting models were used: 1) Prophet 2) ARIMA

---

## Data Resources/Basis

#### Natural Gas Data:
- Price, Consumption, Storage, Exports
- U.S. Energy Information Administration (www.eia.gov)


#### USA Average Temperature Data:
- National Centers for Environmental Information (ncei.noaa.gov)

#### Historical Data:
- 10 Years(2012-2022)

#### Forecast Data:
- 3 Years

---

## Usage

Ensure the conda dev environment is activated.

Please launch jupyter lab to run files following files:

- ng_correlation.ipynb - Natural gas trends and correlations/heatmap
- arima_forecast.ipynb - Times Series Forecasting using ARIMA

Open Google Colab (https://colab.research.google.com/) and upload the following starter notebook:
- prophet_ngforecasting.ipynb - Times Series Forecasting using Prophet

All the csv files to run the models are located in the Resources folder.

---

## Identifying Patterns and Correlations/Heatmap

Useful insights can be gained from the quantitative plots. The dip in Apple (AAPL) stock is due to split of shares during that period. Amazon (AMZN) stock has performed better than AAPL during last 3 yrs data. The Sharpe ratio shows the gain in relation to the risk. The returns have gone higher for both stocks after Covid pandemic. The quantitative analysis plots are as follows:

### Natural Gas Spot and Futures Prices (NYMEX) - Daily
<img src="Images/dailyprice.png" width="650" height="300">

### Gas & Temperature Monthly Trends
<img src="Images/correlation.png" width="650" height="300">

### Heatmap
<img src="Images/heatmap.png" width="400" height="300">

---

## Time Series Forecasting Analysis

Monte Carlo algorithm is used to predict future stock values. Past stock values downloaded using Alpaca APIs are used to create a normal distribution of past daily returns. MC algorithm uses past daily return normal distribution to predict future daily values and cumulative returns by randomly selecting values from the distribution and propagating the stock's current value into the future. Cumulative returns are calculated from the future stock values and plotted for 500 simulations. All simulations are numerically different from each other due to the randomly selected daily return values from the normal distribution. Cumulative return probability distribution is also shown as a bar graph to illustrate the most probable future scenario range from all 500 simulations. 95% Confidence interval and its boundary values are also given for information. These boundary values should be evaluated together with the future cumulative return distribution. The financial forecasting analysis plots are as follows:

### Summary of Prophet and ARIMA forecasting models 
<img src="Images/MC_Simulation.png" width="400" height="300">

---

## Issues

New library "DataReader" was initially used to pull historical stock data. The library was sucessfully used to perform the quantitative analysis but the group ran into issues while using the library for running Monte Carlo simulations. After discussions within the group and class instructor it was decided to use Alpaca library to load data. Additionally this was also done to ensure that the project was completed on time. Please refer to the code file in the SUPERSEDED folder in the main repository.

---

## New Library

New library "Bokeh" was used. Bokeh is a data visualization library in Python that provides high-performance interactive charts and plots. Bokeh output can be obtained in various mediums like notebook, html and server. We used it to get interactive Holoviews graph to display in Visual Studio (since the group did not use the Jupyter Lab).

---

## Presentation

Please click on the following link to view the project presentation.
https://github.com/paragmb/Project1/blob/0159a7dd93a9b84a20cf7eb1b8473090f5864e56/Presentation/FinTech_Project1_Grp3_Presentation.pdf

---

## Future Steps

Although our program gives a guidance on selection of stocks, it will work for any 2 stocks as long as they are supported in Alpaca library. The program can further developed to include multiple (2 or more) stocks for more investment selections. The program can be converted into web-based interactive application in future.

---

## Contributors

Bolaji Ajimotokan, Onur Guvener, Parag Borkar

---

© 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
