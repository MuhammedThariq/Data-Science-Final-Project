Forecasting Nitrous Oxide Emission using Ensemble Machine Learning approach

Objective :

The objective of this research is to develop a method that is capable of predicting the amount of nitrous oxide emissions that are produced by a number of different countries. For the purpose of predicting the emission of nitrous oxide, a multivariate forecasting approach is utilized. This method takes into consideration a variety of other elements, such as the consumption of fertilizers and the surface temperature of these countries. A method known as ensemble machine learning (EML) is utilized in order to forecast the emission of nitrous oxide. This method involves the incorporation of two models, including SARIMAX and LSTM. The EML approach will be combined with both open loop and closed loop forecasting architecture to examine how the performance varies in terms of computational efficiency and prediction accuracy.

Data used :

The necessary data for this study has been gathered from the "Our World in Data" platform. For my research, I have gathered three crucial datasets: nitrous oxide emissions, nitrogen fertilizer consumption, and surface temperature. The  data consists of the country's name, country code, year, and corresponding value. 

nitrous-oxide-emission.csv - Raw data showing the annual nitrous oxide emission across different countries.

nitrogen-fertilizer-application-per-hectare-of-cropland.csv - Raw data showing the annual consumption of fertilizers across different countries.

average-monthly-surface-temperature.csv - Raw data showing the average monthly surface temperature across different countries.

forecast_data.xlsx -  Pre-processed dataset merging all the three raw datasets. Used for exploratory data analysis.

clustered_forecast_data.xlsx - Clustered dataset with country cluster obtained from time series K-means clustering. Used for model development and training.

Data preprocessing :

The data preprocessing  is done in the 'data_preprocessing.ipynb' file. This includes treating mull values and managing outliers in all the three datasets. Finally, the datasets were merged into a single dataset and was exported as an excel file.

Exploratory Data Analysis :

Exploratory data analysis  is done in the 'Exploratory_data_analysis.ipynb' file. This includes identifying the correlation between nitrous oxide emission and other factors including fertilizer consumption and surface temperature. This analysis helped in using these features as exogenous variables during forecasting. The countries where clustered based on their trend in nitrous oxide emission using time serieas K-means clustering algorithm. Dynamic Time Wrapping was employed in order to achieve this. This clustering technique helped in developing models specifically designed for that cluster since different countries will be exhibiting different trend in nitrous oxide emission.

Forecast :

Forecasting part is done in the 'Forecast.ipynb'. Two countries namely China and US were selected representing each cluster to train and test the model. SARIMAX and LSTM models were created for each cluster and initial forecasting was performed using these models. Later EML approach was utilized by combining both models using Average EML and Stacking EML methods. Finally the EML approach was trained in both open loop and closed loop forecasting architecture to examine how the performance varies in terms of computational efficiency and prediction accuracy.
