# Price of a Used Car
GitHub Repository for work done on Professional Certificate in Machine Learning and Artificial Intelligence - Feb 2024

# Practical Application Assignment 11.1: What Drives the Price of a Car?

**Contents**

 * [Introduction](#Introduction)
 * [How to use the files in this repository?](#how-to-use-the-files-in-this-repository)
 * [Business Understanding](#Business-Understanding)
 * [Data Understanding](#Data-Understanding)
 * [Data Preparation](#Data-Preparation)
 * [Regression Model](#Regression-Model)
 * [Findings](#Findings)
 * [Next steps and Recommendations](#Next-steps-and-Recommendations)
 * [License](#license)
 
## Introduction

This repository contains the Jupyter Notebook for the Application Assignment 11.1. This takes a sample jupyter notebook to complete the exercise to analyse Kaggle used car data in [vehicles.csv](./data/vehicles.csv) file in the data folder of this repository to build a machine learning application that evaluates if vehicles features like Odometer, Year, Model etc. can be used to determine used car prices for the car dealership. The primary benefit is to help identify cars that align best with customer expectations.

## How to use the files in this repository?

The notebooks are grouped into the following categories:
 * ``data`` – vehicles.csv data file from Kaggle Machine Learning dataset repository used in the notebooks
 * ``images`` – Image files used in Notebook and Project Description
 * ``notebook`` – Used_Cars_Analysis.ipynb


## Business Understanding

The business objective is to identify key features for used car prices based on the dataset provided so that Car Dealers and their Sales Team can use these key features to understand the cars that they need to have in their inventory to increase sales.

For this application, we used a machine learning process which starts with gathering the data, cleaning, preparing and manipulating the data, training the model then testing to get predicted values and measure model accuracy. As part of the life cycle, additional data from sales should be used on an on-going bases to “improve” the model which leads to higher prediction accuracy on the factors that  consumers are looking for in used cars. 

## Data Understanding

The data had many anomalies and wasn't clean. The year ranged from 1900 to 2022 and the cost of the vehicle ranged from 0 to $3.8 Billon dollars.

The data was cleaned to ensure the model is not impacted by these huge anomalies.

## Data Preparation

Summary of the Data Preparation is as follows:
- Remove records with Zero Prices and Odometer values
- Remove records where some of the factors are not populated
- Drop a number of factors (i.e., VIN, id, region etc.) that are not significant in user car price determination
- Review and remove the other factors (i.e., state, paint color, manufacturer, transmission etc.) and check if they have an impact on car price based on the provided data
- Filtering the data based on year on manufacture greater than 1960 and with prices in the range of $2,000 and $200,000.


## Regression Models

I ran a number of models to understand the primary factors affecting the overall price of a car. 

The XGBoost boost model showed the best results with a r2_score of **0.813**

This model was further tuned through hyperparameter tuning and GridSearch with a final optimized value of **0.842**.


## Findings

In testing these models with the inputs, we observed the following for used car prices:

**- The Used Car Prices are most influenced by Odometer Readings and the Year of manufacturer.The most recent the year of the manufacturer and lower Odometer readings drive the maximum prices and are most preferred by the consumers.**
**- Additional factors impacting the decision is car type (sedan is preferred) with gas as Fuel Type.**

## Next Steps and Recommendations

**The used car dealerships would benefit the most by having an inventory of cars (sedan types) with gas fuel, year range closer to 2020 with a low Odometer Reading.**

**Next Steps**
- To run analysis where multiple factors could be at play for example color, state or condition that could not be analysed as part of this exercise.
- To validate using additional models that could be driven by Deep Learning to explore additional features that might be unexplored using these traditional techniques.
  
## License

Open source projects are made available and contributed to under licenses that include terms that, for the protection of contributors, make clear that the projects are offered “as-is”, without warranty, and disclaiming liability for damages resulting from using the projects.
