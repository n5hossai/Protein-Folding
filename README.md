# Protein-Folding
The objective of my analysis is to create a model that determines the accuracy of a computer-generated protein structure, compared with a known benchmark structure.

## How to run the models?
- Clone the files into your directory
- Have the `.rda` files loaded in your R studio environment
- run the `predict` function on your desired model to find the accuracy if the computer-generated protein structure

## Results and Discussion:
- While obtaining my final model, I started looking for outliers, however, I reached the conclusion that trying to remove some of the outliers after conducting a studentized residual test, the RMSE value only increases. RMSPE for model 4 before removing them was $0.5448438$, while after removing them it increased to $0.5838417$

- There were 6 models tested by my selection procedure. 3 from AIC (Forward, Backward, and Both) and 3 from BIC (Forward, Backward and Both)

- The figures on page 4 and 5 describe the differences in RMSE and MSE between validation and trainin sets.

- There are 89 variables in my model, some are positively, while some are negatively related to the respone variable (accuracy)

- All of them are uncorrelated variables, contributing to the prediction of the response variable.

- aliph1HC_scArgN_long = 0.563553314. With one unit increase in this variable *aliph1HC_scArgN_long*, the response variable increases by 0.563553314
- scArgN_bbO_medlong = 0.437025430. With one unit increase in this variable *scArgN_bbO_medlong*, the response variable increases by 0.437025430
- bbCA_bbO_vshor = -0.395812423 . With one unit increase in this variable *bbCA_bbO_vshor*, the response variable decreases by 0.395812423


![plot of MSE vs Predictors](https://github.com/n5hossai/Protein-Folding/blob/main/mse%20vs%20preds.PNG)

![plot of RMSE values](https://github.com/n5hossai/Protein-Folding/blob/main/RMSE%20vals.PNG)
