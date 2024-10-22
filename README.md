# Capstone-Project--Telecom-Churn
## Problem Statement

In the telecom sector, customers have numerous options when it comes to service providers, and they frequently switch between operators. This intense competition has led to an industry churn rate of 15-25% annually. Since acquiring new customers can be 5-10 times more costly than retaining current ones, customer retention has become a higher priority than customer acquisition.
For many established telecom companies, the top business objective is to retain their most profitable customers.
To address customer churn, telecom companies must predict which customers are most likely to leave.
In this project, we will analyze customer-level data from a leading telecom company, build predictive models to forecast high-risk churn customers, and identify the key drivers of churn.

## Steps to Approach
### Step 1:
Data reading and understanding.<br>
Data cleaning and imputing missing values.<br>
### Step 2:
Filter out high-value customers
### Step 3:
Derive the churn target variable
### Step 4:
Data preparation, including creating derived variables and performing exploratory data analysis (EDA) <br>
Split the data into training and testing sets <br>
Apply scaling <br>
### Step 5:
Address class imbalance <br>
Perform dimensionality reduction using PCA <br>
Build classification models to predict churn using various algorithms <br>
### Step 6:
Model evaluation <br>
Prepare models for predictor variable selection, testing multiple models and choosing the best one <br>
The goal is to provide the company with a well-rounded summary and insights based on the best-performing model. <br>

## Understanding and Defining Churn
Understanding and defining churn <br>
There are two main models of payment in the telecom industry - postpaid (customers pay a monthly/annual bill after using the services) and prepaid (customers pay/recharge with a certain amount in advance and then use the services).
In the postpaid model, when customers want to switch to another operator, they usually inform the existing operator to terminate the services, and you directly know that this is an instance of churn.
However, in the prepaid model, customers who want to switch to another network can simply stop using the services without any notice, and it is hard to know whether someone has actually churned or is simply not using the services temporarily (e.g. someone may be on a trip abroad for a month or two and then intend to resume using the services again).
Thus, churn prediction is usually more critical (and non-trivial) for prepaid customers, and the term ‘churn’ should be defined carefully.  Also, prepaid is the most common model in India and Southeast Asia, while postpaid is more common in Europe and North America.
This project is based on the Indian and Southeast Asian market.

## Definitions of churn
There are various ways to define churn, such as:

## Revenue-based churn: 
Customers who have not utilised any revenue-generating facilities such as mobile internet, outgoing calls, SMS etc. over a given period of time. One could also use aggregate metrics such as ‘customers who have generated less than INR 4 per month in total/average/median revenue.
The main shortcoming of this definition is that there are customers who only receive calls/SMSes from their wage-earning counterparts, i.e. they don’t generate revenue but use the services. For example, many users in rural areas only receive calls from their wage-earning siblings in urban areas.

## Usage-based churn: 
Customers who have not done any usage, either incoming or outgoing - in terms of calls, internet etc. over a period of time.
A potential shortcoming of this definition is that when the customer has stopped using the services for a while, it may be too late to take any corrective actions to retain them. For e.g., if you define churn based on a ‘two-months zero usage’ period, predicting churn could be useless since by that time the customer would have already switched to another operator.

 
