# Neural_Network_Charity_Analysis

## Purpose
For this project we are analyzing organizations that have received funding from our company, Alphabet Soup, over the years. We will use machine learning and neural networks to determine if we can predict whether applicants will be successful if Alphabet Soup funds them.

## Data
We were provided with a csv file entitled, charity_data.csv. This file contains data on over 34,000 organizations that have received funding from Alaphabet Soup of the years. The data contains the following fields:
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

The data was preprocessed using Pandas prior to the machine learning and neural networks analysis.

## Results
The analysis was conducted four times to attempt to achieve and increase model performance.

### First Analysis
The first analysis had the following parameters.
#### Data Preprocessing
The variable considered to be the target in our model is: IS_SUCCESSFUL
The variable considered to be the features in our model is: IS_SUCCESSFUL
The variables that were dropped are: EIN and NAME

#### Compiling, Training and Evaluating the Model
We created two hidden layers with the following information: 
 - Hidden Layer 1 has 80 neurons
 - Hidden Layer 2 has 50 neurons
The activation method was: relu

The parameters of the initial model are shown below
![Model1_parameters](https://github.com/kkoehn8/Neural_Network_Charity_Analysis/blob/main/Images/ModelParameters.PNG)

The model did not meet the target model performance, the model performance was: 72.78%

### Second Analysis
The second analysis was conducted to attempt to improve model performance. For this model we dropped additional columns and added a hidden layer. The second analysis had the following parameters.
#### Data Preprocessing
The variable considered to be the target in our model is: IS_SUCCESSFUL
The variable considered to be the features in our model is: IS_SUCCESSFUL
The variables that were dropped are: EIN, NAME, STATUS, and SPECICAL_CONSIDERATIONS

#### Compiling, Training and Evaluating the Model
We created three hidden layers with the following information: 
 - Hidden Layer 1 has 80 neurons
 - Hidden Layer 2 has 50 neurons
 - Hidden Layer 3 has 20 neurons
The activation method was: relu

The parameters of the initial model are shown below
![Model2_parameters](https://github.com/kkoehn8/Neural_Network_Charity_Analysis/blob/main/Images/ModelParameters_D3_1.PNG)

The model did not meet the target model performance, the model performance was: 72.27%

### Third Analysis
The third analysis was conducted to attempt to improve model performance. For this model we dropped fewer columns and added a hidden layer and bucketed an additional column. Additionally we also changed the activiation method. The third analysis had the following parameters.
#### Data Preprocessing
The variable considered to be the target in our model is: IS_SUCCESSFUL
The variable considered to be the features in our model is: IS_SUCCESSFUL
The variables that were dropped are: EIN

#### Compiling, Training and Evaluating the Model
We created four hidden layers with the following information: 
 - Hidden Layer 1 has 141 neurons
 - Hidden Layer 2 has 94 neurons
 - Hidden Layer 3 has 47 neurons
 - Hidden Layer 4 has 5 neurons
The activation method was: sigmoid

The parameters of the initial model are shown below
![Model3_parameters](https://github.com/kkoehn8/Neural_Network_Charity_Analysis/blob/main/Images/ModelParameters_D3_2.PNG)

The model did not meet the target model performance, the model performance was: 74.29%

### Fourth Analysis
The fourth analysis was conducted to attempt to improve model performance. For this model we dropped additional columns and added a hidden layer and binned an additional column. Additionally we also changed the activiation method. The fourth analysis had the following parameters.
#### Data Preprocessing
The variable considered to be the target in our model is: IS_SUCCESSFUL
The variable considered to be the features in our model is: IS_SUCCESSFUL
The variables that were dropped are: EIN, STATUS, and SPECIAL_CONSIDERATIONS

#### Compiling, Training and Evaluating the Model
We created four hidden layers with the following information: 
 - Hidden Layer 1 has 1185 neurons
 - Hidden Layer 2 has 790 neurons
 - Hidden Layer 3 has 395 neurons
 - Hidden Layer 4 has 5 neurons
The activation method was: sigmoid

The parameters of the initial model are shown below
![Model4_parameters](https://github.com/kkoehn8/Neural_Network_Charity_Analysis/blob/main/Images/ModelParameters_D3_3.PNG)

The model did meet the target model performance, the model performance was: 79.03%

## Summary
As we modified model parameters the model parameters improved. The binning of the NAME field and the addition of a hidden layer with additional neurons improved the performance of the model. Adding additional hidden layers may increase the performance but it might be negligable. The preprocessing of binning additional columns may help improve model performance. 

