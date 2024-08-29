### deep-learning-challenge
## Overview of the Analysis

The purpose of the analysis was to create a tool for the nonprofit foundation Alphabet Soup that can help it select the applicants for funding with the best chance of success in their ventures. With machine learning and neural networks and a CSV of more than 34000 rows of data, a binary classifier was created to predict whether applicants will be successful if funded by Alphabet Soup.

## RESULTS

# Data Preprocessing

This data set’s target variable was IS_SUCCESSFUL. A data value of 0 implies no, and a data value of 1 implies yes.

This data set’s variable features include:
* NAME
* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* STATUS
* INCOME_AMT
* SPECIAL_CONSIDERATIONS
* ASK_AMT

The variable EIN was removed from the input data due to neither being a variable target or feature.

# Compiling, Training, and Evaluating the Model

Number of Neurons:
* First Hidden Layer: 80 neurons
* Second Hidden Layer: 30 neurons
* Output Layer: 1 neuron

Number of Layers:
* The model has three layers: one input layer, two hidden layers, and one output layer.

Activation Functions:
* The activation function used for the hidden layers is ReLU (Rectified Linear Unit), which is commonly used in deep learning models to introduce non-linearity and help the model learn complex patterns in the data.
* The activation function used for the output layer is Sigmoid, which is suitable for binary classification tasks as it squashes the output between 0 and 1, representing the probability of the input belonging to the positive class.

The model was unable to achieve a target predictive accuracy higher than 75%. The highest score achieved occurred on optimization attempt 1 of 3, where it increased from 72.38% (original model) to 73.88% (optimization attempt 1 model).

The following steps where taken to increase model performance:

Attempt 1:
* Dropped fewer columns - This time NAME will not be dropped.
* Created bins for rare occurrences in NAME column.
Attempt 2:
* Dropped fewer columns - This time NAME will not be dropped. - From Attempt 1
* Created bins for rare occurrences in NAME column. - From Attempt 1
*Created bins for rare occurrences in ASK_AMT column.
Attempt 3:
* Dropped fewer columns - This time NAME will not be dropped. - From Attempt 1
* Created bins for rare occurrences in NAME column. - From Attempt 1
* REMOVED seemingly unnecessary bins for rare occurrences in ASK_AMT column from Attempt 2.
* Reduced the number of epochs (100 to 52) to the training regimen.

## Summary

* The model achieved an accuracy of 73.88%, indicating that it correctly predicted the class of the data points nearly 74% of the time.
* The loss value of 0.5224 suggests that the model's performance in terms of minimizing errors during training was moderate.
* Since the accuracy is around 73.88%, there is room for improvement. Hyperparameter tuning may improve the model's performance. Techniques like adjusting learning rates, trying different optimizers, or modifying the network architecture could help enhance the model's accuracy.

## UPDATE
I forgot to download the HDF5 file for Optimization Attempt 1. After running the module again my results **increased** from 73.88% to 74.03%.

# Results for Attempt 1 Initially
![Original ATTEMPT 1](https://github.com/mcscodes/deep-learning-challenge/blob/main/Original_Optimization_1_Results.png)

# Results for Attempt 1 After Being Reran to Download HDF5 file.
![Rerun ATTEMPT 2](https://github.com/mcscodes/deep-learning-challenge/blob/main/Rerun_Optimization_1_Results.png))

# Notes
Xpert Learning Assistant was used in completing this analysis.
