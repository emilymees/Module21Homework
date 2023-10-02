# Module21Homework
# Deep-Learning-Challenge

## Analysis Overview

The purpose of this exercise was to analyze more than 34,000 organizations that have received funding from a non-profit foundation, Alphabet Soup, and build a model that can help in the decision process for future funding applicants.

## Data Preprocessing

After reviewing the dataset it was determined that the `EIN` and `NAME` columns could be removed; otherwise, if these columns remained we would possibly see poor performance when we later trained the model. 

Then bins were created for `APPLICATION_TYPE` and `CLASSIFICATION` to potentially help improve accuracy and possibly reduce any noise in the dataset.
![Alt text](<Screenshot 2023-10-02 180253.png>)
![Alt text](<Screenshot 2023-10-02 180303.png>)

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

![Alt text](<Screenshot 2023-10-02 181618.png>)

## Compiling, Training, and Evaluating the Model



## Summary

