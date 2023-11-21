# Financial-Loan-Default-Prediction
Binary classification using Logistic (Lasso) Regression, MLP, RNN

# Models
Logistic_Regression_L2_ALL: Logistic regression with all features; base line to compare to other models

Logistic_Regression_L1_ALL: Lasso to select essential features

Logistic_Regression_L2_Select: Logistic regression with selected features by Lasso

NN_Multilayer_Perceptron: MLP to reflect cross relationships between features

RNN: Recurrent Neural Network to reflect the sequential data

# Folder Structure
Current - Data  - LastOnlyProcessed  - small

                                     - medium
                                     
                                     - full
                                     
                - Seq: 'seq_uint8_{i}.h5', 'scale_params.pkl'
                
        - Model

# Dataset
The dataset is from Kaggle: [BankCreditDefault](https://www.kaggle.com/datasets/kornilovag94/bank-credit-default-loan-default)

The data is sequential(length 1 to 20) for each unique ID. 

I used last only data for Logistic, Lasso, and MLP, while I used full sequential data for RNN. 

### Preprocessing
Used standard scaler for interger features, and one hot encoder for binary features. 

Make 'small', 'medium', 'full' numpy file for initial, mid-way, final experiments in each folder.

For sequential preprocessing, I used h5py with datatype, uint8.

'scale_params.pkl' contains 'columns', 'integer_features', 'binary_features', 'min', 'max', 'mean', 'var', and 'std'. 

To creade 'scale_params.pkl', adopted and modified the class [RunningStates](https://stackoverflow.com/a/17637351)
