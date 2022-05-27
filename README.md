# BikeSharing
Bike Sharing (Boom Bike) Data Analysis

A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free.

## Problem Statement
A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 

In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.

The company wants to know:
* Which variables are significant in predicting the demand for shared bikes.
* How well those variables describe the bike demands

## Business Goal:
Model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market.

## Steps followed:
* Exploratory data analysis (EDA)
* Model Preparation
  * Dummy Variables creation
  * Scale features before applying linear regression
  * Train Model
    1 Use RFE to analyse all features
    2 Build model using OLS Regression
    3 Generate VIF metrics for features
    4 Analyse featues one by one and re-run steps 2-4
  * Analyse Error
* Predict

## Result
### Final Model has following Features:
* yr
* holiday
* temp
* hum
* windspeed
* Light Snow
* spring
* winter
* May
* Sept

### Final VIF Metrics
    Index   Features    VIF
    0        const      59.12
    7       spring      2.67
    3         temp      2.58
    8       winter      1.93
    4          hum      1.21
    9          May      1.18
    5    windspeed      1.13
    6   Light Snow      1.12
    10        Sept      1.11
    1           yr      1.05
    2      holiday      1.01

### Error Analysis on Train Set
![Error Analysis](https://github.com/joshigeek/BikeSharing/error_train.png?raw=true)

## R-Square values
* On Train Set: 0.8419
* On Test Set : 0.7754

### Contributed by:
* Himanshu Joshi