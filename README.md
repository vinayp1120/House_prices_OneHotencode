# House Prices Prediction with One-Hot Encoding

This repository demonstrates how to build a simple **Linear Regression** model to predict house prices based on categorical and numerical data. In this project, I've explored different techniques for handling categorical variables, particularly **dummy variables** and **one-hot encoding**, to convert categorical data into a numerical format suitable for machine learning models.

## Dataset

The dataset used for this project contains the following features:
- **Town** (categorical): The town where the house is located.
- **Area** (numerical): The size of the house in square feet.
- **Price** (numerical): The price of the house, which serves as the target variable for prediction.

## Model

The **Linear Regression** model was trained on the dataset to predict house prices based on the town and area. Linear Regression is a simple, interpretable model that works well for understanding the relationships between the inputs and the target variable.

## Techniques Used

Handling categorical data is crucial for training machine learning models. Since the town is a categorical feature, I explored two common techniques for converting it into a numerical format:

1. **Dummy Variables**: In this approach, the categorical variable is converted into multiple binary columns, where each column represents a possible category, and a value of 1 or 0 indicates the presence or absence of that category for a given row.

2. **One-Hot Encoding**: Similar to dummy variables, one-hot encoding transforms the categorical data into binary columns. However, special attention must be given to avoid the **dummy variable trap**, which occurs when one of the categories is perfectly predictable from the others. This can lead to multicollinearity issues in the model.

I ensured that the dummy variable trap was handled by either dropping one of the categories during encoding or using built-in functions that manage this issue.

## Model Development

I built two versions of the Linear Regression model, one using dummy variables and the other using one-hot encoding. In both cases:
- The categorical variable "town" was encoded into numerical columns.
- The **area** feature remained unchanged, as it is already a numerical value.
- The models were then trained on this transformed data to predict house prices.

## Performance

Given that the dataset was relatively small, training time was minimal, and the model performed well in terms of accuracy for such a dataset size. For larger datasets, training time may increase, but the methods employed here will still be valid for handling categorical data and building a robust model.

## Conclusion

This project highlights the importance of handling categorical data in machine learning. By using dummy variables and one-hot encoding, we can effectively incorporate categorical features into our models and avoid potential pitfalls like the dummy variable trap. This approach can be applied to larger datasets to train more complex models with greater predictive power.
