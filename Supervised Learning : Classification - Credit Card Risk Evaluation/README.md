{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#  Credit Card Payment Risk Analysis\n",
    "\n",
    "This is a supervised statistical/machine learning model (classification) to predict which clients is able to honor their debt."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "It was used Python 3.8 and jupyter notebook. The following libraries have been used:\n",
    "    \n",
    "- Pandas\n",
    "- NumPy\n",
    "- Scikit-learn\n",
    "- Matplotlib\n",
    "- Seaborn\n",
    "- Imblearn\n",
    "- Pickle"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "We are going to use the models:\n",
    "- kNN\n",
    "- Random Forest\n",
    "- Logistic Regression\n",
    "- Naive Bayes\n",
    "- Support Vector Machines (SVM)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Dataset Information:\n",
    " - 26 features\n",
    " - 64591 samples\n",
    " - 2 classes"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### The goal is to predict the default target:\n",
    "\n",
    "- False - Who has paid the bill (here is the negative)\n",
    "- True - Who has not been able to pay the bill (here is the positive)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Workflow\n",
    "\n",
    "   ### (Part I) - Exploratory and Preprocessing Data Analysis\n",
    "\n",
    "- **1 Importing the Libraries and loading the dataset** \n",
    "    - Imports and dataset loading\n",
    "    - Initial assessment of the dataset\n",
    "    - Analyzing the possible classes\n",
    "- **2 Dealing with the Missing and Inconsistent Values**\n",
    "    - Removing the NaN values and transforming the targets \n",
    "    - Transforming datetime in integer and calculating the difference between payment and loan datetime\n",
    "    - Removing inconsistent data\n",
    "    - Replacing the missing values    \n",
    "- **3 Exploring the data**\n",
    "    - Analyzing the features\n",
    "    - Inpecting the degree of skewness and tailedness in each feature (which feature has a normal distribution?)\n",
    "- **4 Dealing with outliers**\n",
    "    - Removing the outliers using the Z-score\n",
    "    - Removing the outliers using Quantiles (IQR score)\n",
    "    - Checking the distribution of labels after removing the outliers\n",
    "- **5 Correlation and Feature Importance (which feature could affect the result the most?)**\n",
    "    - Correlation\n",
    "    - Feature Importance\n",
    "- **6 Splitting the dataset in train and test**\n",
    "    - Applying the SMOTE technique to deal with the imbalanced datasets\n",
    "- **7 Feature Scaling**\n",
    "        \n",
    "### (Part II) - Implementing and Training the model\n",
    "\n",
    "- **8 Training the baseline model**\n",
    "    - Setting the model (kNN) and training\n",
    "    - Setting the model (Logistic Regression) and training\n",
    "    - Setting the model (Random Forest) and training\n",
    "    - Setting the model (Naive Bayes) and training\n",
    "    - Setting the model (Support Vector Machines SVM) and training\n",
    "- **9 Cross-validation (choosing the best models)**\n",
    "    - Estimating the Recall using a 10-Fold cross-validation\n",
    "- **10 Perfoming the hyperparameter optimization for the best models**\n",
    "    - Using 5-Fold Cross-Validation in RandomizedSearchCV\n",
    "    - Training the model with the help of the best hyperparameters\n",
    "- **11 Combining the best two models to perhaps boost the performance**\n",
    "    - Setting the combined model (kNN and Random Forest) and training\n",
    "- **12 Evaluating the model's real performance (test dataset)**\n",
    "    - Making predictions in the test dataset\n",
    "    - The final performance: the confusion matrices\n",
    "    - Classification report for Random Forest\n",
    "    - Classification report for kNN\n",
    "    - Classification report for the combined models\n",
    "- **13 Summary**\n",
    "- **14 Saving the Classifier (Final Model)**\n",
    "    - Saving the best trained model\n",
    "    - Saving the predict class probabilities for test dataset\n",
    "\n"
   ]
  }
