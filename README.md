# Multivariate-time-series-analysis Macroeconomic-Data.
Multivariate Time Series Analysis – [CASE OF DEVELOPING COUNTRIES; ZAMBIA]📊

📌 Introduction and Objectives of the Project.
This project aims to analyze the relationships between multiple macroeconomic variables—such as Inflation, Interest Rates, Exchange Rates, etc.., and their impact on the inflation Market in Zambia.

## 1️⃣ Exploring and Understanding key macroeconomic variable (Six Indicators). 

Below is the simplified definition our what we will be working with, independent variables," the term "independent" refers to variables that are manipulated or controlled by the researcher, and their values do not depend on other variables in the study; while "dependent" refers to the variable that is measured and is expected to change based on the manipulation of the independent variable(s).

- Inflation_%: The percentage change in the price level of goods and services (dependent variable).

- IR_%: Interest rates set by the central bank (independent variable).

- Forex_K/USD: Exchange rate of the local currency (Kwacha) to the US dollar (independent variable).

- BoZ_Reserves_K: Foreign exchange reserves held by the Bank of Zambia (independent variable).

- Currency_In_Circulation: Amount of local currency in circulation (independent variable).

- Copper_US/Tonne: Price of copper per tonne in US dollars (independent variable).

- Maize_(K'/50Kg): Price of maize per 50 kg in Kwacha (independent variable).

We will ensure your data is clean, complete, and in a consistent format (e.g., monthly time series), Handle missing values (e.g., interpolation or removal), and Normalize or scale the data if necessary (e.g., if variables are in different units)
  
## 2️⃣ Exloratory Data Analysis [EDA] and Formulate Hypotheses.

Unlike univariate analysis, this step involves analyzing relationships between multiple variables. Exploratory data analysis (EDA) is useful by data scientists or analysts to analyze and investigate data sets and summarize their main characteristics, often employing data visualization methods. One tool that will be useful to analyze these relationships.
![inflation and ir_trend](https://github.com/user-attachments/assets/9a1daf23-a595-454f-abcf-f4703a64b7f1)

The relationship between interest rates and inflation is a fundamental concept in economics and monetary policy. The nature of this relationship can vary depending on the economic context, but in most cases, it is governed by the actions of central banks and the behavior of economic agents. In our regression results later in this study, the coefficient for interest rates (IR__) is 0.997028, with a p-value of 0.0000, indicating a positive and statistically significant relationship between interest rates and inflation. 

Positive Relationship
-A 1% increase in interest rates is associated with a 0.997% increase in inflation, holding other variables constant. This positive relationship may seem counterintuitive because, in theory, higher interest rates are expected to reduce inflation, but in this case, it is not
- QUESTION IS NOW WHY:

Below is a description of each indicator variable, looking at the mean value for the period and extremes of each variable such as maximum and minimum occurrence during this period. Highlighted figures such as inflation mean was 11.70%. Inflation during this period reached a maximum of 24.6% and a minimum of 6.1%. The BoZ inflation target is between 6-8%, which seems been a challenge for the central bank to maintain as seen from the trend above.

![Screenshot 2025-02-26 221058](https://github.com/user-attachments/assets/c4b1957b-2b45-4140-a3e8-1971a88033ee)
![other](https://github.com/user-attachments/assets/20808bef-7b69-4644-937d-f27afb5641b8)


  
## 3️⃣ Testing for stationarity and Unit Root.

Applying transformations if necessary e.g. (log differencing, differencing). To ensure accurate modeling, we must check whether our time-series data is stationary and whether the variables move together over time (cointegration). Using ADF we managed to test for stationary and applied the difference method to non_stationary series to convert them to station in readiness for building an effective regression model or equation.
![Screenshot 2025-02-26 220448](https://github.com/user-attachments/assets/92b1c660-c738-43c8-b810-50476421d30d)


  
## 4️⃣ Estimate a Regression Model and Choosing Estimation Method:
A regression model is a statistical tool used to examine the relationship between a dependent variable (the outcome you want to explain, e.g., inflation) and one or more independent variables (the factors that may influence the outcome, e.g., interest rates, exchange rates, etc.). The goal is to quantify how changes in the independent variables affect the dependent variable.
![Screenshot 2025-02-26 223207](https://github.com/user-attachments/assets/f7d3639e-a9d2-498e-bfaf-42cd49ed636e)


The model explains about 46% of the variation in inflation, with Interest Rate, FOREX_K/USD, and BoZ_Reserve being the most significant predictors. However, the presence of autocorrelation and the insignificance of some variables suggest the need for model improvements. Addressing these issues will lead to more reliable and insightful results.

Durbin-Watson Statistic: 0.156233
Interpretation: The Durbin-Watson statistic tests for autocorrelation in the residuals. A value close to 2 indicates no autocorrelation. Here, the value is far below 2, suggesting strong positive autocorrelation in the residuals. This violates the OLS assumption of no autocorrelation and may lead to biased standard errors and unreliable hypothesis tests.


