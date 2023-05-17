# Deep learning challenge
## Overview
This challenge utilises knowledge in machine learning and neural networks to create a binary classifier to predict whether applicants looking for funding are likely to be successful.
The dataset has been provided by the non-profit foundation - Alphabet Soup in a csv file which contains records of over 34000 organisations that have been funded by them in the past.
These are the 3 steps that were applied to the data
- Preprocess the data
- Compile, Train and Evaluate the model
- Optimize the model

## Results
**Preprocessing Data**
- Target variable for the model is ``'IS_SUCCESSFUL'``
- Feature variables for the model are `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANISATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT`
- Variables removed from the data: 
  - In the first model using the starter code, the variables `EIN` and `NAME` were removed under the assumption that they were only identifiers and would not be of importance to the prediction
  - However, in Optimization model 2, only the variable `EIN` was removed and the model provided a higher accuracy and lower loss.
  - In Optimization model 3, the variables dropped were, `EIN`, `SPECIAL_CONSIDERATIONS` and `STATUS` were dropped to provide a marginal increase in accuracy

**Compiling, Training and Evaluating the Model**
- Neurons, Layers and Activation functions selected: The starter model has 2 hidden layers and an output layers of 80, 30 and 1 neuron respectively. The 2 hidden layers used `relu` and the output layer used `sigmoid` activation. 

![Screenshot 2023-05-16 at 9 28 14 PM](https://github.com/Geetraje/deep-learning-challenge/assets/119769357/a4126e45-b29c-40e2-9f99-12e1047b878a)

This model did not achieve the minimum required performance of 75%

![Screenshot 2023-05-16 at 9 37 34 PM](https://github.com/Geetraje/deep-learning-challenge/assets/119769357/f8414543-dbda-406c-8463-097b7de55fac)

**4 optimisations were run on this dataset to come up with a model that provided higher accuracy and lower loss**

**Optimisation 1**
Increased the number of values of each bin - `APPLICATION` AND `CLASSIFICATION` and reduced the numb er of neurons to 12, 6 and 1

![Screenshot 2023-05-16 at 9 46 33 PM](https://github.com/Geetraje/deep-learning-challenge/assets/119769357/8db24549-f003-4572-98d2-91d770da3103)


This model did not achieve 75% accuracy


![Screenshot 2023-05-16 at 9 47 53 PM](https://github.com/Geetraje/deep-learning-challenge/assets/119769357/52966910-d85f-4083-afdb-b3d3777de049)

**Optimization 2**
The variable `NAME` column was retained and an additional hidden layer was added with `relu` activation

![Screenshot 2023-05-16 at 9 53 02 PM](https://github.com/Geetraje/deep-learning-challenge/assets/119769357/183c34d0-95cc-4617-9c63-e57e221c15a8)

This model was a success with an accuracy of 77.93%

![Screenshot 2023-05-16 at 9 55 38 PM](https://github.com/Geetraje/deep-learning-challenge/assets/119769357/02aa22b2-a4a4-4134-a3d8-21e01df54cc1)

2 more models were tried to improve accuracy, by removing additional less important variables, adding more hidden layers, using `tanh` activation and also with a higher number of epochs and while both were above 75%, they were not much greater than Optimisation Model 2

**Optimization 3**

![Screenshot 2023-05-16 at 10 01 07 PM](https://github.com/Geetraje/deep-learning-challenge/assets/119769357/c5bfd4bc-a7cc-453c-9660-74ce8dc9b21f)

**Optimization 4**

![Screenshot 2023-05-16 at 10 00 28 PM](https://github.com/Geetraje/deep-learning-challenge/assets/119769357/74e09718-273d-4c7c-a8af-930d932e6a2d)


## Summary
This model using TensorFlow and Keras was able to provide a prediction with an accuracy of 78% by manipulating and choosing variables, layers, number of neurons and binning values over numerous attempts.

I would recommend using the Random Foerst Classifier or a Support Vector Machine to try to achieve higher accuracy and a lower loss. Both of these models are effective in binary classification, can handle both numerical and categorical variables and address imbalanced datasets and outliers if they are present in this dataset.

## References

IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/

