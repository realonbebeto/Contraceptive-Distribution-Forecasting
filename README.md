# Contraceptive-Distribution-Forecasting

* Analysed Contraceptive Distribution for Sites in Ivory Coast
* Processed and transformed Given Data to fit a recognizable Time Series Format
* Transformed Features 
* Experimented with Neural Network Configuration 

## Code and Resources Used 
**Python Version:** 3.8  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, joblib, tensorflow  
**Paper Inspiration:** https://www.hindawi.com/journals/complexity/2020/6622927/
## Data Cleaning and Processing
After collecting the data, I cleaned and reformated it up so that it was usable for our model. I made the following changes and created the following variables:

*	Ignored other stock related features
*   Generated zero value data for missing products across the regions
*	Ordinally Encoded the site_code and product_code features
*	Robust Scaled the site_code, product_code and stock_dostributed features 

## Model Building 

I split the data into train and tests sets with a test size of about 20%.   

I tried a configuration of various layers from an inspiration of a paper and evaluated them using MAE(training) and RMSE(final result). I chose accuracy RMSE because it is punishes outliers more.

## Model performance

The model performed well but had a challenge for outliers.
*   **CNN-LSTM Based Model**: Test RMSE = 11.61

## Prediction

In this step, I predicted 3 months into the future(2019 Jul, Aug, Sept) to get the feel of how contraceptive distribution will be for the various 156 sites and 10 products.