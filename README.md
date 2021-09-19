# TedTalks_Views_Prediction_Regression

## Problem Statement:

TED is devoted to spreading powerful ideas on just about any topic. These datasets contain over 4,000 TED talks including transcripts in many languages
Founded in 1984 by Richard Salman as a nonprofit organization that aimed at bringing experts from the fields of Technology, Entertainment, and Design together.
TED Conferences have gone on to become the Mecca of ideas from virtually all walks of life. As of 2015, TED and its sister TEDx chapters have published more than 2000 talks for free consumption by the masses and its speaker list boasts of the likes of Al Gore, Jimmy Wales, Shahrukh Khan, and Bill Gates.

## Objective: 
To build a predictive model, which could help in predicting the views of the videos uploaded on the TEDx website.


## Dataset Information

* Number of observations: 4,005
* Number of features: 19

## Features information:
The dataset contains features like:


* talk_id: Talk identification number provided by TED
* title: Title of the talk
* speaker_1: First speaker in TED's speaker list
* all_speakers: Speakers in the talk
* occupations: Occupations of the speakers
* about_speakers: Blurb about each speaker
* recorded_date: Date the talk was recorded
* published_date: Date the talk was published to TED.com
* event: Event or medium in which the talk was given
* native_lang: Language the talk was given in
* available_lang: All available languages (lang_code) for a talk
* comments: Count of comments
* duration: Duration in seconds
* topics: Related tags or topics for the talk
* related_talks: Related talks (key='talk_id',value='title')
* url: URL of the talk
* description: Description of the talk
* transcript: Full transcript of the talk

## Target Variable
* 'views': Count of views

## Project Work flow

1. Importing Libraries and loading dataset
2. EDA on features 
3. Feature Engineering
4. Missing value treatment 
5. Outlier treatment
6. Feature selection
7. Fitting the regression models and HyperParameter Tuning
8. Comparison of Models
9. Final selection of the model
10. Conclusion


### Models used:
1. Linear Regression
2. Random Forest Regressor
3. XGBoost Regressor


## Conclusion:

Starting with loading the data then  performed Exploratory data analysis on various features, then carried out feature engineering and encoding of categorical columns, handled missing values in the dataset, dealt with outliers present in the dataset , performed transformations like log, sqrt and boxcox on numerical features to convert them to gaussian distribution, then carried out feature selection and build various models like Linear Regression, Random Forest Regressor and XGBoost Regressor. Evaluated these models on various metrics like MSE, RMSE, MAE ,R2 score and Adjusted R2 score. Finally selected the best model out of these.

In all these models our errors have been in the range of 2,00,000 which is around 10% of the average views. The model has been able to correctly predict views 90% of the time. After hyper parameter tuning, we have prevented overfitting and decreased errors by regularizing and reducing learning rate. Given that only have 10% errors, our models have performed very well on unseen data due to various factors like feature selection, correct model selection. 
After evaluating the performance of all the models, the best model is Random Forest Regressor based on MAE because MAE is linear and robust to outliers.

