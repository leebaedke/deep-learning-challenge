# deep-learning-challenge

## Overview:
The purpose of this analysis is to create a neural network that utilizes machine learning to help facilitate awarding funds to organizations by predicting whether they will be successful.

## Results:

Data Preprocessing
* The target variable for this model is 'IS_SUCCESSFUL'.
* The feature variables are 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'.
* In this model I have removed 'EIN' and 'NAME', as they do not serve a predictive purpose and could introduce an unwanted bias.

Compiling, Training, and Evaluating the Model

* Initial Model:
  * I used 80 hidden nodes for the 1st layer, and 30 hidden nodes for the 2nd layer, with 'relu' as the activation function for both. 'relu' is considered the most efficient activation function.
  * I was not able to reach 75% with my initial model.
  * I only achieved an accuracy of 73.08%
    Loss: 0.5591842532157898, Accuracy: 0.7308454513549805

* 1st Optimization Model:
  * I used 240 hidden nodes for the 1st layer, 160 hidden nodes for the 2nd layer, and 80 for the 3rd layer, with 'relu' as the activation function for all three.
  * I was not able to reach 75% with my 1st optimization attempt.
  * I improved the accuracy to 73.24%
    Loss: 0.5777676105499268, Accuracy: 0.7323614954948425

* 2nd Optimization Model:
  * I used 240 hidden nodes for the 1st layer, 160 hidden nodes for the 2nd layer, and 80 for the 3rd layer, with 'tanh' as the activation function for all three, I also reduced the epochs to 50.
  * I was not able to reach 75% with my 2nd optimization attempt.
  * The accuracy dropped slightly to 73.07%
    Loss: 0.5528030395507812, Accuracy: 0.7307288646697998
  
* 3rd Optimization model:
  * In addition to 'EIN' and 'NAME', I also removed 'STATUS' as a feature variable, thinking that it may be introduction a bias.
  * I used 300 hidden nodes for the 1st layer, and 100 hidden nodes for the 2nd layer, with 'relu' as the activation function for both, as in the Initial Model.
  * I was not able to reach 75% with this model either.
  * I only achieved an accuracy of 73.33%
    Loss: 0.5583974719047546, Accuracy: 0.7332944869995117
    
## Summary
I was not able to improve the accuracy of the model to reach 75%. Perhaps a different type of modeling could achieve a higher level of accuracy. I would recommend using a Random Forest model, it may be able to interpret the importance of certain features better when making its analysis.  

    
