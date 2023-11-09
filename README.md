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
The analysis aims to build and optimize a deep learning model for a non-profit organisation Alphabet Soup. The primary objective is to develop a predictive model with an accuarcy score surpassing 75% to determine the success of funding by Alphabet Soup based on various input parameters from the charity dataset. 

## Dataset
34,000 organizations. The columns that capture metadata about each organization, are:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

![image](https://github.com/JasmineBamba/deep-learning-challenge/assets/135666038/e1dd1e0d-494a-4981-b6ee-0ee64c06f446)

## Results

### Data Preprocessing
- **What variable(s) are the target(s) for your model?**
The target variable for the all three models is IS_SUCCESSFUL, representing the success of funding by Alphabet Soup as a binary classifier where 1 represents if the organization is successful and 0 if not.

![image](https://github.com/JasmineBamba/deep-learning-challenge/assets/135666038/47c75bdd-7539-4ccb-9eb5-831a32dabd76)


- **What variable(s) are the features for your model?**
Features used in the model include APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS

- **What variable(s) should be removed from the input data because they are neither targets nor features?**
EIN and NAME columns were removed from the input data in the first model, however NAME was added back in the training of second model.

### Compiling, Training, and Evaluating the Model
- **How many neurons, layers, and activation functions did you select for your neural network model, and why?**

**First Model:**
The neural network model is structured with an input layer that adapts to the number of features in the data, followed by two hidden layers with 80 and 30 neurons, both utilizing the ReLU activation function to introduce non-linearity. The output layer consists of one neuron with a sigmoid activation function, suitable for binary classification tasks where it outputs the probability of belonging to one of the classes. These choices serve as a starting point, and the specific number of neurons and layers will adjusted through experimentation.

![image](https://github.com/JasmineBamba/deep-learning-challenge/assets/135666038/87f8505a-6f25-47cf-9202-d728042482e5)

![image](https://github.com/JasmineBamba/deep-learning-challenge/assets/135666038/d838cbbd-3b73-498e-815b-d9669a0df4e0)



**Second Model:**
The neural network model comprises three hidden layers with 150, 100, and 50 neurons respectively, each utilizing Rectified Linear Unit (ReLU) activation functions. The ReLU activation is chosen for its ability to mitigate vanishing gradient issues and computational efficiency. The output layer employs a sigmoid activation function, ideal for binary classification tasks, with a single neuron. Additionally, dropout layers (with rates of 0.3 and 0.2) are inserted after the second and third hidden layers, respectively, to prevent overfitting. The RMSprop optimizer with a modified learning rate of 0.01 is used for more adaptive learning per parameter, potentially facilitating faster convergence in the training process. These architectural decisions are commonly made based on empirical knowledge, experimentation, and problem complexity to strike a balance between model capacity and preventing overfitting.

![image](https://github.com/JasmineBamba/deep-learning-challenge/assets/135666038/58a95d11-c635-4332-8d83-cb54e932b560)

![image](https://github.com/JasmineBamba/deep-learning-challenge/assets/135666038/42bd312b-f30b-4969-8efa-bf25ed92260c)


**Third Model-**
The neural network model comprises an input layer with neurons determined by the number of features, followed by three hidden layers containing 100, 40, and 20 neurons, each utilizing Rectified Linear Unit (ReLU) activation. The output layer consists of a single neuron using a Sigmoid activation for binary classification. The choice of neurons in decreasing order through the hidden layers allows the network to learn varying levels of abstraction. ReLU is employed to mitigate the vanishing gradient issue, while the Sigmoid function on the output layer provides a probability-like output for binary decisions. These choices aim to balance model complexity and learning capability, with adjustments made through experimentation and tuning.

![image](https://github.com/JasmineBamba/deep-learning-challenge/assets/135666038/5c1e03f3-8fae-4067-bbab-110a21ee82de)

![image](https://github.com/JasmineBamba/deep-learning-challenge/assets/135666038/f53d6975-b332-42f0-aa45-fac3a5dc20af)




- **Achievement of Target Model Performance:** Even though the initial model initially attained an accuracy of approximately 73%, attempts were made to improve its performance and achieved 78%.

The model was altered to incorporate the RMSprop optimizer in an effort to enhance its accuracy, yet it only reached 53%. As a result of this decrease in performance, a decision was made to revert to the original Adam optimizer while expanding the neural network with additional layers and increased neuron count. This revised model also integrated the 'NAME' column, resulting in a final accuracy of 78%.

- **Steps for Improving Model Performance:**
To improve model performance based on the previous iterations:

 1. **Optimizer Selection:** Begin with the Adam optimizer, which initially achieved around 73% accuracy. Other optimizers are tested, such as RMSprop, and the performance degrades to 53%, consider reverting to the original optimizer.

 2. **Layer and Neuron Adjustment:** Explore enhancing the neural network architecture. Initially, when the RMSprop model decreased accuracy to 53%, the decision was made to increase the number of layers and neurons. This iterative approach helps in capturing more complex relationships within the data.

 3. **Feature Inclusion:** Integrate additional column from the dataset into the model. In the case mentioned, incorporating the 'NAME' column contributed to achieving the final accuracy of 78%. The inclusion of relevant features can significantly impact model performance.


## Summary
The deep learning models were aimed at predicting funding success for Alphabet Soup, achieving a target accuracy of over 75%. The final model achieved the desired 78% accuracy by iteratively refining the architecture, adjusting optimizers, and integrating the 'NAME' column, demonstrating the significance of feature inclusion.

For a different approach, utilizing ensemble methods like Random Forest or Gradient Boosting could provide a solution to this classification problem. These models are powerful, non-neural network techniques capable of handling complex relationships within the data. Ensemble methods, by combining multiple models, often lead to robust predictions, reducing overfitting and accommodating non-linear relationships. Such models could be a suitable alternative, especially when the deep learning model does not meet the desired accuracy or when the dataset is not excessively large.
