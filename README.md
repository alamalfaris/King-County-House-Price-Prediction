# King County House Price Prediction

![Image of KC](https://github.com/alamalfaris/King-County-House-Price-Prediction/blob/main/kc.jpg)

## Background
> - King County is located in the U.S. state of Washington. The population was 2,252,782 in the 2019 census estimate, making it the most populous county in Washington, and the 12th-most populous in the United States. The county seat is Seattle, also the state's most populous city.
> - How much reasonable price for house in King County?

## Goal
> Predict a reasonable house price in King County

## About Data
> We got this data from Kaggle: https://www.kaggle.com/harlfoxem/housesalesprediction

### Feature Description
- id : Unique id for each home sold
- date : Date of the home sale
- price : Price of each home sold
- bedrooms : Number of bedrooms
- bathrooms : Number of bathrooms, where .5 accounts for a room with a toilet but no shower
- sqft_living : Square footage of the apartments interior living space
- sqft_lot : Square footage of land space
- floors : Number of floors
- waterfront : A dummy variable for whether the apartment was overlooking the waterfront or not
- view : An index from 0 to 4 of how good the view of the property was
- condition : An index from 1 to 5 on the condition of the apartment
- grade : An index from 1 to 13, where 1-3 falls short of building construction and design, 7 has an average level of construction and design, and 11-13 have a high quality level of construction and design
- sqft_above : The square footage of the interior housing space that is above ground level
- sqft_basement : The square footage of the interior housing space that is below ground level
- yr_built : The year the house was initally built
- yr_renovated : The year of the house's last renovation
- zipcode : What zipcode area the house is in
- lat : Latitude
- long : Longitude
- sqft_living15 : The square footage of interior housing living space for the nearest 15 neighbors
- sqft_lot15 : The square footage of the land lots of the nearest 15 neighbors

## Table of Content
- Data Exploration
- Data Analysis and Data Visualization
  - Univariate
  - Bivariate
- EDA Conclusion
- EDA Recommendation
- Data Preparation
- Base Model
- Feature Engineering 1
- Feature Engineering 2
- Hyperparameter Tuning
- ML Conclusion
