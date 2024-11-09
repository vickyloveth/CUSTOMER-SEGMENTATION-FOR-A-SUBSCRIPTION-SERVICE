# CUSTOMER-SEGMENTATION-FOR-A-SUBSCRIPTION-SERVICE

## Table of Content

- Overview
- Dataset
- Tools used
- Analysis and findings
- Insights and Recommendation

  
### OVERVIEW
This project involves analyzing customer data for a subscription service to identify segments and trends.

### DATASET
The dataset contains;
1. Orderid(a unique identifier)
2. Product (product name)
3. Region (geographic region)
4. Orderdate (date of order)
5. Quantity (number of units sold)
6. Unitprice (price per unit)
7. Total revenue (Total revenue per order)

### TOOLS USED
- Microsoft excel
- SQL
- Powerbi for visualization.


### ANALYSIS AND FINDINGS

#### Excel analysis

Excel files containing the  followng;
- Data filtering ans sorting which involves cleaning up the data set and removing duplicates.

  ![Screenshot (39)](https://github.com/user-attachments/assets/da1915ec-8328-4682-8899-012e5f4da868)

Above is the dataset for customer subscription services, and to be able to analyze properly, we source for the duration in which each customers subscribed; hence our subscription duration column



- Pivot tables for regional and products analysis

![Screenshot (40)](https://github.com/user-attachments/assets/59e341cf-6e77-462f-8beb-56de9a038d31)

  
#### SQL analysis

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



#### Power BI Dashboard

Power BI dashboard containing:
- Total number of customers, Total revenue and avarage subscription duration (cards)
- Top selling products by customers (Donut chart)
- Top selling products by revenue (Line chart)
- Subscription type by number of customer in each Region(Matrix)
- Top customer by thier Revenue (Table)
- Number of Customers with Active and cancelled subscription(matrix)
- Monthly sales trend of customers patronage (line chart)
- Count of customer by cancelled subscription (Pie chart)

![Screenshot (44)](https://github.com/user-attachments/assets/7a38c099-5072-4674-b2e8-80f338ff7fcd)


![Screenshot (45)](https://github.com/user-attachments/assets/209ec9da-1d0c-4c03-9db3-0167118d2c77)



#### Key Findings

1. Total Subscriptions: 33,787
2. Distinct Customers: 20
3. Total Revenue: $68M
4. Average Subscription Duration: 12 months
5. Regional Revenue Leaders: East ($16,958), South ($16,899)

Subscription Patterns

1. Basic: 50.08% (most popular)
2. Premium: 25%
3. Standard: 24.92%

Regional Subscription Trends

1. East: Basic (highest)
2. South: Premium (highest)
3. West: Standard (highest)
4. North: Basic (highest)

Quarterly Subscription Trend

1. Steady Growth: Jan-September (avg. 3,385)
2. Decline: Last quarter (<2,000)

Customers with cancelled subscription in each region

1. East: No customer cancelled and we have 8488 active subscribers.
2. North: 5067 customers cancelled thier subscription leaving 3366 active subscribers
3. South: 5064 customers cancelled thier subcription while 3382 are active.
4. west: 5044 customers cancelled while 3376 remain active.

Our subscription analysis reveals a retention rate of 55.09% and a cancellation rate of 44.91%.


### INSIGHTS AND RECOMMENDATION

INSIGHTS

1. High Churn Rate: 44.91% cancellation rate indicates potential issues with customer satisfaction, pricing, or competition.
2. Regional Variations: East and South regions drive revenue, while West and North underperform though not with much difference.
3. Basic Subscription Dominance: 50.08% preference for basic subscriptions suggests potential for upselling/cross-selling.
4. Quarterly Decline: Last quarter's drop (<2,000 subscriptions) warrants investigation.

Recommendations

1. Improve Customer Retention: Enhance customer support, offer incentives, and solicit feedback.
2. Upselling/Cross-Selling: Develop strategies to upgrade basic subscribers to premium/standard.
3. Regional Marketing: Tailor marketing efforts to underperforming regions (West/North).
4. Competitor Analysis: Investigate competitors' offerings, pricing, and strategies.
5. Pricing Review: Assess pricing elasticity, considering basic subscription dominance.
6. Quarterly Performance Monitoring: Regularly analyze subscription trends.
7. Enhance Premium/Standard Benefits: Differentiate offerings to justify premium pricing.
8. Loyalty Programs: Implement rewards for long-term subscribers.






  
    
