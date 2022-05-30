# Bank-customer-churn-using-ANN
ANN model build to predict a bank's customer churn.

# Blog
https://parisrohan.medium.com/bank-customer-churn-prediction-using-ann-6499bf805b6

# Workflow

## 1. Data Description and EDA
* The dataset is downloaded from Kaggle using this link: https://www.kaggle.com/datasets/mathchi/churn-for-bank-customers
* The dataset contains 1000 records and 13 features with no missing values.
* This is an imbalanced dataset as the number of non-churned customers is greater than the number of churned customers.
![image](https://user-images.githubusercontent.com/49038495/171039432-cdc9c51a-b134-49c7-81c2-bbc3a501de2f.png)
* The number of male customers is slightly greater than the number of female customers for the given bank.
![image](https://user-images.githubusercontent.com/49038495/171039505-e0eba954-8c97-486d-bb39-3b16604ff865.png)
* Around 50% of the customers are from the France region and the number of customers from the Spain and Germany region is almost equal.
![image](https://user-images.githubusercontent.com/49038495/171039553-f99e1aa0-78f1-432b-b4cf-f514b8b53d03.png)

## 2. Data preprocessing
The data preprocessing includes applying one-hot encoding on the Geography and Gender features.

## 3. Model Building
* The data is scaled down using StandardScaler after splitting it into train and test data.
* Defining ANN
  * Input Layer — As the training data has 11 features, the input layer will have 11 neurons.
  * Hidden Layer — This depends on the trial. I have chosen 3 hidden layers.
  * Output Layer — As this is a binary classification problem a single neuron will work in the output layer.
* ReLU activation function is applied on the hidden layers and Sigmoid function is applied on th output layer.
* Optimizer used is Adam optimizer.
* The binary cross-entropy loss function is used as this is a binary classification problems.
* Early stopping is used to stop the Neural Network if there is no significant improvement in the model’s accuracy.
* The model scores an accuracy of 85%
![image](https://user-images.githubusercontent.com/49038495/171040302-b750e0a6-5393-49d7-bacb-8786d7aa600f.png)
