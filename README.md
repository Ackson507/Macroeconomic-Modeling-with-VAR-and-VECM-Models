# Multivariate-time-series-analysis Macroeconomic-Data.
Multivariate Time Series Analysis – [CASE OF DEVELOPING COUNTRIES; ZAMBIA]📊

![f937cb40117f3a2892a6f391199a3ad2](https://github.com/user-attachments/assets/e6ca1a05-49aa-4aff-bd87-013833702164)

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

![other](https://github.com/user-attachments/assets/00d64f51-b952-4d8e-aa23-45f56bca8471)

  
## 3️⃣ What is VAR and VECM Model.
Both VAR(Vector Autoregression) and VECM(Vector Error Correction Model) are used for modeling multiple time series that influence each other. The key difference is whether the variables are stationary or Non stationary. A VAR model is a system of regression equations where each variable is explained by its own lags and the lags of all other variables in the system, on the other hand a VECM model is used when variables are non-stationary but cointegrated (i.e., they have a long-run equilibrium relationship)

### What we will use:
We know that most economic time series and financial data are non stationary, meaning we can use VECM, but first we need to check for cointegration. If the variables we have which are assumed to be non stationary are cointergrated, then we will use VECM Model, otherwise we will achieve stationarity by method of differencing and use VAR. in this project we will use VAR(Vector Autoregression),

## 4️⃣ Cointergration Test for VECM :
Cointegration is a statistical property of time series variables that indicates a long-term equilibrium relationship between them, even if they are non-stationary in their levels, To check for cointegration in EViews, we will use the Johansen Cointegration Test with the following specification;

- Lag Length: Automatic selection: EViews can automatically choose the optimal lag length based on criteria like AIC or SIC.
- Critical Values: Significance level for the test (5%=0.05)
- Variables we will use 2013 Jan - 2024 Nov: Inflation, Interest Rates, Forex_K/USD, BoZ_Reserves_K and Currency_In_Circulation
  
## 5️⃣ ADF: Differencing and Testing for stationarity using ADF
![Screenshot 2025-02-28 080937](https://github.com/user-attachments/assets/0a07f423-6bba-4708-90ab-02d9286461d1)

The table above shows how we achived stationarity using ADF UNIT ROOT TEST. As mentioned earlier when using VAR we need to ensure the variables are stationary, to achieve this we used a method of applying differencing to each variable when checking for UNIT ROOT at different levels in order to achieve stationarity such Level(Raw Data), 1st Difference and 2nd Difference.

The table indicatates the Hypothesis we generated and at what level we achieved stationarity. Once we have all the variables stationary we can move to next step.

## 5️⃣ Building VAR Model⚕️

Once we have our varibales ready then we can Estimate the VAR by using QUICK > Estimate VAR using our Eview 14 and set following configueration
- VAR Specification: Standard VAR
- Estimation Sample: Entire Dataset from 2013 January to 2024 November
- Lag Intervals: We will use default generated lag from Eview [We can do the test to find optimal lags but for this study we will stick to default]
- Exogenous Varibale: This is where we include an error term by default it is c
- Endogenous Varibales: This is where we include differenced varibles in our model

## 6️⃣ Refining, Interpreting and Evaluating the Model Estimates.

Below is a VAR Estimate Model table.
![Screenshot 2025-02-28 085804](https://github.com/user-attachments/assets/e500cc21-3ddf-416c-98ef-3f926121a1bd)

- Goodness of Fit: The high R-squared values (e.g., 0.970848) and low standard errors (e.g., 0.393561) suggest the model fits the data well.

- Significance: The high F-statistic (e.g., 426.2788) indicates the model is statistically significant.
  
- The Akaike and Schwarz criteria can be used to compare this model with others.
  
- Potential Issues: The large determinant residual covariance values (2.56E+22) might indicate multicollinearity or scaling issues in the data. In this case we will not go deeper.

Stability Check.
![stability](https://github.com/user-attachments/assets/61570466-982f-41ca-a61f-be3a7903fa3e)

- Since all eigenvalues are inside the unit circle, our model is stable.
  
## 7️⃣ DATA REFERENCES








