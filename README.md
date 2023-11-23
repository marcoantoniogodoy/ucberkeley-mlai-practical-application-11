# Practical Application Assignment 11: What drives the price of a car?

## Overview: 
This repository contains a data analysis performed by Marco A. Godoy as part of the Practical Application Assignment 11 for the UC Berkeley Professional Certificate in ML/AI Program (2023).

For a link to the Jupyter Notebook, please click here:
https://github.com/marcoantoniogodoy/ucberkeley-mlai-practical-application-11/blob/main/prompt.ipynb

Contact Information:
https://www.linkedin.com/in/marco-antonio-godoy

## Data:
In this application, we explore a dataset from kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. The goal for this analysis is to understand what factors make a car more or less expensive. As a result of the analysis, recommendations are provided to the client -- a used car dealership -- as to what consumers value in a used car.

## Summary of the results obtained from the analysis
As requested, we have performed a comprehensive analysis on the vehicle dataset provided, with the goal of identifying the most important features that determine the price of an used car.

The dataset contained a total of 426,880 samples with 18 distinct features. However, during the data exploration phase of our analysis we found that several of these samples contained incomplete information. Therefore, to avoid compromising the quality of our results, we focused only the samples that contained complete data. Additionally, we decided to exclude certain fields such as id and VIN since we believe they are not correlated with the price of an used car. Moreover, there were fields such as region and car model that we also decided to exclude, mainly because their structure was too fragmented. Lastly, we also decided exclude the "state" to limit the scope of the problem.

Once we completed the data exploration and preparation phases, we proceeded to the modeling phase. In this phase we split the data into two groups called "Train" and "Test" respectively. Then, we applied several machine learning techniques over several iterations that used different combination of features to predict the price. These processed resulted in 9 trained models. Then, we evaluated the quality of these models using a cross validation technique where we compared the difference between the actual data and the data predicted by the model. From these 9 models we chose the top three performing models and compared the most important features they use for the estimation of price.

Based on the results of the top three selected models and after finding the common features between them, we concluded that the the most relevant features when determining the price of used cars are "fuel", "type", "year", "cylinders" and "drive".

## Next steps and Recommendations:
As supported by the results ot our analysis, we conclude that the most important features when determining the price of an used car are "fuel", "type", "year", "cylinders" and "drive". However, as we mentioned the dataset provided contained incomplete data in several entries. This resulted in a data loss of about ~80% of the original dataset. Additionally, the location data provided could not be geodecoded due to the lack of structure of the region field. 

However, even with the such limitations, after our data exploration and data reformatting, we feel confident that the quality of the resulted model led to conclusive results. 
