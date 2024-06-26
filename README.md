# Exploring the Drivers of Modern Slavery

Assignment 2 for the Analytics Practicum I Course of AUEB's MSc in Business Analytics.

Even though slavery is illegal, forty million people are estimated to live under some form of modern slavery across the globe. These forms of modern slavery include a wide variety of practices such as forced labour, debt bondage, forced marriage, sexual exploitation, bonded labour, and human trafficking.

Researchers have been trying to estimate the prevalence of modern slavery, as well as factors that can help with this prediction. Machine Learning techniques can help in this endeavour, as has been shown in the following publication:

* Lavelle-Hill, R., Smith, G., Mazumder, A. et al. Machine learning methods for "wicked" problems: exploring the complex drivers of modern slavery. Humanities and Social Sciences Communications 8, 274 (2021). https://doi.org/10.1057/s41599-021-00938-z

Read the paper and familiarize yourself with the methodology followed by the authors.

## Questions
### Q1: Data Preprocessing

The original data contains a single dependent variable, country level slavery prevalence estimates, converted to a percentage of the population. This included prevalence estimates for 48 unique countries over 2016 and 2018. As you will find out by reading the paper, the data had missing values, which the researchers proceeded to fill using assumptions and imputation methods.

You will start with the [unimputed data](training.csv) and will fill in the missing values using the assumptions taken by the researchers. Regarding imputation, you will use the imputation methods afforded by scikit-learn.

### Q2: Slavery Estimation Using All Features

You will train three models using the imputed data to predict slavery prevalence:

* A linear regression model.

* A decision tree.

* A random forest (any variant).

You will notice that the slavery indicator may refer to 2016 or 2018, which means that you must train your model on data up to 2016 to predict slavery prevalence for 2016 and on data between 2016 and 2019 to predict slavery prevalence for 2018 (we assume that 2019 data apply to 2018).

You will evaluate your model using the [Out of Sample data](oos_data.csv). You will use the Mean Average Error (MAE) as the evaluation metric.

Concerning linear regression, you can also use ridge regression and lasso regression. Comment on the importance of various features on predicting slavery prevalence.

### Q3: Slavery Estimation with Theory-based Features

Apart from the full features set, the researchers used the same models as in Q2 using a subset of 35 features. Train your models using the subset and then evaluate again using the [Out of Sample data](oos_data.csv) (in the reduced features set). Comment on the importance of various features on predicting slavery prevalence.

### Q4: Slavery Estimation with PCA-derived Features

You will use Principal Component Analysis (PCA) in order to reduce the full set of features to six features. Try to interpret the six derived features. Then, train and evaluate your models on the PCA-derived features. Comment on the importance of each feature on predicting slavery prevalence.

## Submission Instructions

You will submit a Jupyter notebook that will contain all your code, data, and analysis. Ensure that the notebook will run correctly in a computer that is not your own. That means, among other things, that it does not contain absolute paths. Remember that a notebook is not a collection of code cells thrown together; it should contain as much text as necessary for a person to understand what you are doing.

## Honor Code

You understand that this is an individual assignment, and as such you must carry it out alone. You may seek help on the Internet, by Googling or searching in StackOverflow for general questions pertaining to the use of Python,  libraries, and idioms. However, it is not right to ask direct questions that relate to the assignment and where people will actually solve your problem by answering them. You may discuss with your fellow students in order to better understand the questions, if they are not clear enough, but you should not ask them to share their answers with you, or to help you by giving specific advice.
