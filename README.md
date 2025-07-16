



<img width="250" height="200" alt="amazon" src="https://github.com/user-attachments/assets/face6b97-e62d-4c16-a8c9-d8da602c836b" />

# Project Topic: Amazon-Product-Review-Analysis


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
,  Excel dax expression for task 9
=[@[actual_price]] * [@[rating_count]]
=F2 * H2
, Excel dax expression for task 10
=IF([@[actual_price]]<200, "<₹200", IF([@[actual_price]]<=500, "₹200–₹500", ">₹500"))
=IF(F2<200, "<₹200", IF(F2<=500, "₹200–₹500", ">₹500"))
, Excel dax expression for task 11
=CORREL(discount_range, rating_range)
=CORREL(G2:G1466, H2:H1466)
 Interpretation of task 11
* +1 = Strong positive correlation (as discount goes up, rating goes up)
* -1 = Strong negative correlation
* 0 = No correlation
, Excel dax expression for task 12
=IF([@[rating_count]] < 1000, "Yes", "No")
=IF(H2 < 1000, "Yes", "No")
=COUNTIF(I2:I1466, "Yes")

## Key Insights
- Most Discounted Category: Mobile Accessories had the highest average discount percentage across all categories.
- Product Volume: Electronics had the highest number of product listings, indicating a highly competitive category.
- Most Engaging Category: Home Appliances received the greatest number of customer reviews, showing high user engagement.
- Top-Rated Products: Several products achieved ratings of 4.8 and above, reflecting strong customer satisfaction.
- Heavy Discounts: Over 800 products had discounts of 50% or more, suggesting a widespread use of price reductions to attract buyers.
- Revenue Opportunity: Office Supplies and Electronics showed the highest potential revenue when multiplying actual price by the number of reviews.
- Low-Visibility Products: More than 300 products had fewer than 1,000 reviews, indicating potential underperformance or limited customer awareness.
- Price Distribution: The majority of products fell into the ₹200–₹500 price range, suggesting a focus on affordable mid-range pricing.
- Rating vs Discount Relationship: A slight negative correlation (-0.16) was observed between discount percentage and product rating, meaning deeper discounts do not necessarily improve customer satisfaction.
- Top Performing Products: The best-performing products were those that combined high ratings with a large number of reviews, making them standout items in both quality and popularity.

## Project Report

You can download or view the full project report here: [Amazon.case.study.xlsx](https://github.com/user-attachments/files/21267125/Amazon.case.study.xlsx)
