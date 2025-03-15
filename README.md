# Corn-Spot-Price-LSTM



**My project is an LSTM that estimates corn price fluctuations.**

The problem I will be trying to solve and learn more about is one that is pretty niche to the field that intersects economic theory with fundamental data 
science and machine learning.For my research project I will be utilizing an LSTM trained on weather data as well as wheat spot price data to try and predict the 
corn spot price. The goal of my model is to accurately quantify the impact of how weather variables (wheat_spot_price + max_temperature + ice_days + 
biologically_effective_degree_days + heavy_rain_rain) will influence the spot price of corn. One of my input variables or x’s will also be the
time series spot price of wheat. The reason I am doing this is because wheat and corn are historically very highly correlated and wheat 
can predict a certain amount of corn price fluctuation.


**Data:**

https://www.alphavantage.co/ (integrated API, for corn and wheat historical global prices)

https://www.ecmwf.int/en/forecasts/dataset/ecmwf-reanalysis-v5 (For extracting climate weather data)

https://cds.climate.copernicus.eu/datasets/sis-agroclimatic-indicators?tab=overview (data for agricultural climate indicators, filtered for midwest)

**Instructions on how to train model:**

You don't need to! The model has pretrained weights you can access through pretrained_model.ipynb, however, to run it yourself either go to Demo_Notebook.ipynb which contains a fully implemented version or train_model.ipynb, which has all the relevant training code. To access the data get access to Talapas and use the base_dir path to access datasets from dataloader.ipynb.


**Metrics to Evaluate Model:**

To evaluate this model I will use Mean Squared Error as the criterion.


**Model Predictions:**

![Results](/results4.png)
![Results](/results1.png)
![Results](/results2.png)
![Results](/results3.png)

**Model Limitations:**

This model is used to predict only the spot price of corn, ideally it would be best for the model to be used to predict corn and wheat accurately so it can capture the
divergence and convergence of both prices. Another issue with the model is it doesn't account for macroeconomic factors such as GDP growth, interest rates, inflation, etc.
Which can also explain variance in the price of corn as well. Another limitation to the preditions is, though very well fit to the training data, when evaluated on new data
such as the train or validation data, there seems to be a bit of a lag on the predictions when compared to the true price.







