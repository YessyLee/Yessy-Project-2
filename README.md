![Yessy-Project-2](./images/DAT_Project2_Presentation_Yessy.jpeg)

# Business Analysis on Property Investment in Kings County, CA

**Author:** Yessy Rayner
***

## Business Overview
KC Financial Investment would like to expand their business portfolio to include property buy and sell investment. They would like to invest in the property buy and sell market in the Kings County, California. According to Realtor.com homes for sale in Kings County spend an average of 50 days on the market, so it is quite a lucrative market in term of the short sales turn around. Also the outgoing fees for buying and selling in Kings County are relatively low (under 1%) as long as they don't engage the real estate agent services due to high commission.

Their goal is to maximise profits through the buy and sell, and would like the Business Analyst (myself) to build a model that predict the house prices based on the sales database in the past two years.

Once the prediction model is built, they will then analyse all of the available houses that are currently for sale in the market and purchase the properties that are under predicted asking price. They will resell after a few weeks.

## Data Cleaning and Preparation
In this section, I will be reviewing, checking and cleaning the datas, in order to:

Ensure the datas are in correct data types
Evaluate if there are any missing value and fill it with approriate value
Once datas are cleaned, I will separate them into 3 variables or features as follow for testing and validation in order to get the best model:

Continuous variables (A continuous variable can be of any value in a range, for example: sqft living and lot sizes)
Discrete variables (certain number of particular values that can be counted, for example: number of bedrooms)
Categorical variables (descriptive categories instead of numerical or measured categories, for example: zipcodes)

## Modelling
Upon reviewing the above datas and their value, here are my breakdown on the features or variables. So we can model it approriately on the next step using linear regression model to predict property prices based on below features:

Categorical: Waterfront, zipcode
Discrete: condition, grade, bedrooms, bathrooms, floors, view
Continuous: yr_build, yr_renovated, lat, long, ALL of sqft_
