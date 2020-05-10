# **SPARKIFY**  - User churn prediction
 This is a Capstone Project of the [Udacity Data Science Nanodegree](https://www.udacity.com/).   
Please see also my [Kaggle blog post](https://www.kaggle.com/chriskue/sparkify-user-churn-prediction) for a more detailed explanation of the project. 

## Content
- [Description](#description)
- [Requirements](#requirements)
- [Results](#results)
- [Licensing, Authors, Acknowledgements](#license)


# Description <a name="description"></a>
Sparkify is a fictional music streaming service just as Spotify.
The goal of this educational project is to analyze the log file and build a model to find customers who are very likely to stop using the service soon. More specifically, multiple models are implemented and compared against each other in order to measure performance and to find the best model in order to predict the user behavior. Using the F1-Score as measurement of performance therefore best reflects the accuracy and recall rate of the models. More informations on the F1-Score can be found on [Wikipedia](https://en.wikipedia.org/wiki/F1_score). With the most accurate model possible, it is then possible to send marketing offers in a targeted manner to prevent users from churn without spending to much money.

The data provided is the user log of the service, with demographic info, activities, timestamps etc.

# Requirements <a name="requirements"></a> 
-  Python 3
-  Pyspark
-  Pandas
-  Numpy
-  Matplotlib
-  Seaborn
-  re
-  datetime
-  functools

and Jupyter notebook

Important: 
The .json file (I used only a 128MB subset of the original dataset) is not included in this repo, but you can get it from my [Kaggle blogpost](https://www.kaggle.com/chriskue/sparkify-user-churn-prediction).

# Results <a name="results"></a> 
From the analysis of the small subset of data, the following  factors could be identified as the most important in the evaluation of a possible user churn. 

Top 3 factors:
- time of membership
- the number of 'thumbs down'
- number of friends.  

With the chosen features the following results could be achieved with the different models. With a F1-Score of 0.97, the GBT Classifier delivers a pretty impressive result, but a transfer and validation with the entire data set is pending.<br/>

| Model |Accuracy |	Precision |	Recall 	|F1-Score|
|---:	|----:	|---:	|---:	|---:	|
|Logistic Regression |	0.89| 	0.91 |	0.31 |	0.46|
|Descission Tree |	0.94| 	0.86| 	0.71 |	0.78|
|Random Forest Classifier |	0.95 |	1.0 |	0.68 |	0.80|
|**GBT Classifier** |	**0.99** |	**1.0** |	**0.95**| 	**0.97**|

# Licensing, Authors, Acknowledgements <a name="license"></a>
The dataset was provided by Udacity https://www.udacity.com

A lot of informations from the udacity course and https://sparkbyexamples.com/category/spark/ have been used.   
If other sources are used, they are referenced in the code.

Licensed under the MIT License.