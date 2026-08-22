                             FoodShock AI: Food Price Shock Risk Detection in Bangladesh


Overview

FoodShock AI is a machine learning prototype designed to identify and estimate market-level food price shock risks in Bangladesh.
The project uses market-level food price data from the World Food Programme (WFP) Global Food Prices dataset. It focuses on Green Chili prices and identifies unusually high prices across different markets. The goal is to demonstrate how machine learning can support food price monitoring and prototype early warning systems.


Project Objectives


The main objectives of this project are:

->To identify unusually high food prices across different markets.

->To define and classify market-level price shocks.

->To compare the performance of different machine learning models.

->To estimate the probability of a price shock for different markets.

->To rank markets according to their predicted price shock risk.



Research Questions


1)Can machine learning identify unusually high food prices across different markets?

2)Which markets show a higher risk of experiencing a price shock?

3)Can market and time-related information be used to build a prototype food price risk detection system?


Dataset.

The project uses the Global WFP Food Prices dataset and focuses specifically on Bangladesh.


Selected Commodity

Green Chili was selected because it contained the highest number of available market-level observations among the explored commodities.



Dataset Summary



Total Green Chili observations: 423

Number of markets: 92

Time period: January 2026 – July 2026

Target variable: Price Shock



Initial Commodity Exploration


The project initially explored imported onion price data from India and China. However, the available onion data covered a short time period and contained insufficient observations for reliable machine learning analysis. Therefore, the project focus was shifted from long term price forecasting to market-level food price shock detection.Green Chili was selected because it provided a larger number of observations across multiple markets.


Price Shock 

A price shock is defined as an unusually high market price compared with the average price across all observed markets on the same date.


In this prototype:


Price Shock = 1


when:

Market Price ≥ 20% above the average market price on the same date.


Otherwise:


Shock = 0


Machine Learning Features
The current prototype uses the following features:

->Month

->Market Code

The target variable is:
Price Shock


Machine Learning Models
Two classification models were tested:

1. Logistic Regression: Logistic Regression was used as the baseline machine learning classifier.

2. Random Forest: Random Forest was used to capture potentially more complex relationships between market and time related features.


Model Performance

Logistic Regression:

Accuracy: 69.41%

Precision: 24.14%

Recall: 63.64%

F1 Score: 35.00%


Random Forest:


Accuracy: 85.88%

Precision: 45.45%

Recall: 45.45%

F1 Score: 45.45%

Random Forest was selected as the final model because it achieved the best overall performance in terms of Accuracy, Precision, and F1-score.

Key Findings



->The analysis identified 56 potential price shock observations out of 423 observations.

->Approximately 13.24% of observations were classified as price shock.

->Random Forest achieved the highest overall Accuracy of 85.88%.

->The model was used to estimate price shock probabilities across different markets.

->Beanibazar showed the highest predicted risk in the July prototype analysis at 88.5%.

->Sunamganj Sadar showed the second-highest predicted risk at 75.5%.



Example Prediction


Input

Market: Kawran Bazar Dhaka

Month: July


Output

Predicted Price Shock Risk: 57.00%

Risk Level: MEDIUM



Risk Classification


HIGH Risk: Predicted probability of 70% or above

MEDIUM Risk: Predicted probability between 40% and 69.99%

LOW Risk: Predicted probability below 40%



Project Workflow


WFP Global Food Prices Dataset
            ↓
Bangladesh Data Selection
            ↓
Commodity Exploration
            ↓
Green Chili Selection
            ↓
Data Preparation
            ↓
Price Shock Definition
            ↓
Feature Engineering
            ↓
Train-Test Split
            ↓
Logistic Regression
            ↓
Random Forest
            ↓
Model Evaluation
            ↓
Best Model Selection
            ↓
Market-Level Risk Prediction
            ↓
Risk Ranking and Visualization

Technologies Used


Python

Google Colab

Pandas

NumPy

Matplotlib

Scikit-learn

Machine Learning


Limitations


This project is an early stage prototype and has several limitations:

->The dataset covers a relatively short period from January to July 2026.

->The model uses only month and market information as predictor variables.

->Important factors such as inflation, exchange rates, rainfall, fuel prices, agricultural production, import costs, and supply chain disruptions are not included.

->Market names were converted into numerical codes. These codes do not represent a natural numerical relationship between markets.

->The results should therefore be interpreted as prototype based risk estimates rather than definitive real world forecasts.



Future Improvements

Future versions of FoodShock AI could include:

->Longer historical price data

->Inflation indicators

->Exchange rate data

->Fuel and transportation costs

->Rainfall and weather indicators

->Agricultural production data

->Import and supply chain information

->One-hot encoding for market variables

->Geographic features such as latitude and longitude

->Time-series forecasting models

->Real time data integration

->An interactive dashboard for policymakers and market monitoring



Conclusion

FoodShock AI demonstrates how machine learning can be used to identify and estimate market level food price shock risks in Bangladesh.

Using available Green Chili market price observations, the prototype classified unusually high prices and compared risk patterns across different markets. The project demonstrates the potential of AI-based systems to support food price monitoring and prototype early warning mechanisms.

With longer historical datasets and additional economic, weather, and supply side variables, this prototype could be further developed into a more robust food price monitoring system.

Nourin Sultana

Department of Economics

Shahjalal University of Science and Technology (SUST),Sylhet.


Project: FoodShock AI

Focus: Economics × Artificial Intelligence × Machine Learning
