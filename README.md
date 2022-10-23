# Neural_Network_Charity_Analysis
# Module 19. Alphabet-Soup_Charity Neural Network Classification Problem

![image](https://user-images.githubusercontent.com/107591542/197405611-4e279016-5557-44ce-9098-29056aad2664.png)


## Overview 

The purpose of this challenge is to apply some skills and subjects related with machinelearning. From Alphabet Soup’s business team, an analyst received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.
The goal of this project is find a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. Within this dataset are the columns showed below that have metadata about each organization.

 
I followed some steps to reach the goal like these:
•	Preprocessing Data for a Neural Network Model . Data Cleaning and Data Preprocessing
•	Compile, Train, Evaluate the Model
•	Optimize the Model: Redefine the Model, Compile, Train, Evaluate
o	Adjusting the input data  by Dropping more or fewer columns; Creating more bins for rare occurrences in columns.
o	Increasing or decreasing the number of values for each bin.
o	Adding more neurons to a hidden layer.
o	Adding more hidden layers.
o	Using different activation functions for the hidden layers.
o	Adding or reducing the number of epochs to the training regimen.

## Results. Deliverables/Analysis

###  Target variables for the model

The target variable is “IS_SUCCESSFUL” that shows if  the money was used effectively


###  Features variables for the model

By cleaning the data, we dropped columns “EIN, “NAME” and got a new dataframe. Feature variables are all  in the dataset but “IS_SUCCESSFUL” 

 
![image](https://user-images.githubusercontent.com/107591542/197405658-2e6d4f90-09cd-45f8-8da4-9ca511717c94.png)


### What variable(s) are neither targets nor features, and should be removed from the input data?

Columns “EIN, “NAME” were removed because they are just identification and they are no useful for the analysis. Additionally two variables were binned (“APPLICATION_TYPE”, “CLASSIFICATION”) because of their low occurrence value counts 


### Neurons, layers, and activation functions 

The imput features are 43. Following the good rule of thumb (to have two or three times the amount of neurons in the hidden layer). I select two layers (hidden_nodes_layer1 = 80
hidden_nodes_layer2 = 50) as showed below . These layers used ReLU as activitation function and the “sigmoid” was used on the output layer

![image](https://user-images.githubusercontent.com/107591542/197405675-5ebf6174-82b0-4758-a170-50c963aef57d.png)

 
### Target model performance

I got accuracy around 0.73 which is acceptable  as target model performance on this step. Optimization is required to improve accuracy
 
![image](https://user-images.githubusercontent.com/107591542/197405694-884355c8-895c-456a-8f7f-5a59c6bca6c7.png)

### Steps to increase model performance

To increase the model performance I did some actions like:
•	Adjusting the input data  by dropping more or fewer columns and by creating more bins for rare occurrences in columns.
•	Increasing or decreasing the number of values for each bin.
•	Adding more neurons to a hidden layer.
•	Adding more hidden layers.
•	Using different activation functions for the hidden layers.
•	Adding or reducing the number of epochs to the training regimen.

Charts below show some results

•	Our three layers model shows an insignificant improvement accuracy from 0.725 to 0.726

 ![image](https://user-images.githubusercontent.com/107591542/197405708-b4603c13-f17f-4a70-bf4c-8347b32bd5cb.png)

![image](https://user-images.githubusercontent.com/107591542/197405718-2635f865-24d7-4299-ac14-7afbe043a714.png)

![image](https://user-images.githubusercontent.com/107591542/197405734-3549aaae-9789-4b53-ab80-d4d881e04542.png)
 

•	Our four layers model shows 

 ![image](https://user-images.githubusercontent.com/107591542/197405741-fe2fdbd4-8d1c-4666-98cf-ce277adbea37.png)

![image](https://user-images.githubusercontent.com/107591542/197405756-01d3da95-8298-4525-b3e9-089531a7416c.png)


•	Using RandomForestClassifer I got 0.776 which is better. 

 ![image](https://user-images.githubusercontent.com/107591542/197405760-0ac39e58-3958-48ae-8e71-d3d795322cd4.png)


## Summary

I realized that sometimes, doing some changes to the model it does not generate great improvements. Accuracy is almost the same when we used three ot four layers as well  as when we used different activitation functions

It means that it is a trial and error process in order to find the right solution. I realize that creating a  RandomForest Classifier for Comparison showed a best accuracy ( 0.776).

I could mean that is the better model to use in order to solve the problem which is to find a binary classifier capable of predicting whether applicants will be successful. Althougt 0.776 is a good value it might be not enough for making excellent decisions.

I think that, in order to reach better results we have to perform new processes with different layers and different activitation functions. Even we should consider to include new data

We should follow a trial and error method several times, lear from the results and eventually  choose the best one

