# SyriaTel Customer Churn Analysis
<img src="images/syriaTellogo.jpg" alt="House" width=200 height=200 />

## Overview
This project analyses aspects of telecommunications to understand what causes people to stop taking the calls/doing business with them. This project uses logistic regression, random forest and k nearest neighbor to understand this binary classification problem.

## Business Problem
<img src="images/syriaTel.jpg" alt="House" width=200 height=200 />


SyriaTel, a telecommunications company wants to know whether there are any indicators of whether a customer will stop doing business with them. The goal is to predict what measures are causing customers to 'churn' or leave the Telecom company. This could lead to customer retention if understanding what aspects of the customer interaction are causing them to 'churn'.



## Data Understanding
The data provided is csv file of data collected from SyriaTel involving aspects of their interactions with customers, such as when they are calling, how long they are on the phone, if it is an international phone call, and how much was charged per call. 
The highest correlated features with churn were total day minutes on the phone and total day charge of the phone calls. It is depicted below in a correlation heatmap. 

![image](https://user-images.githubusercontent.com/65221687/193645245-1e247b25-26b0-4849-9512-65dade565abd.png)

## EDA

In exploring the data it was found that 15% of people are churning away from the company.
![image](https://user-images.githubusercontent.com/65221687/193645416-8eec9388-6fb7-48b4-8fc0-c9afe602a1ca.png)

Feature selection using the highest model Random Forest for the importances:
![image](https://user-images.githubusercontent.com/65221687/193648361-1fe0800c-966c-41b1-8e51-4b90d7b0cea7.png)
![image](https://user-images.githubusercontent.com/65221687/193648382-7fdd8f56-2a11-4e21-b50c-1bb4108c10bf.png)



## Modeling
After instationating Logistic regression, K-Nearest Neighbors, Random Forest, Decision Trees, Naive Bayes, and Vector Support, the highest accuracy was recorded with Random Forest. 



![image](https://user-images.githubusercontent.com/65221687/193645454-51a8c796-57c0-47dd-a347-750dd8c2e64d.png)

![image](https://user-images.githubusercontent.com/65221687/193645480-797f3032-1957-4522-9931-a7be5f8c4d61.png)

## Hypertuning

Three types of models were used for hypertuning, Logistic Regression, K-Nearest Neighbors, and Random Forest. The Random Forest was still the highest model after hypertuning as it was before hypertuning as depicted in the model comparison figure below. 


