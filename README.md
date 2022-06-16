# Amazon_Vine_Analysis

Analyzing Amazon reviews written by members of the paid Amazon Vine program through spark

## Overview of Analysis
The purpose of this analysis is to look into amazon reviews to determine if there is bias for those in the Amazon Vine Review program. I chose to analyze jewelry reviews.

## Results 
  The dataset was first loaded into a google colab notebook and then put into a dataframe using spark. From there the data was uploaded to a database using Amazon AWS and imported into Postgres.
  
  ![vine_pg](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/vine_pg.png)
  ![customers_pg](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/customers_pg.png)
  ![products_pg](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/products_pg.png)
  ![review_pg](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/review_pg.png)
 
 After uploading the database to postgres, further analysis was conducted to look deeper into 5-star reviews.
 
 Dataframe for reviews in Amazon Vine Program:
  ![paid_vine](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/paid_vine.png)
  
 Dataframe for reviews not in Amazon Vine Program:
 ![unpaid_vine](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/unpaid_vine.png)
 
 Total reviews for vine and non-vine reviews:
 
 ![total_paid](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/total_vine.png)
 ![total_unpaid](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/total_unpaid.png)
 
 - We can see that the majority of reviews are not associated with the Amazon Vine Program. 1763580 for unpaid versus 3814 for paid reviews.
 
 Total 5-star reviews for vine and non-vine reviews:
 
 ![5_star_paid](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/vine_5_star.png)
 ![5-star_unpaid](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/unpaid_5_star.png)
 
 - The number of 5 star reviews for non-vine associated reviews is much higher than those associated with the Amazon Vine Program
 
![totals](https://github.com/JTGonzaga/Amazon_Vine_Analysis/blob/main/Analysis/total_values.png)
- The total amount of reviews is 1,767,349
- The amount of 5-star reviews is 1,081,244
- The percentage of 5-star vine reviews is well under 1% at 0.09%
- The percentage of unpaid vine reviews is just over 61%

## Summary

From the results gathered from this dataset, I do not think there is any positivity bias for the reviews in the Amazon Vine Program. The large difference in 5-star review percentage for paid and unpaid reviews, 0.09% and 61% respectively, show the opposite. I don't think this is due to a lack of data considering that over a million reviews were included in the dataset. In my opinion, this makes sense. I theorize that reviewers that are getting paid to review want to be more critical and analytical. This can be a positive thing because it can lead to more honest reviews of items. A way to further analyze this would be to find the standard deviations of paid versus unpaid reviews.
