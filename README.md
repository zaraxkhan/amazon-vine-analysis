# Amazon-Vine-Analysis
In this analysis, I will be using PGAdmin, PySpark, and AWS to analyze some Amazon Furniture review dataset.

## Overview
For this analysis, I will be using Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.I’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. I will need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I’ll use PySpark to determine if there is any bias toward favorable reviews from Vine members in the chosen dataset. Then, I will write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.

First, I will create an AWS RDS database with tables in pgAdmin, pick a dataset from the Amazon Review datasets and extract the dataset into a DataFrame. I'll transform the DataFrame into four separate DataFrames that match the table schema in pgAdmin. Then, upload the transformed data into the appropriate tables and run queries in pgAdmin to confirm that the data has been uploaded.

Next, I will determine if there is any bias towards reviews that were written as part of the Vine program. For this analysis, I'll determine if having a paid Vine review makes a difference in the percentage of 5-star reviews.

## Results
- How many Vine reviews and non-Vine reviews were there?

There were 136 Vine reviews and 18019 non-Vine reviews for the furniture review dataset.
#### Paid Reviews vs Unpaid Reviews
![Screen Shot 2022-09-21 at 7 30 18 PM](https://user-images.githubusercontent.com/105755095/191633161-e0814bc7-2247-40b6-ad48-ba4024acea1f.png)
![Screen Shot 2022-09-21 at 7 30 32 PM](https://user-images.githubusercontent.com/105755095/191633165-709c459b-c0c6-4b1b-be20-12075d279de6.png)

- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

From the five star reviews, there were 74 reviews that were paid and 8,482 reviews that were unpaid, or non_vine reviews.
#### Paid 5-Star Reviews vs Unpaid 5-Star Reviews
![Screen Shot 2022-09-21 at 7 32 37 PM](https://user-images.githubusercontent.com/105755095/191633256-0e2b4bfb-1120-44d7-a79b-1e6968437413.png)
![Screen Shot 2022-09-21 at 7 32 44 PM](https://user-images.githubusercontent.com/105755095/191633266-2ee40dcc-9390-420c-9ce1-92840fec976d.png)

- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

In this dataset, about 54% of 5 stars came from Vine reviewers and around 47% of the 5 star reviews were from unpaid buyers.

#### Paid 5-Star Review Percentage vs. Unpaid 5-Star Review Percentage
![Screen Shot 2022-09-21 at 7 34 04 PM](https://user-images.githubusercontent.com/105755095/191633474-0a7aa214-e801-4c3e-9334-1df2554adebd.png)
![Screen Shot 2022-09-21 at 7 34 12 PM](https://user-images.githubusercontent.com/105755095/191633486-a5e64a44-8498-4ee8-b4be-8ba8dc9bc0c7.png)


## Summary
In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
making sure that it was a verified purchase
