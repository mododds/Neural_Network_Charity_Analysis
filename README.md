# Neural_Network_Charity_Analysis
Module 19 

## Overview of the analysis: 
The purpose of this analysis is to build a neural network machine learning module to take information about various organizations and their use of charitable donations in order to create a model that will help determine how to distribute funds to organizations in the future.

## Results: Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
- The target variable for this model is the "is successful" field (which indicates if the organization used their donation effectively
- Please see the [attached](https://github.com/mododds/Neural_Network_Charity_Analysis/blob/main/features.png) list of features used for this model
- Name and EIN were removed from the input data as they are neither targets nor features.

### Compiling, Training, and Evaluating the Model
- The original model had 80 neurons in the first layer, and 30 neurons in the second layer.

-- This is in line with the general rule of thumb to have 2 - 3 times the number neurons to your inputs (after scaling the data, we had 43 input parameters).

- I was not able to achieve the target performance of 75% accuracy. [Here is an accuracy graph for the first run](https://github.com/mododds/Neural_Network_Charity_Analysis/blob/main/Accuracy_Original.png)

-- Attempt 1: Increase the number of neurons

Result: After about 60 epochs, the [accuracy](https://github.com/mododds/Neural_Network_Charity_Analysis/blob/main/Accuracy_Opt_Attpt_1.png) of iteration became much spiker than the original run

-- Attempt 2: Increase the number of hidden layers

Result: After about 20 epochs, the [accuracy](https://github.com/mododds/Neural_Network_Charity_Analysis/blob/main/Accuracy_Opt_Attpt_2.png) scores seemed to peek and again, were incredibly spikey

-- Attempt 3: Adjust optimizer and activation types & number of epochs

Result: Hidden layer activation type softplus provided marginally better results (while other types performed very poorly).  Adamax provided the best option for optimization, however, it didn't perform much better than adam. Click [here](https://github.com/mododds/Neural_Network_Charity_Analysis/blob/main/Accuracy_Opt_Attpt_3.png) for an accuracy graph.  

** Please note: the changes/results of the optimization attempts were so minimal, even re-running the same module that previously yielded 73.7% accuracy, only yielded < 73.5% the second run. 

## Summary: 
- 74% accuracy isn't too bad; however, I believe this could have been accomplished with a supervised machine learning model as well. 
- The data had many companies, however, it only had 9 usable features within the dataset.  To run a sufficient ANN, I believe more input data would be required. I think incorporating additional data points, such as a company's charitable contributions, ESG ratings, community involvement, etc. may help this ANN perform better.
