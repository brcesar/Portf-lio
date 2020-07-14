#  Credit Card Payment Risk Analysis

This is a supervised statistical/machine learning model (classification) to predict which clients is able to honor their debt.

It was used Python 3.8 and jupyter notebook. The following libraries have been used:
    
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Imblearn
- Pickle

We are going to use the models:
- kNN
- Random Forest
- Logistic Regression
- Naive Bayes
- Support Vector Machines (SVM)

#### The goal is to predict the default target:

- False - Who has paid the bill (here is the negative)
- True - Who has not been able to pay the bill (here is the positive)

## Workflow

   ### (Part I) - Exploratory and Preprocessing Data Analysis

- #### 1 Importing the Libraries and loading the dataset 
    - Imports and dataset loading
    - Initial assessment of the dataset
    - Analyzing the possible classes
- #### 2 Dealing with the Missing and Inconsistent Values
    - Removing the NaN values and transforming the targets 
    - Transforming datetime in integer and calculating the difference between payment and loan datetime
    - Removing inconsistent data
    - Replacing the missing values    
- #### 3 Exploring the data
    - Analyzing the features
    - Inpecting the degree of skewness and tailedness in each feature (which feature has a normal distribution?)
- #### 4 Dealing with outliers
    - Removing the outliers using the Z-score
    - Removing the outliers using Quantiles (IQR score)
    - Checking the distribution of labels after removing the outliers
- #### 5 Correlation and Feature Importance (which feature could affect the result the most?)
    - Correlation
    - Feature Importance
- #### 6 Splitting the dataset in train and test
    - Applying the SMOTE technique to deal with the imbalanced datasets
- #### 7 Feature Scaling
        
### (Part II) - Implementing and Training the model

- #### 8 Training the baseline model
    - Setting the model (kNN) and training
    - Setting the model (Logistic Regression) and training
    - Setting the model (Random Forest) and training
    - Setting the model (Naive Bayes) and training
    - Setting the model (Support Vector Machines SVM) and training
- #### 9 Cross-validation (choosing the best models)
    - Estimating the Recall using a 10-Fold cross-validation
- #### 10 Perfoming the hyperparameter optimization for the best models
    - Using 5-Fold Cross-Validation in RandomizedSearchCV
    - Training the model with the help of the best hyperparameters
- #### 11 Combining the best two models to perhaps boost the performance
    - Setting the combined model (kNN and Random Forest) and training
- #### 12 Evaluating the model's real performance (test dataset)
    - Making predictions in the test dataset
    - The final performance: the confusion matrices
    - Classification report for Random Forest
    - Classification report for kNN
    - Classification report for the combined models
- #### 13 Summary
- #### 14 Saving the Classifier (Final Model)
    - Saving the best trained model
    - Saving the predict class probabilities for test dataset
