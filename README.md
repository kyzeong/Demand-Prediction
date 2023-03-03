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

First we did exploratory data analysis to the past sales history in order to pinpoint the best product for our initial modeling. The best product is defined by the top sales quantity and also order frequency. In this case, Product 1359 is the best product which meets bost the requirement of our best product criteria. Once we have defined the best product, we resample the data to weekly sales.

We tried to predict with 2 different algorithms, time series and neural network. In time series, there are ARIMA and SARIMAX. SARIMAX with exogenous feature work the best in terms of lowest RMSE, followed by SARIMAX without exogenous feature and lastly ARIMA model. After trying time series, I have also tried LSTM model. Although the RMSE is slightly higher than SARIMAX with exogenous feature, it is selected as the final model because it does not require exogenous feature and can predict sales of individual product independantly.

Lastly, the fine tuned LSTM model is used to predict the following 4 weeks sales of each and every product.

---

### Conclusion

The model is successfully implemented and it is able to predict the following 4 weeks sales for all products.

---

### Recommendation

An application or a dashboard can be included for further enhancement for a more user friendly interface which allows non-technical personnel to be able to generate predictions.

---

### Document Flow

All the coding are stored in the "Code" folder. Under the #Code# folder:
1. First file is EDA
2. Second file is baseline model and time series model
3. Thrid file is LSTM model
4. Fourth file is the final model and implementation

Under the #Data_Historical# file:
1. Historical Product Demand - the raw historical data file which we based our model on
2. Final_Predictions - the following 4 weeks demand prediction
