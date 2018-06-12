# Risk-Classification-for-Insurance-Customers---Prudential-Dataset-Kaggle

This project is a part of a kaggle competition put up by Prudential Insurance company. IN USA the insurance process is considered as time consuming as companies usually take about 30 days to classify risk for a customer and come up with quotation. As a result most of the people get turned off. So the idea behind this is to build a machine learning model that can automate the process of classifying risk into 8 different ordinal categories. 


The dataset consists of 128 features comprising of continuous, discrete and ordinal variables. The target variable is an ordinal variable with 8 different risk categories, 1 -> less risky ; 8 -> most risky. Initially I had to perform some data cleaning and pre-processing such as removing columns with large number of missing values, data imputation, dummy encoding variables and outlier detection. 


After dummy encoding, I was left with 204 variables. Implemented Pricipal Component analysis to optimize the number of components retaining as much information as possible. After exploring PCA results with scree plot, I was able to do dimensionality reduction having 50 columns in my final data frame retaining 98% of variance. 


Finally implemented ML models to classify risk with as much accuracy as possible. Implemented Multinomial regression, Support Vector Machines and Neural Networks. However on performing k fold cross validation with hyperparameter tuning, my code wasn't giving output for more than 30 hours. Such was the computation required which was not feasible from my computer. 


So I did some kind of trial and error and implemented the 3 models. I wasn't able to perform CV and tune hyperparameters. With better computation, accuracies can further be increased. I have commented the code that can be run to get best accuracies given computational efficiency. 


Base model accuracy was 32%. The goal is to build upon this to further increase accuracy. Implemented multinomial regression to get accuracy of 44%. Support Vector Machine with gaussian kernel to get accuracy of 53% on train set and 47% on test set. Neural Network with 10 neurons in 1 hidden layer to get accuracy on test set as 48%. Built an ensemble model above these 3 models with "voting" to increase accuracy but could not get more accuracy than neural networks.


Accuracy with neural network seems really good. So with enough computation, more layers and neurons can be added to neural net to get high accuracies. According to me, neural networks is the way to go for Prudential Dataset. 
