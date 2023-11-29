# Module 21 Report

## Overview of the Analysis

The purpose of this analysis is to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. The data used for this analysis is composed of more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset, there are a number of columns that capture metadata about each organization such as the following:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

## Results


- The target for our model is the 'IS_SUCCESSFUL' column which indicates whether the money was used effectively.
- The features for our model are all the columns except 'IS_SUCCESSFUL', 'EIN', and 'NAME'.
- The 'EIN' and 'NAME' columns were removed from the input data because they are identification information and do not contribute to the model's predictive ability.
- The categorical variables in the data were converted to numerical using one-hot encoding.
- The data was split into training and testing datasets. The training data was scaled using the StandardScaler from sklearn.
First Model

- The first neural network model was designed with two hidden layers. The first hidden layer has 80 neurons and the second hidden layer has 30 neurons. The 'relu' activation function was used for the hidden layers and the 'sigmoid' activation function was used for the output layer.
- The model was trained for 100 epochs.
- The model's performance was evaluated using the testing data. The model achieved an accuracy of approximately 72.5%.
Optimized Model

- The optimized neural network model was designed with four hidden layers. The first hidden layer has 14 neurons, the second hidden layer has 28 neurons, the third hidden layer has 42 neurons, and the fourth hidden layer has 56 neurons. The 'relu' activation function was used for the hidden layers and the 'sigmoid' activation function was used for the output layer.
- The model was trained for 100 epochs.
- The model's performance was evaluated using the testing data. The model achieved an accuracy of approximately 75.2%.

## Summary

The optimized deep learning model was able to achieve a higher accuracy than the first model. This suggests that the additional complexity in the optimized model helped it to better capture the patterns in the dataset.

For future work, other models such as a Random Forest Classifier could be explored. This model could potentially perform better because it can capture non-linear relationships between features and the target variable, and it does not require feature scaling. The Random Forest model is also less prone to overfitting compared to a deep learning model.