# Amazon_Vine_Analysis

## Purpose/Overview
Using PySpark to perform ETL on 1 of 50 provided datasets to analyze Amazon reviews written by members of the paid Amazon Vine program, and provide results to SellBy.
Connecting to an AWS RDS instance and loading data into PgAdmin, then determining if there is a bias toward favorable reviews in selected dataset, and providing an additional item to support findings.


## Analysis and Results

1-How many Vine reviews and non-Vine reviews were there?
The dataset appears a little on the small side for Big Data with 145,431 reviews. Only reviews with 20 or more votes where considered for the rest of the analysis leaving 3,342 reviews. Helpful votes were defined as being 50% or greater than the total votes narrowing the list to 1,685 reviews.
Unfortunately, due to the applied criteria, it significantly diminished the sample size. In the remainder 1,685 reviews, there were no reviews that were paid for by the Vine program.
All 1,656 remaining reviews are unpaid Vine with 0 paid Vine.

2A- How many Vine reviews were 5 stars?
As for 5-star unpaid Vine reviews, there were 631 reviews. Attempting to divide by zero, the code would result in a zero division error. 

2B-How many non_VIne reviews were 5 stars?
There are also 0 paid Vine with 5-star reviews.

3A- What percentage of Vine reviews were 5 stars? 
The percentage of 5-star Vine reviews resulted in 37.4%.

3B- What percentage of non-Vine reviews were 5 stars? 
Zero %

## Summary
Because the sample size was constricted to a degree that it was impossible to compare paid and unpaid Vine reviews, the analysis is biased towards unpaid Vine reviews. 
Another indicator is comparing 37% of unpaid, 5-star Vine reviews to 0% paid, 5-star Vine reviews also shows that the unpaid Vine are biased as well.

The starting criteria of 20 likes or the 50% helpful criteria may have been too high, which made the data set too small. Adjustments to these criteria is a first step to reconsidering using this data set.
