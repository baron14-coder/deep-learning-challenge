# deep-learning-challenge
       ANALYSIS
the purpose of this analysis is to build a binary classification model using deep learning to predict whether an applicant would be successful in securing funding from Alphabet Soup. 

STEPS TAKEN:

the data was Preprocessed  by handling categorical features, dropping unnecessary columns and scaling numerical values.

Designed a deep neural network model using TensorFlow/Keras.

I used keras tuner to choose different optimizations to improve accuracy beyond 75%.

Evaluated the model's performance and considered alternative approaches.
Results
Data Processing

Target Variables (y):

IS_SUCCESSFUL - Indicates if the applicant successfully used the funding.
Feature Variables (X):

All remaining columns except identification variables.

Categorical variables were one-hot encoded (APPLICATION_TYPE, CLASSIFICATION, AFFILIATION).

Numerical variables were scaled using StandardScaler().

Variables Removed:

EIN and NAME were removed since they contained no predictive value.

Some categorical values with low frequency were grouped into an 'Other' category for better organization.

Compiling, Training, and Evaluating the Model:

Inital Model:

2 hidden layers (80 neurons and 30 neurons)

Activation Function: ReLu

Output Layer: Sigmoid for binary classification
it had final accuracy of 72%

Optimization Attempts:

first Optimized Model:

2 hidden layers (74 neurons, 85 neurons, 93 neurons)
Activation Function: ReLu
I increased the number of neurons and added an additional layer to increase optimization
Model Performance:
Final Optimized Accuracy: 72.5%

Second optimization model:
 Changed activation from ReLu to tanh and added an additional layer also increasing the neurons in each layer. 
Model Performance:
Final Optimized Accuracy: 72.2%

Third optimization model:
 Kept ReLu activation, added an additional layer then increased the neurons even more but had no effect on the accuracy

Model Performance:
Final Optimized Accuracy: 72.5%

Challenges:

Model performance failed to reach 75% accuracy even with different optimizations.

A different approach may be needed to reach 75% or higher accuracy.

Recommendations:

Random Forest or XGBoost

Tree-based models handle categorical data without needing one-hot encoding.

