# Financial-Loan-Default-Prediction
Binary classification using Logistic, Lasso, MLP, RNN

# Dataset
The dataset is from Kaggle: [BankCreditDefault](https://www.kaggle.com/datasets/kornilovag94/bank-credit-default-loan-default)

The data is sequential(length 1 to 20) for each unique ID. 

I used last only data for Logistic, Lasso, and MLP, while I used full sequential data for RNN. 

### Preprocessing
Used standard scaler for interger features, and one hot encoder for binary features. 

For sequential preprocessing, I used h5py. 
