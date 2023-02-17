# Demand Prediction
# by Kong Yin Zeong


### Problem Statement

Sales forecast helps in overall business planning, budgeting, and risk management. It is an important part of making business decisions. A proper sales forecast allows companies to allocate resources for future growth and manage its cash flow efficiently. This project aims to perform sales prediction of the following month for every items at every warehouse of a manufacturing company so that the company can allocate resources and have a proper planning of stock replenishment every month.

In this project, 4 weeks sales will be predicted with various models and the performance of the models will be evaluated. 

---

### Assumptions

Aedes mosquitoes prefer to breed in clean, stagnant water such as flower vases, flower pot plates, roof gutters, earthen jars for water storage or decorative purposes, watering cans, and bamboo pole holders. Many of the breeding sites mentioned accumulate stagnant water easily especially when there it is raining. Therefore, the breeding of Aedes mosquitoes indirectly linked to th weather. Hypothetically, we could predict the number of dengue cases with weather data.

Besides weather data, we could also make use of Google trend in various search term to predict number of dengue cases. The logic behind this is people usually Google search the sypmtoms when they are suspecting they have any disease.

Based on the problem statement and assumptions, we will generate regression model to predict the number of dengue cases.

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

