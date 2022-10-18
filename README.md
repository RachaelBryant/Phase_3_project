# SyriaTel Customer Churn Analysis
<img src="images/syriaTellogo.jpg" alt="House" width=200 height=200 />

## Overview
This project analyses aspects of telecommunications to understand what causes people to stop taking the calls/doing business with them. This project uses logistic regression, random forest and K-Nearest neighbor to understand this binary classification problem.

## Business Problem
<img src="images/syriaTel.jpg" alt="House" width=200 height=200 />


SyriaTel, a telecommunications company wants to know whether there are any indicators of whether a customer will stop doing business with them. The goal is to predict what measures are causing customers to 'churn' or leave the Telecom company. This could lead to customer retention if understanding what aspects of the customer interaction are causing them to 'churn'.



## Data Understanding
The data provided is csv file of data collected from SyriaTel involving aspects of their interactions with customers, such as when they are calling, how long they are on the phone, if it is an international phone call, and how much was charged per call. 
The highest correlated features with churn were total day minutes on the phone and total day charge of the phone calls. It is depicted below in a correlation heatmap. 

![image](https://user-images.githubusercontent.com/65221687/193645245-1e247b25-26b0-4849-9512-65dade565abd.png)

## EDA

In exploring the data it was found that 15% of people are churning away from the company.

![image](https://user-images.githubusercontent.com/65221687/194056262-8c758279-4a74-4ad2-9868-dea94194aa55.png)

With SMOTE applied to address the imbalance within the data.

![image](https://user-images.githubusercontent.com/65221687/196063564-77ab98b4-a6fa-4928-82ec-3f7829bd8741.png)


Feature selection using the highest model Random Forest for the importances:
![image](https://user-images.githubusercontent.com/65221687/193648361-1fe0800c-966c-41b1-8e51-4b90d7b0cea7.png)
![image](https://user-images.githubusercontent.com/65221687/193648382-7fdd8f56-2a11-4e21-b50c-1bb4108c10bf.png)



## Modeling
After instationating Logistic regression, K-Nearest Neighbors, Random Forest, Decision Trees, Naive Bayes, and Vector Support, the highest accuracy was recorded with Random Forest. 

![image](https://user-images.githubusercontent.com/65221687/193645480-797f3032-1957-4522-9931-a7be5f8c4d61.png)
![image](https://user-images.githubusercontent.com/65221687/194055082-d83a8d86-eb06-4770-a289-e9293b25a7c3.png)


## Hypertuning

Three types of models were used for hypertuning, Logistic Regression, K-Nearest Neighbors, and Random Forest. The Random Forest was still the highest model after hypertuning as it was before hypertuning as depicted in the model comparison figure below. Only the K-Nearest Neighbor model showed improvement from the basemodel however, it can be noted that the basemodel for Random forest at 95% is already high. 

![image](https://user-images.githubusercontent.com/65221687/196063506-f27bfa0a-00e3-48ff-ae2f-dd3a143e4622.png)
![image](https://user-images.githubusercontent.com/65221687/196063088-bd17723b-aae3-4fd7-8207-95824cdeb4d3.png)



Hypertuned SMOTE models


![image](https://user-images.githubusercontent.com/65221687/196063064-9fd4ff2d-cea9-443f-9504-9dc83753ead7.png)
![image](https://user-images.githubusercontent.com/65221687/196063076-37893788-7c64-4d08-9261-77c5b2a37980.png)



## Creating New Data to Best Model
In order to test exactly which aspects are effecting churn, new data sets were copied from the original and then altered in regards to the the two most significant features, total day minutes and total day charged.

The total day minutes was decreased by a standard deviation to understand whether lessening the total day minutes on the phone could lessen churn. 
Utilizing the Random Forest hypertuned model, which had the highest recall, on the new data it produced a training set accuracy of 1 and a test set accuracy of .948, greatly supporting this model and the importance of this feature in terms of churn.

For the second new data set, the total day minutes was one standard deviation less from the original data, the same as the first new dataset, and also the column total day charged was dropped due to potential collinearity because both features had the same amount of correlation to churn. TFor the second manipuated copied data, we kept the one standard deviation lessened total day minutes, but we also dropped total day charge from the data set because of the potential for collinearity. It did not improve the training set with 1 and the test set slightly worsebed to .712.

## Recommendations
-Shorter phone calls may lead to higher retention rates.
-Whether daily or hourly, how payment is collected will effect churn as well. Changing the method from daily to hourly could discourage churn.

# For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/rabrya0072/Phase_3_project/blob/main/Phase%203%20project.ipynb) or [presentation](https://github.com/rabrya0072/Phase_3_project/blob/main/presentation.pdf.pdf)) in this repository.

For additional info, contact Rachael Bryant at Rachaelbryant@flatironschool.com
# Repository Structure
├── code
│   ├── __init__.py
│   ├── data_preparation.py
│   ├── visualizations.py
├── data
├── images
├── README.md
├── presentation.pdf
└── Phase_3_project.ipynb


