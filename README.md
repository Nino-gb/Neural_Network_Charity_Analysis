# Neural Network Charity Analysis

## Overview 

From Alphabet Soup’s business team, we received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

With our knowledge of machine learning and neural networks, we will use the features in the provided dataset to  create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

The project consists of three technical analysis :

1. Preprocessing Data for a Neural Network Model 

2. Compile, Train, and Evaluate the Model 

3. Optimize the Model 

AlphabetSoupCharity.ipynb

Optimize the Model AlphabetSoupCharity_Optimation.ipynb


## Results

### Data Preprocessing

- We build the model using tensorflow.kras.models.Sequential and tensorflow.kras.models.Dense

- We used "IS_SUCCESSFUL" column as a Target variable 

- The model features are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS,STATUS and ASK_AMT.

- We have removed the following columns 'EIN', 'NAME', from DataFrame

### Compiling, Training, and Evaluating the Model

-Our first deep-learning neural network model was made of two hidden layers with 80 and 30 neurons, first and second activation function was with relu and the output activation was sigmoid generating an accuracy of 70%. Our model accuracy is under 75%. This is not a satisfying performance to help predict the outcome of the charity donations. Therefore,  we will perform steps to try and increase model performances 

#### First Attempt : Removed some STATUS AND ASK_AMT and we end up with a 63% accuracy

#### Second Attempt : We changed the first two activation function to tanh and the outlayer function to relu with a 62% accuracy

#### Third Attempt: Decrease two hidden layers with 46 and 20 neurons and the result was a 61% of accuracy. 

After three attempts, I wasn't able to generate a predictive accuracy higher than 75% and the optimization methods employed did not caused significant improvement.
