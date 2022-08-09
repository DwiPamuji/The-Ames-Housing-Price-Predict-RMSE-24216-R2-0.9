# The Ames Housing Price predict
---
by [Dwi Pamuji Bagaskara](https://github.com/DwiPamuji)

Gambar???


# Contents
---

1. [Business Problem Understanding](#business-problem-understanding)
1. [Data Understanding](#data-understanding)
1. [Exploratory Data Analysis](#exploratory-data-analysis)
1. [Data Preprocessing](#data-preprocessing)
1. [Modeling and Evaluation](#modeling-and-evaluation)
1. [Hyperparameter Tuning](#hyperparameter-tuning)
1. [Compare Model Predict with Actual](#compare-model-predict-with-actual)
1. [Test Machine Learning](#test-machine-learning)
1. [Conclusion](#conclution)

# <a id="business-problem-understanding">Business Problem Understanding</a> 
---

## Context
House is one of the primary needs, as a customer One of the difficulties in owning a house is determining the price of the house based on the facilities provided. Is the price of the house in accordance with the existing facilities or is the price too expensive. For home sellers, determining the ideal house price for sale is also very important. that sellers don't lose their sales, or no one want to buys the house cause too expensive

## Problem Statement
Determine the price of the house whether the price is appropriate

## Goals
help customers to predict the price of the house they want to buy or want to sell

## Analytic Approach
so what we need to do is analyze the data and find patterns between houses. then we will make machine learning regression for predict house price. **which will be useful for customers to determine the price of the house they want to buy or what they sell**

## Metric Evaluation
Evaluation metrics to be used are RMSE and R-Squared, RMSE is the mean value of the square root of the error, means the model is more accurate in predicting the price according to the limitations of the features used. R-squared is used to determine how well the model can represent the overall variance of the data. The closer to 1, the more fit the model is to the observation data.

# <a id="data-understanding">Data Understanding</a>
---

Dataset are obtained from: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data

## Data Fields Present in the Dataset

MSSubClass: Identifies the type of dwelling involved in the sale.	

        20	1-STORY 1946 & NEWER ALL STYLES
        30	1-STORY 1945 & OLDER
        40	1-STORY W/FINISHED ATTIC ALL AGES
        45	1-1/2 STORY - UNFINISHED ALL AGES
        50	1-1/2 STORY FINISHED ALL AGES
        60	2-STORY 1946 & NEWER
        70	2-STORY 1945 & OLDER
        75	2-1/2 STORY ALL AGES
        80	SPLIT OR MULTI-LEVEL
        85	SPLIT FOYER
        90	DUPLEX - ALL STYLES AND AGES
       120	1-STORY PUD (Planned Unit Development) - 1946 & NEWER
       150	1-1/2 STORY PUD - ALL AGES
       160	2-STORY PUD - 1946 & NEWER
       180	PUD - MULTILEVEL - INCL SPLIT LEV/FOYER
       190	2 FAMILY CONVERSION - ALL STYLES AND AGES

MSZoning: Identifies the general zoning classification of the sale.
		
       A	Agriculture
       C	Commercial
       FV	Floating Village Residential
       I	Industrial
       RH	Residential High Density
       RL	Residential Low Density
       RP	Residential Low Density Park 
       RM	Residential Medium Density
       
       
For Detail you can see in data_description.txt'

# <a id="exploratory-data-analysis">Exploratory Data Analysis</a>
---

## EDA General
### Persentage House Zone

<img src="Assets/EDA 1.jpg" alt="Persentage House Zone"/><br>

### Persentage Sale Type

<img src="Assets/EDA 2.jpg" alt="Persentage Sale Type"/><br>

### Persentage Sale Condition

<img src="Assets/EDA 3.jpg" alt="Persentage Sale Condition"/><br>

### House Fasilities

<img src="Assets/EDA 4.jpg" alt="Persentage Sale Type"/><br>

## EDA Data Train
### barplot for saleprice and the data type with objects

<img src="Assets/EDA 5.jpg" alt="Persentage Sale Type"/><br>


