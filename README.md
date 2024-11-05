# CUSTOMER-SEGMENTATION-FOR-A-SUBSCRIPTION-SERVICE

## OVERVIEW
This project involves analyzing customer data for a subscription service to identify segments and trends.

 ## DATASET
The dataset contains;
1. Orderid(a unique identifier)
2. Product (product name)
3. Region (geographic region)
4. Orderdate (date of order)
5. Quantity (number of units sold)
6. Unitprice (price per unit)
7. Total revenue (Total revenue per order)

## TOOLS USED
- Microsoft excel
- SQL
- Powerbi for visualization.

## ANALYSIS

### Excel analysis

Excel files containing the  followng;
- Data filtering ans sorting which involves cleaning up the data set and removing duplicates.

  ![Screenshot (39)](https://github.com/user-attachments/assets/da1915ec-8328-4682-8899-012e5f4da868)

Above is the dataset for customer subscription services, and to be able to analyze properly, we source for the duration in which each customers subscribed; hence our subscription duration column



- Pivot tables for regional and products analysis

![Screenshot (40)](https://github.com/user-attachments/assets/59e341cf-6e77-462f-8beb-56de9a038d31)

  
### SQL analysis

The SqL files contains the Queries for data extraction and filtering on excel. it aslo contains the Aggregate funtions for revenue and quantity calculation.
It also help to know customers preference in each product.

#### Key queries

--------TOTAL NUMBER OF CUSTOMER PER REGION----------


```
select region, COUNT(*) as 'NO OF CUSTOMER'
from [dbo].[CUSTOMER DATA]
group by region
```


 
--------FIND THE MOST POPULAR SUBSCRIPTION TYPE BY THE NUMBER OF CUSTOMERS------

```
 SELECT 
     SUBSCRIPTIONTYPE,
COUNT 
     (CUSTOMERID) AS NO_OF_CUSTOMERS
FROM 
      [dbo].[CUSTOMER DATA]
GROUP BY
      SubscriptionType
ORDER BY 
     NO_OF_CUSTOMERS DESC;
```


![Screenshot (41)](https://github.com/user-attachments/assets/99e2abae-0040-4b64-9b04-0350a9d7f0ad)

![Screenshot (42)](https://github.com/user-attachments/assets/1b9172e5-7d50-49b0-b15c-1c1c0decb67d)

![Screenshot (43)](https://github.com/user-attachments/assets/0f89842b-cbdd-414b-bb23-70bc4a4a40e9)



### Power BI Dashboard

Power BI dashboard containing:
    
