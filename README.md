## Deep-learning-challenge
Module 21 challenge

## Overview

This challenge utilises knowledge in machine learning and neural networks to create a binary classifier to predict whether applicants looking for funding are likely to be successful. The dataset has been provided by the non-profit foundation - Alphabet Soup in a csv file which contains records of over 34000 organisations that have been funded by them in the past. These are the 3 steps that were applied to the data

1. Preprocess the data
2. Compile, Train and Evaluate the model
3. Optimize the model

## Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received access to a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

1. EIN and NAME—Identification columns
2.APPLICATION_TYPE—Alphabet Soup application type
3. AFFILIATION—Affiliated sector of industry
4. CLASSIFICATION—Government organization classification
5. USE_CASE—Use case for funding
6. ORGANIZATION—Organization type
7. STATUS—Active status
8. INCOME_AMT—Income classification
9. SPECIAL_CONSIDERATIONS—Special considerations for application
10. ASK_AMT—Funding amount requested
11. IS_SUCCESSFUL—Was the money used effectively

## Results

# Preprocessing data

1. Target variable for the model is 'IS_SUCCESSFUL'
2. Feature variables for the model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANISATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT
3. Variables removed from the data:
    1. In the first model using the starter code, the variables EIN and NAME were removed under the assumption that they were only identifiers and would not be of importance to the prediction
    2. However, in Optimization model 2, only the variable EIN was removed and the model provided a higher accuracy and lower loss.
    3. In Optimization model 3, the variables dropped were, EIN, SPECIAL_CONSIDERATIONS and STATUS were dropped to provide a marginal increase in accuracy
  

# Compiling, Training and Evaluating the Model

# Model 1
Neurons, Layers and Activation functions selected: The starter model has 2 hidden layers and an output layers of 12, 6 and 1 neuron respectively.
The 2 hidden layers used relu and the output layer used sigmoid activation.

This model achieved only 72% accuracy.

![Screenshot 2025-04-02 213708](https://github.com/user-attachments/assets/115471d5-548c-47bf-9572-59c6f9378d10)


![Screenshot 2025-04-02 213721](https://github.com/user-attachments/assets/0f6cecac-0c4e-4516-a070-97c021135c77)

# Model 2 optimization

The variable NAME column was retained and 4 hidden layer was added with tanh activation. 
With this model the accuracy of 77% was achieved.

![Screenshot 2025-04-02 214027](https://github.com/user-attachments/assets/c71196c9-faad-47d9-a591-cbbcb5dbbf91)


![Screenshot 2025-04-02 214036](https://github.com/user-attachments/assets/e3c91038-aa35-4d15-aac1-d8dc9977c9a3)


# Model 3 optimization

Retained Name column,removing Special_Considerations and Status columns and adding two more hidden layers with different activation functions.
With this model the accuracy of 77% was achieved.


![Screenshot 2025-04-02 214331](https://github.com/user-attachments/assets/f5e8239e-e9fe-4e5e-9f03-55e4edcef6ce)


![Screenshot 2025-04-02 214318](https://github.com/user-attachments/assets/74db7d13-2449-4f5d-a864-a88ccf502268)

## Summary

This model using TensorFlow was able to provide a prediction with an accuracy of 77% by manipulating and choosing variables, layers, number of neurons and binning values over numerous attempts.

Using the Random Foerst Classifier or a Support Vector Machine to try to achieve higher accuracy and a lower loss would be benificial. Both of these models are effective in binary classification, can handle both numerical and categorical variables and address imbalanced datasets and outliers if they are present in this dataset.
