![1684888953690](image/README/1684888953690.png)



# TELECOM CHURN PROJECT

Written by Fiona Njuguna

Phase 3 Project

> This project is a part of the [Data Science (DSF-FT) Course](https://moringaschool.com/courses/data-science-course/) at [Moringa School](https://moringaschool.com/). The full project description can be found [here](https://www.kaggle.com/datasets/shilongzhuang/telecom-customer-churn-by-maven-analytics).

## Overview

Churn is a metric that shows customers who stop doing business with a company or a particular service. Customers in the telecom sector have a variety of service providers to choose from and can actively switch between operators. The telecoms sector has a turnover rate of 15 to 25 percent annually in this fiercely competitive market. Customer retention is becoming even more crucial than acquiring new customers because it costs 5–10 times more to do so than to keep an existing customer.

---



## 1. Business Understanding

### Business Problem

In this project, I analyse customer data from Emvinah Telecommunication Ent, build predictive models to identify reasons that cause customer churning by identifying the indicators of churning from the features used in the predictive models.

#### Specific Objectives

* To identify the trends/patterns between both customers that churn and customers that stayed
* To identify customers that churn using a basic analysis and predict the chances of a customer churning based on available variables
* To identify the best machine learning model for accurately classifying churned and non-churned consumers.

#### Research Questions

* How can we apply Machine Learning and necessary classification methods to predict customer churning in Telecom?
* Are there suggestions help advise on what to do to avoid increase in customer churning rate?

### 1.3 Success Criteria

Metrics that will be used to gauge this model's effectiveness are:

* An accuracy score of over 85%

---

## 2. Data Understanding

#### 2.1 Data Description


* The data set used contains information about features that affect customer churning.
* It contains 7043 records and 38 columns.(23 categorical, 15 numeric).
* A full description of all the features in the DataFrame can be found [here]([https://www.kaggle.com/datasets/shilongzhuang/telecom-customer-churn-by-maven-analytics](https://www.kaggle.com/datasets/shilongzhuang/telecom-customer-churn-by-maven-analytics)).

---



## 3. Data Cleaning

The dataset had a couple of missing values in various columns such as:

* Churn Category
* Churn Reason
* Online Security
* Online Back up...among others

Columns with a high missing values percentage were dropped from the dataframe since they could affect the distribution of the data.

Those with a less missing values percentage were filled using forward fill. 

Forward fill helps maintain the trends and patterns present in the data.

By using the most recent observed value to fill missing values, it allows for the preservation of any existing patterns or relationships that might exist in the dataset.

---

## 4. Modelling

The target variable for this was the column 'Customer Status' that signified the customers that churned and those that stayed. 

Label Encoding was performed on the boolean categorical columns while One Hot Encoding was performed on the non_boolean categorical columns.

The two were then put together as well as the numerical columns to form one dataframe for modelling analysis.

The baseline model was the Dummy Classifier with StandardScaler as our scaler used to test the chosen features on a basic level. 

More sophisticated models explored in modelling were:

* K-Nearest Neighbors
* Decision Tree
* Random Forest

---

## 5. Evaluation

Pipelines were used to scale and fit the models.

Cross Validation was used to ensure thta the models were not overfitting or underfitting.

Confusion matrixes were also plotted to evaluate and visualize the performance of the model.

The success metric used for model evaluation was an Accuracy of 85%.

From the model predictions above, the model that reached the desired accuracy score was the Random Forest model and performed better after parameter tuning and performing a cross validation on it.

It improved by a slight percentage increase of 1%.

---

## 6. Conclusion


* The model best fit to use in predicting customer churn predictions is the Random Forest model since it managed to acquire our desired accuracy score.
* Telecom firms can lower customer churn and raise customer satisfaction by using machine learning approaches for churn prediction, studying customer behavior and patterns.
* The identified predictors and patterns can help in accurately classifying customers that churned and those that stayed.
* The likelihood that a customer would leave can be predicted using the given factors and the right  techniques.

---

## 7. Recommendations


* Consider using techniques like feature selection or feature importance to identify the most influential variables for churn prediction.
* Work together with business stakeholders to comprehend their needs, take advantage of their subject-matter expertise, and match the churn prediction model with business objectives and strategies.
* Validate the models on an independent test set to assess their performance on unseen data.
