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
### Barplot for Saleprice and The Data Type with Objects

<img src="Assets/EDA 5.jpg" alt="Barplot for Saleprice and The Data Type with Objects"/><br>

### Distribution plot 
<img src="Assets/EDA 6.jpg" alt="Distribution plot "/><br>

# <a id="data-preprocessing">Data Preprocessing</a>
---

## Indentify Outlier
<img src="Assets/DP 1.jpg" alt="Indentify Outlier"/><br>
Total Missing Value 897 data or 61.4% from all data

## Indentify Duplicated Data
<img src="Assets/DP 4.jpg" alt="Indentify Duplicated Data"/><br>
We didn't find Duplicated data in this dataset

## Missing Value
<img src="Assets/DP 5.jpg" alt="Indentify Missing Value"/><br>
<img src="Assets/DP 2.jpg" alt="Indentify Missing Value"/><br>

**Scheme for Handling Missing Value :**
1. Simple Imputer with value 0 : LotFrontage, MasVnrArea, GarageYrBlt
1. Simple Imputer with value None : MasVnrType
1. Simple Imputer with value Modus : Electrical
1. Simple Imputer with value NA : Alley, BsmtQual, BsmtCond, BsmtExposure, BsmtFinType1, BsmtFinType2, FireplaceQu, GarageType, GarageFinish, GarageQual, GarageCond, PoolQC, Fence, MiscFeature

# Modeling and Evaluaton
---

we will compare 9 model and choose best 2 model for Hyperparameter Tuning
<img src="Assets/MaE 1.jpg" alt="Benchmark 9 Model"/><br>
Best 2 model is Gradient Boost and XGBoost
<img src="Assets/MaE 2.jpg" alt="Best 2 model"/><br>

# Hyperparameter Tuning
---

## **Compare Best 2 model After Tuning and Before Tuning**
<img src="Assets/HT 2.jpg" alt="Compare After Tuning and Before Tuning"/><br>
Than we will compare with regplot Gradient boost after tuning and before tuning
<img src="Assets/Comp 1.jpg" alt="Regplot Compare"/><br>
we choose Gradient Boost Before Tuning to Machine Learning

## **Compare Predict with Actual**
<img src="Assets/Comp 2.jpg" alt="Compare Pred with Act"/><br>

We decide to apply gradient boost before tuning to data test and save machine learning "sample_submission.csv"

# Conclusion
RMSE results show machine learning will 24216.4. we can conclude that when this model is used to predict house prices in Ames in the value range as trained on the model, the average estimate will miss about 24,216.4. but in fact this model has biggest miss 153,222. and R2 score 0.9, which means that the independent variable greatly affects the dependent variable
