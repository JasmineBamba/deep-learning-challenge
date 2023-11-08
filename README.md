# deep-learning-challenge
Neural Network Model

## What it a is Neural Network?

Neural networks are a powerful machine learning technique modeled after neurons in the brain.
Neural Network is an advanced form of machine learning that contains multiple layers of nodes, which perform individual computations.These computations are connected and weighed against one another until the neurons reach the final layer. In the final layer, the neurons return either a numerical result or an encoded categorical result.

Neural networks can:
- Recognizes patterns and feautures of input data
- Provides a clear quanitative output

![image](https://github.com/JasmineBamba/deep-learning-challenge/assets/135666038/32d481ac-5deb-4874-92ca-b15a26106235)


# Neural Network Model Performance Report

## Overview of the Analysis
The analysis aims to build and optimize a deep learning model for Alphabet Soup. The primary objective is to develop a predictive model to determine the success of funding by Alphabet Soup based on various input parameters from the charity dataset.

## Results

### Data Preprocessing
- **Target Variable:** The target variable for the model is IS_SUCCESSFUL, representing the success of funding by Alphabet Soup.
- **Features:** Features used in the model include APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, etc.
- **Variables Removed:** EIN and NAME columns were removed from the input data as they were neither target variables nor features.

### Compiling, Training, and Evaluating the Model
- **Neurons, Layers, Activation Functions:** The model was designed with a neural network structure comprising 2 hidden layers with 80 and 30 neurons, respectively, using ReLU activation functions. The output layer used a sigmoid activation function due to the binary classification nature of the problem.
- **Achievement of Target Model Performance:** Although the initial model achieved around 73% accuracy, efforts were made to enhance performance.
- **Steps for Improving Model Performance:** Various optimization techniques were attempted, including adjusting data preprocessing, altering the model architecture by adding more layers, neurons, and activation functions, optimizing hyperparameters like epochs and batch sizes. However, the target accuracy of over 75% was not fully attained.

## Summary
The deep learning model's performance indicates a reasonable level of accuracy but falls short of the defined target. To potentially solve this classification problem, considering a different model such as a Random Forest Classifier or a Gradient Boosting Classifier might be beneficial. These models can handle complex interactions between variables differently and might improve predictive accuracy.
