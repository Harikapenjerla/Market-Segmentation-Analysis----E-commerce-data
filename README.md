# Market-Segmentation-Analysis for E-commerce data

Brazilian E-commerce real data of orders at Olist store. Dataset consist of 100000 orders from 2016 to 2018. The dataset has many variables like order status, price, payment method, customer location, reviews from customers, product attributes and geolocation (latitude/longitude). 
Note:
1.	An order might have multiple items.
2.	Each item might be fulfilled by a distinct seller.
3.	All text identifying stores and partners where replaced by the names of Game of Thrones great houses.

## Data Schema:
 
![image](https://user-images.githubusercontent.com/54416525/89240188-62be4180-d5c9-11ea-9fc1-aa3802e475b7.png)

## Time Series Forecasting:
An autoregressive (AR) model predicts future behavior based on past behavior. It is used for forecasting when there is some correlation between values in a time series and the values that precede and succeed them. You only use past data to model the behavior, hence the name autoregressive. The process is basically linear regression of the data in the current series against one or more past values in the same series. 
An AR(p) model is an autoregressive model where specific lagged values of yt are used as predictor variables. Lags are where results from one time period affect following periods. 
The value for “p” is called the order. For example, an AR would be a “first order autoregressive process.” The outcome variable in a first order AR process at some point in time t is related only to time periods that are one period apart (i.e. the value of the variable at t – 1). A second or third order AR process would be related to data two or three periods apart. 
The AR(p) model is defined by the equation: <br />
yt = δ + φ1yt-1 + φ2yt-2 + … + φpyt-1 + At <br />
Where: <br />
•	• yt-1, yt-2…yt-p are the past series values (lags), <br />
•	• At is white noise (i.e. randomness), <br />
•	• and δ is defined by the following equation: <br />
Where μ is mean.<br />
The final model forecasted plot with the prediction values of next 30 days. We restricted our predictions to 30 days since the sales are highly dynamic and we should be very cautions while predicting for longer time periods.

![image](https://user-images.githubusercontent.com/54416525/89240299-ba5cad00-d5c9-11ea-8e8b-7a23a2d0c892.png)
 
## Customer Segmentation using RFM values and K-means:
Customer segmentation is used in marketing to better understand customer behavior of the business. The most common types of customer segmentation are 
Demographic Segmentation 
Geographic Segmentation 
Behavioral Segmentation 
Lifecycle Based Segmentation 
Segmentation used for this analysis was based on the purchase behavior of the customers based on features like recency, frequency, monetary values which is commonly known as RFM. 
Recency: Number of days the user has been inactive, from the moment of last purchase to the latest time in t2he dataset. 
Frequency: Total number of transactions completed by a customer. 
Monetary: Total revenue generated by the customer.
K-means model gives the following four clusters 
 
![image](https://user-images.githubusercontent.com/54416525/89240360-e2e4a700-d5c9-11ea-9c4a-9a545ed773c3.png)

From above k-means clustering analysis with 4 clusters. 
Cluster1: Customers who spend more “Big Spenders” Cluster. <br />
Cluster3: Customers who spend recently.” Most Recent” Cluster.<br />
Cluster4: Customers who spend frequently. “Loyal Customers” Cluster. <br />
Cluster2: Customers who are Inactive, lost etc. “Others” Cluster.<br />


## Geolocation & Customer Segmentation Dashboard:
Created dashboards using tableau below is the screenshot of dashboard. <br />
![image](https://user-images.githubusercontent.com/54416525/89240408-00197580-d5ca-11ea-9110-5ab393c243c4.png) <br />

![image](https://user-images.githubusercontent.com/54416525/89240421-0576c000-d5ca-11ea-9d05-00e2282766c4.png) <br />


## Insights and Conclusion:
The main contribution of this two-stage modelling plus Dashboard building to current scholarly discourse is that it provides a more data-driven approach in generating the business strategies for stakeholders. This methodology can be readily applied to other customer segmentation and other Quantitative Marketing Analysis. Because the clustering process consists only of unsupervised learning techniques, some clusters may have no economic explanations, hence resulting in less significance when regressed against the data.<br /> 
• By using customer segmentation analysis, we can mainly focus on the special offers/promotions to increase loyalty among customers. Also select best communication channel for each group of customers and improve marketing strategies. For example, the product promotion can prioritize based on the recency, other customers segments who is likely to make purchases. Loyal customers need more attention in this business so by providing more promotions/offers can be a useful strategy. <br />
• Credit cards is the most used Payment type by the customers so to improve customer satisfaction by offering credit card rewards points. Sales forecasting for the next 30 days seems to be around 130 million dollars which is less than last two months. So, it necessary improve customer online experience and product categories. <br />
• Time series prediction results shows that the next 15 days, the sales could potentially hit low. This could assist organization officials in taking a better decision. 
• The dashboard assists with the visual interpretation on various aspects of the data like customer segmentations, product segmentations and geo location analysis. <br />
 

## References:
https://www.kaggle.com/olistbr/brazilian-ecommerce <br />
http://en.wikipedia.org/wiki/RFM_(market_research) <br />
https://towardsdatascience.com/understanding-k-means-clustering-in-machine-learning-6a6e67336aa1 <br />
https://machinelearningmastery.com/autoregression-models-time-series-forecasting-python/ <br />
https://www.tableau.com/learn/tutorials/on-demand/dashboard-interactivity-using-actions <br />
https://machinelearningmastery.com/how-to-use-correlation-to-understand-the-relationship-between-variables/ <br />
https://www.business2community.com/customer-experience/4-types-of-customer-segmentation-all-marketers-should-know-02120397 <br />
https://help.tableau.com/current/guides/get-started-tutorial/en-us/get-started-tutorial-build.html <br />
https://www.tableau.com/solutions/marketing-analytics <br />


## Note:
Time series forecasting is done in python, filename as TimeSeries Forecasting.ipynb and TimeSeries Forecasting.html <br />
Customer Segmentation Using RFM values and K-Means is done in R, filename as Clustering.R and Clustering.html <br />
Dashboards in tableau, filename as Clustering.twb, Geospatial Analysis.twbx.

Please let me know any suggestions.TIA.

