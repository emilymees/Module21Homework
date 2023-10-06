# Module21Homework
# Deep-Learning-Challenge

## Analysis Overview

The purpose of this exercise was to analyze more than 34,000 organizations that have received funding from a non-profit foundation, Alphabet Soup, and build a model that can help in the decision process for future funding applicants.

## Data Preprocessing

After reviewing the dataset it was determined that the `EIN` and `NAME` columns could be removed; otherwise, if these columns remained we would possibly see poor performance when we later trained the model. 

Then bins were created for `APPLICATION_TYPE` and `CLASSIFICATION` to potentially help improve accuracy and possibly reduce any noise in the dataset.
![Alt text](<https://github.com/emilymees/Module21Homework/blob/main/Images/Screenshot%202023-10-02%20180253.png>)
![Alt text](<https://github.com/emilymees/Module21Homework/blob/main/Images/Screenshot%202023-10-02%20180303.png>)

After converting the categorical data to numeric with `pd.get_dummies`, the data was split into features and target arrays. 

Target variable for this model:
* *IS_SUCCESSFUL*

Feature variables for this model:
* *APPLICATION_TYPE*
* *AFFILIATION*
* *CLASSIFICATION*
* *USE_CASE*
* *ORGANIZATION*
* *STATUS*
* *INCOME_AMT*
* *SPECIAL_CONSIDERATIONS*
* *ASK_AMT*

![Alt text](<https://github.com/emilymees/Module21Homework/blob/main/Images/Screenshot%202023-10-02%20181618.png>)

## Compiling, Training, and Evaluating the Model

The first training model was built with 2 hidden layers which included 80 and 30 neurons, and `relu` activation function.

![Alt text](<https://github.com/emilymees/Module21Homework/blob/main/Images/Screenshot%202023-10-02%20182837.png>)

This resulted in 0.555 loss and approximately 72.52% accuracy with the test data. 

Since our target accuracy was 75% I then went through 4 optimization trials where I either increased the number of hidden layers, increased the number of neurons for each hidden layer, adjusted the activation function, and then tried dropping the `INCOME_AMT` column from the dataset. 

Unfortunately each of these optimization attempts did not produce the target accuracy and stayed close to 72% accuracy.

## Summary

While there was a slight increase in performance switching back to `relu` activation function and dropping the `INCOME_AMT` column, I was still only able to achieve 72.8% accuracy. Further investigation into additional binning or layers/neurons would need to take place to potentially achieve target accuracy. 