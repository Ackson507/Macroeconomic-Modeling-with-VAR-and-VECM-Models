# Multivariate-time-series-analysis Macroeconomic-Data.
Multivariate Time Series Analysis – [CASE OF DEVELOPING COUNTRIES; ZAMBIA]📊

📌 Introduction and Objectives of the Project.
This project aims to analyze the relationships between multiple macroeconomic variables—such as Inflation, Interest Rates, Exchange Rates, GDP etc.., and their impact on one another.

## 1️⃣ Definition and Understanding of key macroeconomic variable Indicators). 

Below is the simplified definition of some of the macroeconoic indicators and their meaning to any in relation to the economy of a country:
- Inflation_%: The percentage change in the price level of goods and services
- IR_%: Interest rates set by the central bank
- Forex_K/USD: Exchange rate of the local currency (Kwacha) to the US dollar.
- BoZ_Reserves_K: Foreign exchange reserves held by the Bank of Zambia.
- Currency_In_Circulation: Amount of local currency in circulation.
- Copper_US/Tonne: Price of copper per tonne in US dollars.
- Maize_(K'/50Kg): Price of maize per 50 kg in Kwacha.
- Gross Domestic Product per capita(USD): The total economic output of a country (Gross Domestic Product - GDP) divided by its total population

We will ensure your data is clean, complete, and in a consistent format (e.g., monthly time series), Handle missing values (e.g., interpolation or removal), and Normalize or scale the data if necessary (e.g., if variables are in different units)
  
## 2️⃣ Exloratory Data Analysis [EDA] and Formulate Hypotheses.

Unlike univariate analysis, this step involves analyzing relationships between multiple variables. Exploratory data analysis (EDA) is useful by any data scientists or analysts as it is a way of investigating data sets by summarizing their main characteristics, often employing data visualization methods. 

![ir_inf](https://github.com/user-attachments/assets/1b1ba4a2-867a-4ac2-8b21-aed3ae48be71)

The relationship between interest rates and inflation is a fundamental concept in economics and monetary policy. The nature of this relationship can vary depending on the economic context, but in most cases, it is governed by the actions of central banks and the behavior of economic agents. Below is a multiple chat indicating the trend of each indicator in the past period under study.

  
## 3️⃣ What is VAR and VECM Model.
Both VAR(Vector Autoregression) and VECM(Vector Error Correction Model) are used for modeling multiple time series that influence each other. The key difference is whether the variables are stationary or Non stationary. A VAR model is a system of regression equations where each variable is explained by its own lags and the lags of all other variables in the system, on the other hand a VECM model is used when variables are non-stationary but cointegrated (i.e., they have a long-run equilibrium relationship)

### What we will use:
We know that most economic time series and financial data are non stationary, meaning we can use VECM, but first we need to check for cointegration. If the variables we have which are assumed to be non stationary are cointergrated, then we will use VECM Model, otherwise we will achieve stationarity by method of differencing and use VAR. 
  
## 4️⃣ Cointergration Test:
Cointegration is a statistical property of time series variables that indicates a long-term equilibrium relationship between them, even if they are non-stationary in their levels, To check for cointegration in EViews, we will use the Johansen Cointegration Test with the following specification;

- Lag Length: Automatic selection: EViews can automatically choose the optimal lag length based on criteria like AIC or SIC.
- Critical Values: Significance level for the test (5%=0.05)
- Variables we will use 2013 Jan - 2024 Nov: Inflation, Interest Rates, Forex_K/USD, BoZ_Reserves_K and Currency_In_Circulation


