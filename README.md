# Multivariate-time-series-analysis Macroeconomic-Data.
Multivariate Time Series Analysis – [CASE OF DEVELOPING COUNTRIES; ZAMBIA]📊

📌 Introdcution and Objectives of the Project.
This project aims to analyze the relationships between multiple macroeconomic variables—such as Inflation, Interest Rates, Exchange Rates, e.t.c., and their impact on inflation Market in Zambia. Using Vector Autoregression (VAR) and Vector Error Correction Model (VECM) techniques, we will identify how these factors interact over time and influence inflation.

1️⃣ Exploring and Understanding key macroeconomic variable (Six Indicators). 

Below are the simplified definition our what we will be working with, independent variables," the term "independent" refers to variables that are manipulated or controlled by the researcher, and their values do not depend on other variables in the study; while "dependent" refers to the variable that is measured and is expected to change based on the manipulation of the independent variable(s).

- Inflation_%: The percentage change in the price level of goods and services (dependent variable).

- IR_%: Interest rates set by the central bank (independent variable).

- Forex_K/USD: Exchange rate of the local currency (Kwacha) to the US dollar (independent variable).

- BoZ_Reserves_K: Foreign exchange reserves held by the Bank of Zambia (independent variable).

- Currency_In_Circulation: Amount of local currency in circulation (independent variable).

- Copper_US/Tonne: Price of copper per tonne in US dollars (independent variable).

- Maize_(K'/50Kg): Price of maize per 50 kg in Kwacha (independent variable).


  
2️⃣ Time-series decomposition.

Unlike univariate decomposition, this step involves analyzing relationships between variables.

🔹 Trend Analysis: Does inflation affect interest rates over time?

🔹 Seasonality Analysis: Do forex fluctuations follow predictable patterns?
  
3️⃣ Testing for stationarity and Unit Root.

Applying transformations if necessary e.g. (log differencing, differencing). To ensure accurate modeling, we must check whether our time-series data is stationary and whether the variables move together over time (cointegration).
  
🔹 Augmented Dickey-Fuller (ADF) Test: Checks for stationarity.
  
4️⃣ Building a forecasting model. 

In particular Vector Autoregressive (VAR) to Vector Error Correction Model (VECM) model to predict future value, to do this we will use:

🔹 Vector Autoregression (VAR): Best for short-term forecasting of interdependent variables.

🔹 Vector Error Correction Model (VECM): Best for modeling long-term equilibrium relationships between macroeconomic indicators.

5️⃣ Evaluate economic implications on:

-Banks and Microfinance Institution
-Forex.
