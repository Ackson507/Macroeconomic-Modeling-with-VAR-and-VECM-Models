# Multivariate-time-series-analysis Macroeconomic-Data.
Multivariate Time Series Analysis – [CASE OF DEVELOPING COUNTRIES; ZAMBIA]📊

📌 Introdcution and Objectives of the Project.
This project aims to analyze the relationships between multiple macroeconomic variables—such as Inflation, Interest Rates, Exchange Rates, e.t.c., and their impact on inflation Market in Zambia. Using Vector Autoregression (VAR) and Vector Error Correction Model (VECM) techniques, we will identify how these factors interact over time and influence inflation.

## 1️⃣ Exploring and Understanding key macroeconomic variable (Six Indicators). 

Below are the simplified definition our what we will be working with, independent variables," the term "independent" refers to variables that are manipulated or controlled by the researcher, and their values do not depend on other variables in the study; while "dependent" refers to the variable that is measured and is expected to change based on the manipulation of the independent variable(s).

- Inflation_%: The percentage change in the price level of goods and services (dependent variable).

- IR_%: Interest rates set by the central bank (independent variable).

- Forex_K/USD: Exchange rate of the local currency (Kwacha) to the US dollar (independent variable).

- BoZ_Reserves_K: Foreign exchange reserves held by the Bank of Zambia (independent variable).

- Currency_In_Circulation: Amount of local currency in circulation (independent variable).

- Copper_US/Tonne: Price of copper per tonne in US dollars (independent variable).

- Maize_(K'/50Kg): Price of maize per 50 kg in Kwacha (independent variable).

We will ensure your data is clean, complete, and in a consistent format (e.g., monthly time series), Handle missing values (e.g., interpolation or removal) and Normalize or scale the data if necessary (e.g., if variables are in different units).
  
## 2️⃣ Exloratory Data Analysis [EDA] and Formulate Hypotheses.

Unlike univariate analysis, this step involves analyzing relationships between multiple variables. Exploratory data analysis (EDA) is useful by data scientists or analyst to analyze and investigate data sets and summarize their main characteristics, often employing data visualization methods. One tool which will be useful to analyze this relation is to 
![inflation and ir_trend](https://github.com/user-attachments/assets/9a1daf23-a595-454f-abcf-f4703a64b7f1)

![Screenshot 2025-02-26 221058](https://github.com/user-attachments/assets/c4b1957b-2b45-4140-a3e8-1971a88033ee)


  
## 3️⃣ Testing for stationarity and Unit Root.

Applying transformations if necessary e.g. (log differencing, differencing). To ensure accurate modeling, we must check whether our time-series data is stationary and whether the variables move together over time (cointegration). Using ADF we managed to test for stationary and applied difference method to non_stationary series to convert them to station in readiness for dbuilding effective regression model or equation.
![Screenshot 2025-02-26 220448](https://github.com/user-attachments/assets/92b1c660-c738-43c8-b810-50476421d30d)


  
## 4️⃣ Estimate a Regression Model and Choosing Estimation Method:
A regression model is a statistical tool used to examine the relationship between a dependent variable (the outcome you want to explain, e.g., inflation) and one or more independent variables (the factors that may influence the outcome, e.g., interest rates, exchange rates, etc.). The goal is to quantify how changes in the independent variables affect the dependent variable.
![Screenshot 2025-02-26 223207](https://github.com/user-attachments/assets/c606eff4-cc35-449e-ad43-025c99393512)

The model explains about 46% of the variation in inflation, with Interest Rate, FOREX_K/USD, and BoZ_Reserve being the most significant predictors. However, the presence of autocorrelation and the insignificance of some variables suggest the need for model improvements. Addressing these issues will lead to more reliable and insightful results.

Durbin-Watson Statistic: 0.156233
Interpretation: The Durbin-Watson statistic tests for autocorrelation in the residuals. A value close to 2 indicates no autocorrelation. Here, the value is far below 2, suggesting strong positive autocorrelation in the residuals. This violates the OLS assumption of no autocorrelation and may lead to biased standard errors and unreliable hypothesis tests


