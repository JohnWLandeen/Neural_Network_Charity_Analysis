# Neural_Network_Charity_Analysis


## Overview

The purpose of this Neural Networking analysis besides creating a binary classifier that determines whether an organization applicant will be successful or not if the company Alphabet Soup funds them, is to build the most effective model with the highest Accuracy and lowest loss scores possible. In the AlphabetSoutCharity jupyter notebook, the dependant variable feature 'IS_SUCCESSFUL' is determined by all other features either standard scaled if numeric or binarized with pandas get_dummies if categorical. For training, a sequential keras neural network model is established with two dense hidden layers sporting the famed non-linear activation function RELU and an output layer with the Sigmoid activation function. The AlphabetSoupCharity_Optimization notebook makes further attempts at honing accuracy and loss scores by increasing dense layers and changing node counts in layers. 

## Results

* Data Preprocessing

   * The data target is the dependant variable 'IS_Successful'.

   * The independant variables in the data are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.

   * Unnecessary features for our data that are dropped are the ID number known as EIN and the NAME feature that denotes the name of each club.

   * Binning occurs for the feature APPLICATION_TYPE with all unique values with a count less than one hundred and for the feature CLASSIFICATION with all unique values under nineteen hundred.

   * StandardScaler is applied to all numeric features and pandas get_dummies is applied to all categorical features resulting in a multitude of binarized features.

* Compiling, Training, and Evaluating the Model

   * For the third and most effective model in the AlphabetSoupCharity_Optimization notebook, there are four hidden RELU layers with each numbered at eigth neurons. The final output layer has one neuron with the Sigmoid activation function. This was done with the intent to reverse the common funneling method in nueral networking.

   * The ideal target performance of seventy five percent accuracy was not met through optimization. The closest score was recorded at seventy two point five three percent with loss at about fifty five percent.

   * The models performance had small incremental increases with the sequential inclusion of more layers.


## Summary

The deep neural networking models seem to have a remarkably high rate of classifying negative as opposed to positive. Perhaps most organizations don't meet the expectations for AlphabetSoups standards and end up negative in the binary results. Or the data wasn't found to be interpretable to the extent that it needed to be for effective classification with Neural Networking models. Other classification models could have better interpretation of the data for making proper predictions such as a RandomForest Classifier or SVM model. These models may have better methods for interpreting our data and creating more accurate positives in the case of this particular dataset.