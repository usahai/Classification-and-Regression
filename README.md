# Classification and Regression

This is a basic regression and classification analysis. 

<u>Regression</u>

K Nearest Regressors - These are not commonly used in Regression. The purpose of this is to show the difference in train and test rate as the value of k increases.  There is clearly an overfitting problem here.

Linear Regression - 5 folds, returns best training and testing score

Polynomial Regression - Power to the squared, i.e. degree=2. Plot shows this is not a good fit.

<u>Regularizers</u>
Ridge - Hyper-parameter ALPHA set to [0.001,0.01,0.1,1,10,100,1000]. Best parameters returned from GridSearchCV

Lasso - Plot shows a dip in train and test accuracy as the value of hyper-parameter ALPHA increases.

LinearSVR - Extremely poor train and test scores.

SVR with Kernel Trick - Since LinearSVR uses the linear kernel, we can 'trick' the SVR module into running the same model by setting the kernel to linear, and then tuning the 2 hyper-parameters: gamma and C (penalty of the error term).

Decision Tree Regressor - I understand that these are also not commonly used in Regression. However, I ran this from a learning stand point to understand 2 things. 1. How do traditional classifiers running as regressors stack up against traditional regression algorithms. 2. How to acutally run them should the need arise.

<u>Classification</u>

KNN Classifier - Ran it with 1,5,10,15,20 neighbors. Best score came when there was 1 NN, while train and test scores were 1.00 and 0.86. I believe that there was an overfitting problem here. I used a scatter plot to show the classification of the datapoints in the grid

Logistic Regression - Ran with the penalty of the error term at [0.001,0.01,0.1,1,10,100,1000], and with both Lasso (l1) and Ridge(l2) regularizers to mitigate the overfitting problem.

LinearSVC - Ran with no hyper-parameters. 5 folds. Train and test scores were 0.89 and 0.87 respectively.

SVC with Kernel Trick - Since LinearSVC uses the line[InternetShortcut]
URL=https://github.com/usahai
ar kernel, we can 'trick' the SVC module into running the same model by setting the kernel to linear, and then tuning the 2 hyper-parameters: gamma and C (penalty of the error term). Train and test scores after 'tricking' the classifier were 0.89 and 0.92 respectively. Heatmap to show the scores of the tuning of the 2 parameters.

Decision Tree Classifiers - Max_depth range set from 1-20, random_state fixed to ensure the model gives consistent results. Plotted the train and test scores at each max_depth. 
