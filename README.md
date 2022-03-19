# Amazon_Vine_Analysis

## Overview of Project
Analysing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products.

Using PySpark to perform ETL on a dataset of roughly 570,000 reviews of items in the "Lawn & Garden" catergory of Amazon. Filter the data set into useful Vine and Non-Vine reviews. 

### Purpose
 Determine if there is any bias toward favorable reviews from Vine members in the dataset.

## Analysis
I used PySpark to perform my analysis and pulled the dataset from a S3 Bucket I set up on my Amazon AWS account. 

To improve the reliablity of the data set I removed all reviewers that had less than 20 reviews. To futher improve the data I removed any reviewers that provided more unhelpful votes than not. 

At that point I split the data into the vine [paid_reviews] and non-vine [unpaid_reviews] reviews and gathered the results. 

## Results
* ### Total number of Vine Reviews = 452

![Total Vine Reviews](/vine_total.png) 

* ### Total number of non-Vine Reviews = 570,181

![Total Non-Vine Reviews](/nonvine_total.png) 

* ### Total 5-Star Vine Reviews = 210

![Total 5-Star Vine Reviews](/vine_5_star.png)

* ### Total 5-Star non-Vine Reivews = 291,254

![Total 5-Star Non-Vine Reivews](/nonvine_5_star.png)

* ### Percentage of Vine reviews that were 5 stars = 46.46%

![Percentage of 5-Star Vine Reviews](/vine_5_star_percent.png) 

* ### Percentage of non-Vine reviews that were 5 stars = 51.08%

![Percentage of 5-Star Non-Vine Reviews](/nonvine_5_star_percent.png) 

## Summary
These results show that there is no positivity bias for reviews in the Vine program. The percentage of 5-star reviews is slightly below those outside the Vine program, and we would expect the opposite if there was a positive bias. 


## Author
> Chris Newell 03/19/2022
