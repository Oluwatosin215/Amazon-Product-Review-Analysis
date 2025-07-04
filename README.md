#### Project Topic: Amazon-Product-Review-Analysis

## Project Overview: 
This is an Excel project analyzing Amazon Product Reviews to extract business insights ,It is to help sellers understand product performance ,pricing and customer feedback.

## Data source:
The dataset was provided as part of a data analytics project scenario.  
It contains product and review information scraped from Amazon product pages, including:
- Product details (name, category, price, discount, rating)
- Customer review data (titles, content, review count)
- Total of 1,465 unique products
- Data shared in `.xlsx` format
  
## Tools Used: 
- Microsoft Excel [Download Here](https://www.microsoft.com)
   - Pivot Tables
   - Calculated Columns
   - Dashboard
- Power Query (for cleaning)
- Manual business logic
  
##  Key Questions Answered
- What is the average discount percentage by product category?
-  How many products are listed under each category?
-  What is the total number of reviews per category?
-  Which products have the highest average ratings?
-  What is the average actual price vs the discounted price by category?
-  Which products have the highest number of reviews?
-  How many products have a discount of 50% or more?
-  What is the distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)?
-  What is the total potential revenue (actual_price × rating_count) by category?
-  What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)?
-  How does the rating relate to the level of discount?
-  How many products have fewer than 1,000 reviews?
-  Which categories have products with the highest discounts?
-  Identify the top 5 products in terms of rating and number of reviews combined.
  
## Deliverables
- Excel dashboard
- Pivot tables
- Summary insights

## Data Analysis
This is where i include some basic lines of Dax expressions used during this analysis
Excel dax expression for task 7
=IF(G2 >= 0.5, "Yes", "No")
=COUNTIF(H2:H1466, "Yes")
,Excel dax expression for task 9
=[@[actual_price]] * [@[rating_count]]
=F2 * H2
,Excel dax expression for task 10
=IF([@[actual_price]]<200, "<₹200", IF([@[actual_price]]<=500, "₹200–₹500", ">₹500"))
=IF(F2<200, "<₹200", IF(F2<=500, "₹200–₹500", ">₹500"))
,Excel dax expression for task 11
=CORREL(discount_range, rating_range)
=CORREL(G2:G1466, H2:H1466)
 Interpretation of task 11
* +1 = Strong positive correlation (as discount goes up, rating goes up)
* -1 = Strong negative correlation
* 0 = No correlation
,Excel dax expression for task 12
=IF([@[rating_count]] < 1000, "Yes", "No")
=IF(H2 < 1000, "Yes", "No")
=COUNTIF(I2:I1466, "Yes")

## Project Report

You can download or view the full project report here:

[Amazon case study.xlsx](https://github.com/user-attachments/files/21054751/Amazon.case.study.xlsx)
