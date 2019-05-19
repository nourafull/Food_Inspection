# Chicago Food Inspection

## Executive Summary

#### Problem Definition
This data science project aims to optimize the Food Inspection process at Chicago city by trying to predict the restaurants that contain food violations, especially critical & serious violations, as defined by Chicago's Food Inspection Reporting System. The status of an inspection can be Pass, Pass with Conditions, or Fail, depending on the type of violations found. To create a predictive model, we used data about the weather, community area features, restaurant chain size, restaurant risk level, and the number and percentage of past failed visists. We noticed in our analysis that restaurants with more than one inspection behave differently than restaurants with only one or two inspections. Therefore, we creates two models, one using all observations, and the second using only restaurants with one or two past inspection visits.

#### Research Question
According to the inspection process, we would like to predict restaurants that would pass with conditions or fail, because those are the restaurants that contain serious or critical violations. We would like to create a model that predicts whether a restaurant requires inspection, based on the data we have on past inspections. Therefore, we would like to predict whether an observation belongs to one of two classes: 
- Pass
- Pass wth Conditions or Fail

#### Model Evaluation
When evaluating our model, we would like to increase Precision.We want to try to catch all restaurants with violations, and do not mind catching some restaurants without violations in the process. In other words, we do not want to miss the restaurants with critical and serious violations.

We used four classification models: 
- Logistic Regression
- Decision Trees
- Random Forrests
- XGBoost 

XGBoost returned 83.6%, the highest Accuracy among all models.

#### Results & Recommendations
According to our analysis and our models' feature importance, the feature that has the highest correlation with the results of an inspection is the percentage of past failed inspections. Other features also correlated with an inspection's results, but very weakly. We created two models, one for the complete dataset, and another for the observations with more than two insepctions. According to our results, the first model outperformed the second one.

Our recommendation for future work is to add more features to the dataset, mainly features about the restaurants themselves. Other than the restaurant risk level and the chain size, our dataset was lacking information about the restaurants themselves, such as the type of cuisine, the price range, and customer ratings from social media. 

Furthermore, the community area could be investigated further. According to the feature importance of the models, some community areas are either positively or negatively correlated with the results of an inspection. We could add a feature that represents the 9 regions of Chicago, they might show a pattern that we could not see with 77 community areas. 

## Table of Content
- Import and Preprocess Data
- Exploratory Data Analysis
- Feature Re-engineering
    - Regions	
        - Crime
        - Sanitation
        - Poverty, Education & Unemployment
    - Frequency of Inspections & Failures
    - Number of branches per restaurant (Restaurant Chain Sizes)
    - Weather
        - Season
        - Temperature and Humidity
        - Three consecutive days of high Temperature
    - Violations
    - Yelp Data
- Modeling
    - Model 1: All Restaurants
    - Model 2: Restaurants with 3 and more Inspection Visits
- conclusion
