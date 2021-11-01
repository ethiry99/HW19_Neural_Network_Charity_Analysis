# HW 19 Neural Network Charity Analysis

## Overview of the Project
* #### Use nueral networks to predict success of charity proposals
* #### Create bianary classifier to make the prediction using .csv dataset provided by Alphabet Soup.

## Results
### Data Preprocessing Questions
1)  What variable(s) are considered the target(s) for your model?
    * The target IS_Succesful, is used in this model as we predeict if an applicant will be successful if they are granted the assistance. 
2)  What variable(s) are considered to be the features for your model?
    * The features in this model are; APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS & ASK_AMOUNT.   
3)  What variable(s) are neither targets nor features, and should be removed from the input data?
    * The columns that were not used in the model are EIN & NAME.
### Compiling, Training, and Evaluating the Model
4)  How many neurons, layers, and activation functions did you select for your neural network model, and why?
    * There are 80 neurons in the first hidden layer and 30 in the second.  The layers using RELU while the output layer is using SIGMOID. It attained an accuracy of 72.5%.<br></br> ![](https://github.com/ethiry99/HW19_Neural_Network_Charity_Analysis/blob/main/Resources/Images/orig.png?raw=true)
5)  Were you able to achieve the target model performance?
    * Neither the original analysis or the optimization attempts acheived a 75% 
6) What steps did you take to try and increase model performance?
    * In the 1st optimization attempt tanh is used for the activation in the hidden layers. It returned an accuracy of 72.6%, very similar to the original analysis.<br></br>![](https://github.com/ethiry99/HW19_Neural_Network_Charity_Analysis/blob/main/Resources/Images/opt1_tanh.png?raw=true)
    * In the 2nd optimization attempt a third hidden layer is added and the activations for those layer is RELU and the output layer activation is TANH. It returned an accuracy of 72.5%, matching the original analysis.<br></br>![](https://github.com/ethiry99/HW19_Neural_Network_Charity_Analysis/blob/main/Resources/Images/opt2_xtra_layer.png?raw=true)
    * In the 3rd optimization attempt I created bins for the ask amount to try and reduce some of noise from the wide range of ask amont entries and added neurons to the hidden layers.  The epochs being ran are also increased from 100 in the previous attempts to 200 in this final attempt.  This final attempt 72.6%.<br></br>![](https://github.com/ethiry99/HW19_Neural_Network_Charity_Analysis/blob/main/Resources/Images/opt2_binning.png?raw=true)

## Summary
   * None of the optimation attempts had a significant affect on the results.
   * Perhaps increasing the number of bins on the ASK_AMT feature could help increase the accuracy by more closely representing the dataset.
   * Another possibilty could be reducing the features to identify the ones that are the best predictors.
   * There are also optimizers and activators that we have not studied yet.  Conceivably one of them would work better with the provided data.










