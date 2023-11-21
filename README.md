# Financial-Loan-Default-Prediction
Binary classification using Logistic, Lasso, MLP, RNN

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

For sequential preprocessing, I used h5py with datatype, uint8.

Make 'small', 'medium', 'full' numpy for initial, mid-way, final experiments in each folder.
