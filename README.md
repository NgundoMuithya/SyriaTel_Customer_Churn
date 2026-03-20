<img src='./Images/Telecommunication.webp' style='width: 100%; height: 400px; object-fit: cover;' />

---
<h1 align='center'>
SYRIATEL CHURN ANALYSIS
</h1>

> **Author**: Ngundo Muithya

> **Email**: ngundolarrymuithya@gmail.com

---

<h2 align='center'>
1. INTRODUCTION
</h2>

### Overview

SyriaTel is a leading Syrian mobile telecommunication company established in the year 2000, headquartered in Damascus, providing GSM and LTE services

SyriaTel is interested in predicting whether a customer will churn (stop working with the company) or not.

I will create a predictive model that will help determine if a customer will churn or not.

I will do this by using the publicly available SyriaTel customer information (stored [here](./Data/syriatel_data.csv)) on churning to create two models: a **logistic regression model** and a **decision tree** and use model evaluation to determine which is better at predicting whether or not a customer will churn.

### Business Understanding

The business objectives are:
* Create a model that reliably predicts whether or not a customer will churn
* Identify the attributes that are most likely to cause churning
* Develop recommendations on how to limit churning

I will focus on two types of classifiers: **logistic regression models** and **decision trees**

---

<h2 align='center'>
2. DATA UNDERSTANDING
</h2>

I will use the publicly available data on churning provided by SyriaTel [here](./Data/syriatel_data.csv)

It contains various information about customers, including whether or not they will churn.

A descriptive definition of the columns is located [here](./Data/SyriaTel_Dataset_Feature_Dictionary.txt)

### Exploratory Data Analysis

I discovered that the data contained no empty or duplicate values.

I performed data cleaning and performed some visualization:

#### Churn Percentage by International Plan Status

<img src='./Images/Churn_Percentage_By_International_Plan_Status.png'/>

88% of those without international plans stayed while only 57% of those with international plans stayed.

#### Churn Distribution by Voice Mail Plan

<img src='./Images/Churn_Distribution_By_Voice_Mail_Plan.png'/>

A customer with a voice mail plan is less likely to churn compared to one without a voice mail plan although they are both more likely to stay.

<h2 align='center'>
3. MODEL BUILDING
</h2>

### a) Logistic Regression

I determined the dataset had class imbalance

I built two logistic models: one **using class weights** and another **using SMOTE** and compared the two to get the best one.

#### i) Using Class weights

##### Recall scores for logistic models using different clas weights