# Demand Prediction
# by Kong Yin Zeong


### Problem Statement

Sales forecast helps in overall business planning, budgeting, and risk management. It is an important part of making business decisions. A proper sales forecast allows companies to allocate resources for future growth and manage its cash flow efficiently. This project aims to perform sales prediction of the following month for every items at every warehouse of a manufacturing company so that the company can allocate resources and have a proper planning of stock replenishment every month.

In this project, 4 weeks sales will be predicted with various models and the performance of the models will be evaluated. 

---

### Assumptions

The data acquired from Kaggles consists of 2160 products and products are being supplied to 4 different warehouses. Given the nature of the data, I believe it is safe to assume that we can predict the following 4 weeks sales with times series (Arima/Sarimax) and LSTM models. Since there is no name given to each product other than the product code and category code, we assume the products in the same category should have higher correlation with each other.

---

### Data

The data is collected from a few sources as listed below.

* Forecasts for Product Demand ([source](https://www.kaggle.com/datasets/felixzhao/productdemandforecasting?select=Historical+Product+Demand.csv))

---

### Data Dictionary

|Feature|Type|Description|
|---|---|---|
|Product_Code|*string*|The product name encoded|
|Warehouse|*string*|Warehouse ID|
|Product_Category|*string*|Product category of each product|
|Date|*string*|The date customer needs the product|
|Order_Demand|*string*|Order quantity|

---

### Summary

Product 1359 has the highest order count and also ordered quantity. I take Product 1359 as my "top" product and modelling is done revolving Product 1359 in the beginning. Once we have optimized the model, we can duplicate the same model to the other products.

---

### Conclusion

Objective of this project is achieved where the model is able to predict the number of dengue cases based on weather data and Google trend. Out of the few algorithms tested, XGBoost gives the best results in terms of accuracy and RMSE score. A cost-benefit analysis has been conducted to determine the breakeven point of pesticide spraying cost and the cost of dengue fever.

---

### Recommendation

|             Items             	| Cost (SGD) 	|
|:-----------------------------:	|:----------:	|
| Fumigation (every two weeks)  	| 2,778      	|
| Treatment                     	| 112.5      	|
| **Breakeven number of cases** 	|   **25**   	|

Based on the cost-benefit analysis, it is recommended to perform pesticide spraying when the average case per fortnight is more than 25.

