# User Churn Prediction

This project aims to implementing supervised machine learning models to predict user churn probability for telecommunication company. 

The project is divided into four parts:

1. Data Exploration: In this part, we know the size of raw dataset and get the number of data for each class and the number of feature. The number of data is 5000 and the number of feature is 21. The number of churn data is 707 which account for 14.14% and the number of non-churn data is 4293 which account for 85.86%. we can see the data is a little imbalanced. We also remove some whitespaces in variable with string format and check the null value. Then we find the distribution of each feature for each class. Some features are indistinguishable and some features are corelated.

2. Feature Preprocessing: In this part, we extract the label vector, tramfrom yes and no value to boolen value and use one-hot encoding to add the categorical variable to featrue matrix. Then standardize the dataset to reduce the influence of feature with large value. 

3. Model Training and Result Evaluation: In this part, we split the data and train Logistic Regression, K-Nearest Neighbors, SVM and Random Forest models to predict user churn probability by sklearn. And use grid search and cross validation to find optimal hyper-parameters and evaluate the performance using accuracy, precision, recall, F1 value, ROC and AUC. The random forest model have the best performance over these models. Accuracy is 0.951. Precision is: 0.918. Recall is: 0.685. F1 value is: 0.784. 

<div align=center>
<img src="https://raw.githubusercontent.com/TengM95/User_Churn_Prediction/master/ROC_rf.png"/> 
<img src="https://github.com/TengM95/User_Churn_Prediction/blob/master/cm_rf.png"/>
 </div>
   
   
   
   
4. Feature Selection: In this part, we analyze the feature based on the model. The different coefficients of l1 and l2 logistic regression models show the defferent influence of l1 and l2 regularization. The coefficients of l1 model are much more sparse. Based on the random forest model, we can get the importance of each feature.
