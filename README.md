# Amazon Vine Analysis

## Overview
This project analyzes Amazon Vine reviews data, a program that companies can use to obtain reviews for their products by Amazon Vine members. Some members are paid for their review, but the majority of reviews are unpaid. The purpose of this analysis is to determine if there is a bias toward favorable reviews when the member is paid. 

#### Resources
* Dataset: [Amazon Reviews US Outdoors Products](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Outdoors_v1_00.tsv.gz) 
* AWS, PostgreSQL, Google Colab Notebook

## Analysis
#### Filter the Dataset
The data was first filtered to include only products with greater than or equal to 20 total votes and a proportion of helpful votes to total votes of greater than or equal to .5. 

#### Determine the Presence of Positivity Bias
Next, the total number of paid versus unpaid reviews as well as the total number of paid 5-star reviews versus unpaid 5-star reviews was found. The proportion of five star reviews to total reviews for each payment category was then compared to determine bias.

## Results
#### Reviews by Payment Category
In total, there were 39,976 reviews for outdoor products that fit the filter criteria.
* Paid: 107 reviews
* Unpaid: 39,869 reviews
![Total Reviews](/images/Total_Reviews.png)

#### Five-Star Reviews by Payment Category
Of the 39,976 reviews, 21,061 were five-star reviews.
* Paid: 56
* Unpaid: 21,005
![5 Star Reviews](/images/5star_reviews.png)

#### Percentage of 5-Star Reviews by Payment Category
Of the total number of reviews, 52.68% (21,061/39,976) were 5-star reviews.
* Paid: 52.34%
* Unpaid: 52.69%
![Percent 5 Star](/images/Percentage_5star.png)

## Summary
This analysis shows that there is not positivity bias in the Amazon Vine program for reviews of outdoor products. Paid and unpaid reviewers gave essentially the same percentage of 5-star reviews, 52.34% and 52.69%, respectively. 

#### Supporting Analysis
To support these conclusions, expanding the analysis to include 3- and 4-star reviews would inform if positivity bias occurs at other rating levels. Other measures such as mean rating, median, and mode could also show differences between paid and unpaid reviewers. Finally, while outdoor products don't show positivity bias towards 5-star ratings, other product categories may be different. To draw conclusions about the Amazon Vine program as a whole, data across all product categories should be aggregated and analyzed.
