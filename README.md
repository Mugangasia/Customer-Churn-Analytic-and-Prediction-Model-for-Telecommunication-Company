![image](https://github.com/Mugangasia/Customer-Churn-Analytic-and-Prediction-Model-for-Telecommunication-Company/assets/98708792/7f9412e9-a773-46a5-9738-d1eee28e40fc)
# Customer Chun Prediction Model
$Author$ - Bravin Mugangasia

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

![image](https://github.com/Mugangasia/Customer-Churn-Analytic-and-Prediction-Model-for-Telecommunication-Company/assets/98708792/eda6d9ea-e12f-422e-ba4f-9471e0a290e9)

* A churn rate of ```0.1449``` (or 14.49%) means that, on average, 14.49% of customers in the given dataset have discontinued or terminated their service within a specific period of time.

* In this context, the churn rate represents the percentage of customers who have churned (cancelled their subscriptions or switched to a competitor's service) out of the total number of customers in the dataset. 
* A higher churn rate indicates a higher rate of customer attrition, which can have negative implications for a business, such as loss of revenue, market share, and customer loyalty.

![image](https://github.com/Mugangasia/Customer-Churn-Analytic-and-Prediction-Model-for-Telecommunication-Company/assets/98708792/cb3281ad-ee93-461a-ae00-4a5ab1463545)
![image](https://github.com/Mugangasia/Customer-Churn-Analytic-and-Prediction-Model-for-Telecommunication-Company/assets/98708792/33917787-546d-499b-a8aa-e60338e6c780)

* The number of days the customer has been with the service provider does not affect the chun rate.
* The total number of minutes the customer used during the day has a negligable relationship between Non-churn and Churn customers.
* The number of customer service calls made by the customer affects the churn rate. WE have high churned subscribers with high customer service calls.
* Most Churn customers are international clients. This might be because of high charges or Tarifs from the telcom provider.

# MODELING
We used three different models to predict Customer Churn. Logistics Regression, Decision Tree, Random Forest, K-Nearest Neighbors and HYperparameter tunning usind GridSearch CV.

#### MODEL 1 : LOGISTICS REGRESSION 

![image](https://github.com/Mugangasia/Customer-Churn-Analytic-and-Prediction-Model-for-Telecommunication-Company/assets/98708792/011ded4a-537c-4c04-8642-812f3b8f57ce)

                             Metrics
                             Accuracy                     0.844078
                             Precision                    0.333333
                             Recall                       0.029703
                             F1 Score                     0.054545
                             Confusion Matrix  [[560, 6], [98, 3]]
                             AUC Score                    0.763916

* Accuracy: ```85.01%``` - This represents the overall accuracy of the model in correctly predicting the target variable on the test data.
* Precision: ```57.14%``` - This indicates the proportion of true positive predictions out of the total positive predictions. It measures the model's ability to avoid false positive predictions.
* Recall: ```3.96%``` - This represents the proportion of true positive predictions out of the actual positive instances in the data. It measures the model's ability to identify positive instances correctly.
* F1 Score: ```7.41%``` - This is the harmonic mean of precision and recall. It provides a single metric to evaluate the balance between precision and recall.
* Confusion Matrix: ```[[563, 3], [97, 4]]``` - This matrix shows the counts of true negatives ```(563)```, false positives ```(3)```, false negatives ```(97)```, and true positives ```(4)```. It provides a detailed breakdown of the model's predictions.
* AUC Score: ```76.89%``` - This represents the area under the Receiver Operating Characteristic (ROC) curve. It measures the model's ability to distinguish between positive and negative instances.

#### MODEL 2 : LOGISTIC REGRESSION 
![image](https://github.com/Mugangasia/Customer-Churn-Analytic-and-Prediction-Model-for-Telecommunication-Company/assets/98708792/68e8e115-3042-47e0-a8c0-fbc33125a157)

                             Metrics
                             Accuracy                     0.844078
                             Precision                    0.333333
                             Recall                       0.029703
                             F1 Score                     0.054545
                             Confusion Matrix  [[560, 6], [98, 3]]
                             AUC Score                    0.763916

* Based on these metrics, ```Model 1``` performs better in terms of accuracy, precision, recall, ```F1 score```, and ```AUC``` score compared to ```Model 2```. ```Model 1``` has higher values for all these metrics, indicating better overall performance in predicting the target variable.

####  MODEL 3 : MODEL 4 : MODEL 5
* Decision Tree
* Random Forest
* K-Nearest Neighbors

Decision Treee:
Accuracy  :  0.925
F1 Score  :  0.747
Precision :  0.763
Recall    :  0.733
ROC AUC Score: 0.846

Random Forest:
Accuracy  : 0.913
F1 Score  : 0.633
Precision : 0.877
Recall    : 0.495
ROC AUC Score: 0.741

KNN:
Accuracy  : 0.855
F1 Score  : 0.171
Precision : 0.625
Recall    : 0.099
ROC AUC Score: 0.544

* Based on these metrics, the Decision Tree model has the highest accuracy, F1 score, precision, and recall among the three models. Additionally, it has the highest ROC AUC score of 0.846, indicating better class separation compared to the other models. Therefore, the Decision Tree model appears to be the best performer among the three models.

![image](https://github.com/Mugangasia/Customer-Churn-Analytic-and-Prediction-Model-for-Telecommunication-Company/assets/98708792/7f1a5159-ab3a-41df-9db3-8ebf5a45a0a4)


# Conclusion 

* ```Random Forest:``` The Random Forest model has the highest AUC score of ```0.897```, indicating better class separation compared to the other models. This suggests that the Random Forest model performs well in distinguishing between the classes.

* ```Decision Tree:``` The Decision Tree model has an AUC score of ```0.846```, which is lower than the Random Forest model but still indicates a good level of class separation. The Decision Tree model performs reasonably well in distinguishing between the classes.

* ```Logistic Regression:``` The Logistic Regression model has an AUC score of ```0.768936```. While it has a lower AUC score compared to the Random Forest and Decision Tree models, it can still provide some level of class separation, although not as strong as the other models.

* ```KNN:``` The KNN model has the lowest AUC score of ```0.597```, indicating relatively weaker class separation compared to the other models. The KNN model may struggle to distinguish between the classes effectively.

Based on the AUC scores alone, the Random Forest model appears to be the best performer among the four models. This would be the best Model for the Telecommunication to use to predict which customer will unsibscribe from their services and take precautionary steps to reduce the chan rate.

# Other Insights 

* The number of days the customer has been with the service provider does not affect the chun rate.

* The total number of minutes the customer used during the day has a negligable relationship between Non-churn and Churn customers.

* The number of customer service calls made by the customer affects the churn rate. WE have high churned subscribers with high customer service calls.

* Most Churn customers are international clients. This might be because of high charges or Tarrifs from the telcom provider.

RECCOMENDATIONS 
Given that Random Forest Does a better job of predicting Customer Churn, we need feature engineering and a larger dataset with more features to help intergrate other factors for better prediction and course of action to be taken.




