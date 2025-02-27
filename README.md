# Multivariate-time-series-analysis Macroeconomic-Data.
Multivariate Time Series Analysis – [CASE OF DEVELOPING COUNTRIES; ZAMBIA]📊

📌 Introduction and Objectives of the Project.
This project aims to analyze the relationships between multiple macroeconomic variables—such as Inflation, Interest Rates, Exchange Rates, GDP etc.., and their impact on one another.

## 1️⃣ Definition and Understanding of key macroeconomic variable Indicators). 

Below is the simplified definition of some of the macroeconoic indicators and their meaning to any in relation to the economy of a country:
- Inflation_%: The percentage change in the price level of goods and services (dependent variable).
- IR_%: Interest rates set by the central bank (independent variable).
- Forex_K/USD: Exchange rate of the local currency (Kwacha) to the US dollar (independent variable).
- BoZ_Reserves_K: Foreign exchange reserves held by the Bank of Zambia (independent variable).
- Currency_In_Circulation: Amount of local currency in circulation (independent variable).
- Copper_US/Tonne: Price of copper per tonne in US dollars (independent variable).
- Maize_(K'/50Kg): Price of maize per 50 kg in Kwacha (independent variable).
- Gross Domestic Product per capita(USD): The total economic output of a country (Gross Domestic Product - GDP) divided by its total population

We will ensure your data is clean, complete, and in a consistent format (e.g., monthly time series), Handle missing values (e.g., interpolation or removal), and Normalize or scale the data if necessary (e.g., if variables are in different units)
  
## 2️⃣ Exloratory Data Analysis [EDA] and Formulate Hypotheses.

Unlike univariate analysis, this step involves analyzing relationships between multiple variables. Exploratory data analysis (EDA) is useful by any data scientists or analysts as it is a way of investigating data sets by summarizing their main characteristics, often employing data visualization methods. 

![ir_inf](https://github.com/user-attachments/assets/1b1ba4a2-867a-4ac2-8b21-aed3ae48be71)

The relationship between interest rates and inflation is a fundamental concept in economics and monetary policy. The nature of this relationship can vary depending on the economic context, but in most cases, it is governed by the actions of central banks and the behavior of economic agents. Below is a multiple chat indicating the trend of each indicator in the past period under study.

![other](https://github.com/user-attachments/assets/469aceb9-a531-4ec6-ad6b-7f0181a3d082)


  
## 3️⃣ Testing for stationarity and Unit Root.

Applying transformations if necessary e.g. (log differencing, differencing). To ensure accurate modeling, we must check whether our time-series data is stationary and whether the variables move together over time (cointegration). Using ADF we managed to test for stationary and applied the difference method to non_stationary series to convert them to station in readiness for building an effective regression model or equation.
![Screenshot 2025-02-26 220448](https://github.com/user-attachments/assets/92b1c660-c738-43c8-b810-50476421d30d)


  
## 4️⃣ Estimate a Regression Model and Choosing Estimation Method:
A regression model is a statistical tool used to examine the relationship between a dependent variable (the outcome you want to explain, e.g., inflation) and one or more independent variables (the factors that may influence the outcome, e.g., interest rates, exchange rates, etc.). The goal is to quantify how changes in the independent variables affect the dependent variable.
![Screenshot 2025-02-26 223207](https://github.com/user-attachments/assets/f7d3639e-a9d2-498e-bfaf-42cd49ed636e)


The model explains about 46% of the variation in inflation, with Interest Rate, FOREX_K/USD, and BoZ_Reserve being the most significant predictors. However, the presence of autocorrelation and the insignificance of some variables suggest the need for model improvements. Addressing these issues will lead to more reliable and insightful results.

Durbin-Watson Statistic: 0.156233
Interpretation: The Durbin-Watson statistic tests for autocorrelation in the residuals. A value close to 2 indicates no autocorrelation. Here, the value is far below 2, suggesting strong positive autocorrelation in the residuals. This violates the OLS assumption of no autocorrelation and may lead to biased standard errors and unreliable hypothesis tests.


