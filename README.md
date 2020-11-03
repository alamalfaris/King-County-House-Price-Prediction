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

## EDA Conclusion
- Houses with price above median mostly are located in the center and nearby of city
- Houses with price under median mostly are located far from city
- Houses with 0 - 3 bedrooms mostly under median price
- Houses with more than 3 bedrooms mostly above median price
- Houses with 0 - 2 bathrooms mostly under median price
- Houses with more than 2 bathrooms mostly above median price
- Middle-low (225 - 644 sqft) and Middle-up (645 - 1291 sqft) houses mostly under median price
- Luxury (> 1291 sqft) houses mostly above median price
- Houses with 1 floor mostly under median price
- Houses with more than 1 floor mostly above median price
- Houses without waterfront almost balance between number of under and above median price
- Houses with waterfront mostly above median price
- Houses without view mostly under median price
- Houses with except very bad view mostly above median price
- Houses with very bad, bad, and very good condition mostly under median price
- Houses with best condition mostly above median price
- Houses with good condition are almost balance between under and above median price
- Houses with bad quality and average quality mostly under median price
- Houses with high quality mostly above median price
- Houses without basement mostly under median price
- Houses with basement mostly above median price
- House with basement mostly luxury house (>1292 sqft)
- Houses that renovated mostly above median price
- Houses that not renovated mostly under median price
- Number between young and old house almost balance
- Young houses mostly above median price
- Old houses mostly under median price

## EDA Recommendation
- Houses that are located in the center and nearby city can priced above median
- Houses that are located far from city can priced under median
- Houses with 0 - 3 bedrooms can priced under median price
- Houses with more than 3 bedrooms can priced above median price
- Houses with 0-2 bathrooms can priced under median price
- Houses with more than 2 bathrooms can proced above median
- Middle-low and Middle-up houses can priced under median
- Luxury houses can priced above median
- Houses with 1 floor can priced under median price
- Houses with more than 1 floor can priced above median price
- Houses without waterfront can priced under or above median price depends on other variables
- Houses with waterfront can priced above median price
- Houses without view can priced under median price
- Houses with view can priced above median price
- Houses with very bad, bad, and very good condition can priced under median price
- Houses with good and best condition can priced above median price
- Houses with bad and average quality can priced under median price
- Houses with high quality can priced above median price
- Houses without basement can priced under median price
- Houses with basement can priced above median price
- Houses that not renovated can priced under median price
- Houses that renovated can priced above median price
Young (<= 40 years old) houses can priced above median price
Old (more than 40 years old) houses can priced under median price

## ML Conclusion
- Ridge:
  - Best score from ridge is still Ridge + Polynomial + price feature transformation, fit in 0.82
- KNN:
  - Best score from KNN is KNN + Hyperparameter Tuning, test score reach 0.85 although the score are overfitting among train and test
- XGBoost:
  - Best score from XGB is XGBoost + Hyperparameter Tuning, test score reach 0.91 although the score are overfitting among train and test. Also this is highest test score than other algorithms
