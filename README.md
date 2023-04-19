# HeartDiseaseClassification 
Classification of patients on possibly having a heart disease or not, based on personal answers data about their health and life styles.

## 1. Problem
How to classify patients in possibly having a heart disease or not based on personal answers data about their health and life styles using Machine Learning models?

## 2. Data
The data I'm using is from Kaggle's heart disease classification competition (https://www.kaggle.com/c/heart-disease-uci/data).

## 3. Evaluation
Evaluation was made using estimators.

## 4. Features
I'm dealing with structured data, containing 14 variables for over 300 patients.

## 5. Code and resourses used
**Python version:** 3.7

**Packages:** Pandas, NumPy, Matlplotlib and Scikit-Learn

## 6. EDA
Getting into know the DataFrame:
* How many columns does it have?
* What do they mean?
* What kind of data (numerical, strings etc.) do they have?
* Is there any missing data?

For each DataFrame column there's a description:
1. age - The age of the patient;
2. sex - The gender of the patient. (1 = male, 0 = female);
3. cp - Type of chest pain. (1 = typical angina, 2 = atypical angina, 3 = non — anginal pain, 4 = asymptotic);
4. trestbps - Resting blood pressure in mmHg;
5. chol - Serum Cholestero in mg/dl;
6. fbs - Fasting Blood Sugar. (1 = fasting blood sugar is more than 120mg/dl, 0 = otherwise);
7. restecg - Resting ElectroCardioGraphic results (0 = normal, 1 = ST-T wave abnormality, 2 = left ventricular hyperthrophy);
8. thalach - Max heart rate achieved;
9. exang - Exercise induced angina (1 = yes, 0 = no);
10. oldpeak - ST depression induced by exercise relative to rest;
11. slope - Peak exercise ST segment (1 = upsloping, 2 = flat, 3 = downsloping);
12. ca - Number of major vessels (0–3) colored by flourosopy;
13. thal - Thalassemia (3 = normal, 6 = fixed defect, 7 = reversible defect);
14. num - Diagnosis of heart disease (0 = absence, 1, 2, 3, 4 = present).

After that, I started to explore the correlations between variables by making a correlation matrix, for example:

![image](https://user-images.githubusercontent.com/106838561/233213143-59c5e135-16d3-4783-a250-ac51d974ab58.png)

## 7. Modelling
I made a comparison between three classification models:
* Logistic Regression
* K-Nearest Neighbors Classifier
* Random Forest Classifier

## 8. Results
Initially I was able to get each model's score for accuracy:
* Logistic Regression = **0.89**
* K-Nearest Neighbors Classifier = **0.69**
* Random Forest Classifier = **0.85**


![image](https://user-images.githubusercontent.com/106838561/233213904-1aa8eb94-b1c1-4aa0-8e5f-62dde49bc29e.png)

Then some hyperparameter tunning was made for Logistic Regression model since it delivered the best accuracy. For that I used RandomizedSearchCV and GridSearchCV, getting **0.87** as the accuracy for the first one and **0.89** for the second one.

Finally, I evaluated the tuned machine learning classifier using ROC curve and AUC score, confusion matrix, classification report, precision, recall and F1-score, obtaining the scores shown as follows:

![image](https://user-images.githubusercontent.com/106838561/233215522-302d49c0-debd-42a9-9410-843ce0165263.png)

Also, I was able to plot a graphic for visualization the feature importance in this problem:

![image](https://user-images.githubusercontent.com/106838561/233215721-6f3342ba-27c5-41bf-878d-1adbe93cf11e.png)
