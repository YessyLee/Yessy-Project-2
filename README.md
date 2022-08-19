![Yessy-Project-2](./images/DAT_Project2_Presentation_Yessy.jpg)

# Business Analysis on Property Investment in Kings County, CA

**Author:** Yessy Rayner
***

## Business Overview
KC Financial Investment would like to expand their business portfolio to include property buy and sell investment. They would like to invest in the property buy and sell market in the Kings County, California. According to Realtor.com homes for sale in Kings County spend an average of 50 days on the market, so it is quite a lucrative market in term of the short sales turn around. Also the outgoing fees for buying and selling in Kings County are relatively low (under 1%) as long as they don't engage the real estate agent services due to high commission.

Their goal is to maximise profits through the buy and sell, and would like the Business Analyst (myself) to build a model that predict the house prices based on the sales database in the past two years.

Once the prediction model is built, they will then analyse all of the available houses that are currently for sale in the market and purchase the properties that are under predicted asking price. They will resell after a few weeks.

## Data Understanding and Preparation
I will analyse Kings County's property sales datas in the past two year to build a regression model. There are approximately 21,000 sales in the past 2 years.
This is a good size for analysis.

The datat cleaning process will ensure the datas are in correct data types, checking missing value and fill it with approriate value.
Once datas are cleaned, I will separate them into 3 variables or features as follow for testing and validation in order to get the best model:

1. Continuous variables (A continuous variable can be of any value in a range, for example: sqft living and lot sizes)
2. Discrete variables (certain number of particular values that can be counted, for example: number of bedrooms)
3. Categorical variables (descriptive categories instead of numerical or measured categories, for example: zipcodes)

## Modelling
Upon reviewing the above datas and their value, here are my breakdown on the features or variables. So we can model it approriately on the next step using linear regression model to predict property prices based on below features:

Categorical: Waterfront, zipcode
Discrete: condition, grade, bedrooms, bathrooms, floors, view
Continuous: yr_build, yr_renovated, lat, long, ALL of sqft_

The data also split into a train data (75%) and a test data (25%) to ensure accuracy, also using random_state and shuffle to avoid any biases.

## Regression Results

1. Model 1: Build a base model based on 3 features that have the highest correlation to the price. However the R2 score is only 0.564. 
2. Model 2: Added 5 continuous features which bring the R2 score up to 0.756.
3. Model 3: Added 5 discrete features to Model 2, which bring the R2 score to 0.775 (Pretty good score with 13 features altogether)
4. Model 4: Using Recursive Feature Elimination method, the RFE picked 10 of the most important features and the score is on par with model 3 at 0.772
5. Final Model: Adding 2 more categorial features which increased the R2 score to 0.876

Here are some graphs for comparison (Base Model vs. Final Model):

![BEFORE MODELLING BASE VARS](https://user-images.githubusercontent.com/107485501/185570357-05a329d6-4f69-4c2c-bce8-e2aa5dbeddd0.png)
![AFTER MODELLING TRAIN SET](https://user-images.githubusercontent.com/107485501/185570385-3058a63d-e9fc-4f38-ad75-b9aa22028961.png)

Plotting data against predictions/final model to check on the accuracy:

![FINAL MODEL GRAPH ACTUAL VS PREDICTION](https://user-images.githubusercontent.com/107485501/185570507-6382c42f-6428-4ece-8ab4-d28729c67440.png)


