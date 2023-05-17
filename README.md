# Deep learning challenge
## Overview
This challenge utilises knowledge in machine learning and neural networks to to create a binary classifier to predict whether applicants looking for funding are likely to be successful.
The dataset has been provided by the non-profit foundation - Alphabet Soup in a csv file which contains records of over 34000 organisations that have been funded by them in the past.
Thses are the 3 steps that were applied to the data
- Preprocess the data
- Compile, Train and Evaluate the model
- Optimize the model
- Write a report on the Neural Network model

## Results
**Preprocessing Data**
- Target variable for the model is ``'IS_SUCCESSFUL'``
- Feature variables for the model are `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANISATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT`
- Variables removed from the data: 
  - In the first model using the starter code, the variables `EIN` and `NAME` were removed under the assumption that they were only identifiers and would not be of importance to the prediction
  - However, in Optimization model 2, only the variable `EIN` was removed and the model provided a higher accuracy and lower loss.

**Compiling, Training and Evaluating the Model**
- Neurons, Layers and Activation functions selected: The starter model has 2 hidden layers and an output layers of 80, 30 and 1 neuron respectively. The 2 hidden layers used `relu` and the output layer used `sigmoid` activation. 

![Screenshot 2023-05-16 at 9 28 14 PM](https://github.com/Geetraje/deep-learning-challenge/assets/119769357/a4126e45-b29c-40e2-9f99-12e1047b878a)

