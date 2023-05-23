# Business Problem:

The telecommunications company has been experiencing a high rate of customer churn, leading to a loss of revenue and market share. 
The churn rate has been steadily increasing, and it is crucial for the company to address this issue promptly. 
The business problem is to reduce customer churn and improve customer retention.

# Objectives:

Reduce customer churn rate: The primary objective is to decrease the percentage of customers who cancel their subscriptions or switch to a competitor's service. 
The target is to achieve a significant reduction in churn rate within a specified timeframe.

# Data Understanding

* ```State:``` The state in which the customer resides.
* ```Account length:``` The number of days the customer has been with the service provider.
* ```Area code:``` The telephone area code associated with the customer's phone number.
* ```Phone number:``` The customer's phone number.
* ```International plan:``` Whether the customer has an international calling plan (yes or no).
* ```Voice mail plan:``` Whether the customer has a voice mail plan (yes or no).
* ```Number vmail messages:``` The number of voice mail messages the customer has.
* ```Total day minutes:``` The total number of minutes the customer used during the day.
* ```Total day calls:``` The total number of calls the customer made during the day.
* ```Total day charge:``` The total charge for the customer's daytime usage.
* ```Total eve minutes:``` The total number of minutes the customer used during the evening.
* ```Total eve calls:``` The total number of calls the customer made during the evening.
* ```Total eve charge:``` The total charge for the customer's evening usage.
* ```Total night minutes:``` The total number of minutes the customer used during the night.
* ```Total night calls:``` The total number of calls the customer made during the night.
* ```Total night charge:``` The total charge for the customer's nighttime usage.
* ```Total intl minutes:``` The total number of international minutes the customer used.
* ```Total intl calls:``` The total number of international calls the customer made.
* ```Total intl charge:``` The total charge for the customer's international usage.
* ```Customer service calls:``` The number of customer service calls made by the customer.
* ```Churn:``` Whether the customer has churned or not (True or False).

# Results

1. Explaratory Analysis
 
![output](https://github.com/Mugangasia/Customer-Churn-Analytic-and-Prediction-Model-for-Telecommunication-Company/assets/98708792/0d17f407-d22a-42d9-8d3a-96aaa6e45c0d)

* Majority of the DataFrame has subscribers on the ```international Plan``` ans ```Voice Mail Plan.```

![image](https://github.com/Mugangasia/Customer-Churn-Analytic-and-Prediction-Model-for-Telecommunication-Company/assets/98708792/d882e9e0-c2c5-4709-b7ce-9fffd21b31e3)
* The ```churn``` Distribution is normally Distributed between the ```False``` and ```True``` Values.
* The CUstomer service calls have outliers but they are not true outliers. WE will keep them in the analysis.

![image](https://github.com/Mugangasia/Customer-Churn-Analytic-and-Prediction-Model-for-Telecommunication-Company/assets/98708792/c2ae4861-bcc6-4958-981d-511796a16642)
* A churn rate of ```0.1449``` (or 14.49%) means that, on average, 14.49% of customers in the given dataset have discontinued or terminated their service within a specific period of time.

* In this context, the churn rate represents the percentage of customers who have churned (cancelled their subscriptions or switched to a competitor's service) out of the total number of customers in the dataset. 
* A higher churn rate indicates a higher rate of customer attrition, which can have negative implications for a business, such as loss of revenue, market share, and customer loyalty.





