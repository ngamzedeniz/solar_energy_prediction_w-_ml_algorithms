# Solar_Energy_Prediction_w'_Machine_Learning_Algorithms

Motivation For This Project:


Turkey is a very valuable country in terms of solar energy potential. So much so that it is the country with the most sunshine duration in Europe annually.

Aksaray province, which is the study area, is one of the provinces of Turkey with a high sunbathing potential, and having a flat land can make this province a solar panel paradise.

Forecasting solar energy is an interdisciplinary subject in terms of renewable energy investments, a better understanding of our natural ecosystem, and understanding how the energy cycle is in the world.

Short and long term solar energy forecasting has an important place in the energy market. 


Expore & Process DATA

1. Retrieve

The data includes maximum humidity, minimum humidity, relative humidity, wind magnitude, dew point temperature, minimum maximum and actuel temperature, minimum, maximum and actuel sunshine duration and solar radiation of Aksaray province for the years 2017-2019, sunrise time angle.

2. Clean & Explore

Values with zero radiation were deleted so that the model could work with more meaningful data and the data set was normalized. The purpose of normalizing is to make the model work better, and this method have been used in many studies. (Karasu et al, 2017; Alsafadi and Filik, 2020)

3. Prepare / Transform

The hourly data converted into daily data, in order to obtain the total daily radiation.
Temperature and sun duration converted into average, maksimum and minimum values of days, while other variables converted into daily average. 
 (ws) and zenith angles were calculated and added to the data set. There has been proved that zenitg angle imporved the model performance of predicting solar radiation (Fatemi and Kuh, 2013).



Modeling

1. Develop & Train Model

XGBoost, Random Forest and Knn models have used for predict solar radiation.



2. Validate & Evaluate Model

In this study, the model results evaluated with statistical metrics such as R (Pearson Corelation Coefficient), RMSE (Root Mean Squared Error), MAE (Mean Absolute Error). With the Random Forest model, the order of importance of the meteorological variables in estimating the solar radiation was determined, data were extracted from the variable with the lowest order of importance to the variable with the highest order, and RMSPE, MAPE and R values in each step were calculated, how the model reacted with various meteorological variables tested.

Results showed that XGBoost model have better performance predicting solar radiation compared to other models. Is has been also showed that increase of various meteorological variable inputs improve the model results. Results with higher error were observed before the data were normalized. Normalized data was run on all models. For this, the preprocessing function of the sklearn library is used. 


Sources:

Karasu, S., Altan, A., Sarac, Z., & Hacioglu, R. (2017). Prediction of solar radiation based on machine learning methods. The journal of cognitive systems, 2(1), 16-20.

ALSAFADI, M., & FİLİK, Ü. B. HOURLY GLOBAL SOLAR RADIATION ESTIMATION BASED ON MACHINE LEARNING METHODS IN ESKISEHIR. Eskişehir Technical University Journal of Science and Technology A-Applied Sciences and Engineering, 21(2), 294-313.

Fatemi, S. A., & Kuh, A. (2013, December). Solar radiation forecasting using zenith angle. In 2013 IEEE Global Conference on Signal and Information Processing (pp. 523-526). IEEE.










