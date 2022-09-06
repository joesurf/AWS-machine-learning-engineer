# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Remove all values below zero.

### What was the top ranked model that performed?
Weighted ensemble model. This model takes a weightage of multiple models to produce the best result. 

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Converting datatime into separate variables and hot-encoding categorical variables like weather and season.

### How much better did your model perform after adding additional features and why do you think that is?
The model can better find patterns across data with more specific variables that accurately represent the characteristics.

## Hyper parameter tuning
### How much better did your model perform after trying different hyper parameters?
Not much better. AutoGluon finds the best hyper parameters on its own, so changing them will not make much of a difference.

### If you were given more time with this dataset, where do you think you would spend more time?
Feature engineering.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|?|?|?|1.80552|
|add_features|?|?|?|1.33069|
|hpo|?|?|?|1.33439|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score.png](img/model_test_score.png)

## Summary
While AutoGluon can build state of the art machine learning models directly, it is more useful as a go-to baselining method.
Though AutoGluon does the data preprocessing and feature engineering, I find that I can get better performance if I preprocess and feature engineer the data before training with AutoGluon.