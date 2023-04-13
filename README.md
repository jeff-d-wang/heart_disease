# heart_disease

## Introduction: 
Heart Disease is one of the leading causes of death but it can be detected early through various measurements and thus be prevented through early action. This problem is interesting because by running models to understand possible correlations between features and some form of heart disease, we can analyze possible avenues of early testing for patients to predict their risk for such diseases. My approach was to see any interesting visual or immediate correlations between certain features and the target value then to run models like Decision Tree and Logistic Regression to compare accuracy and feature importances.

## Setup:
The Heart Disease dataset from UCI is a multivariate type that contains 14 attributes: age, sex, chest pain type, resting blood pressure, serum cholesterol, fasting blood sugar, resting electrocardiographic results, maximum heart rate achieved, exercise induced angina, oldpeak — ST depression induced by exercise relative to rest, the slope of the peak exercise ST segment, number of major vessels and Thalassemia. There were originally 76 features but published studies only refer to these 14 to be useful. The dataset was sourced from various hospitals like from Cleveland (main source), Hungary, Switzerland, and VA Long Beach though the last three have a lot of missing values and are thus not included in the main dataset. The data needed a bit of work because some features were catagorical so I used one-hot encoding to resolve some of the attributes like chest pain and angina. I will use Decision Tree Regression because past papers and research have shown that using such with 10 fold cross validation has been successful with this dataset and other related ones because of their ability to factor in all features and calculate probabilities within them, giving us a good idea of the problem. From there, I will test various values for the hyper-parameters like tree-depth through trial and error.

## Results:
From the base model, we see an accuracy of 75.41% and the main attributes it found useful were cp (chest pain), exang (exercise induced angina), trestbps (resting blood pressure), age, chol (cholesterol), and oldpeak (ST depression induced by exercise relative to rest). Through tuning the hyperparameters of the same model, we got an improvement of accuracy to 75.41% with the same features being noted as important for decision making. Through logistic regression with cross validation of 10 folds, I got an accuracy of 80.33%.

## Discussion:
Not great, could be better. Trying KNN, SVM, Naive Bayes, Random Forest, NN.

## Conclusion:
In several sentences, summarize what you have done in this project.