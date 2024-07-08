# DEEP LEARNING NEURAL NETWORK MODEL

## Overview
The purpose of this analysis is to create a neural network model to predict whether a grantee of the nonprofit foundation Alphabet Soup will be successful. I utilized a dataset with information on over 34,000 historical grantees. The model I created can help the foundation determine which investments have the greatest probability of favorable returns in the future with 73% accuracy.

## Results
### Data Preprocessing
•	What variable(s) are the target(s) for your model? The variable “IS_SUCCESSFUL” is the target for this model. It is a binary variable that shows whether the investment from Alphabet Soup resulted in a successful venture.
•	What variable(s) are the features for your model? APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMOUNT, SPECIAL_CONSIDERATIONS, and ASK_AMT.
•	What variable(s) should be removed from the input data because they are neither targets nor features? EIN and NAME were both removed because they are identifying variables that do not inform the model.

### Compiling, Training, and Evaluating the Model
•	How many neurons, layers, and activation functions did you select for your neural network model, and why? 
•	The initial model design was selected based on common practices for binary classification neural networks. I added the first Dense layer and the nine input layers to match the number of features/dimensions in the model (‘input_dim’). For the first hidden layer, I used 128 neurons to help the model learn different patterns. The second hidden layer is half of this number, 64 neurons, to gradually reduce the complexity. The third hidden layer was half of the second, 32 neurons. Again, this lower number helps reduce complexity so the model can begin to generalize. The output layer is only one neuron which is appropriate for sigmoid activation and binary classification; it produces a probability score between 0 and 1. I used ReLU activation because it introduces non-linearity and is a popular choice for enhancing model speed and performance.
•	Were you able to achieve the target model performance? No, the highest accuracy level I achieved was 0.726
•	What steps did you take in your attempts to increase model performance?
•	I added dropout layers to prevent overfitting, I experimented with more and fewer epochs to allow the model to learn effectively without overfitting, and I tried different optimizers, however using ‘rmsprop’ instead of ‘adam’ did not increase the overall accuracy of the model.

### Summary
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
•	The binary classification model I created was 72.6% accurate at predicting whether a grantee would have successful project. Without additional context on the organization’s investment goals, it was difficult to know which features to remove, if any. Given the opportunity, I would like to collect additional data on program efficacy aligned with the foundation’s mission. For example, how is the “Is Successful” variable defined? I’d like to explore the numbers of people served by each investment and other program outputs such as hours or days of service (if the grantees are service providers). Adding these additional continuous variables might enhance the model. In the absence of these additional variables, I might continue to experiment with different quantities of neurons and different optimizers.
