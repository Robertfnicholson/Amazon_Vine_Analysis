# Amazon Vine Analysis Challenge

## Overview of the Analysis
In this challenge, I analyzed the Amazon Tools Review dataset. This involved using PySpark to perform the ETL process to 
extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. It 
then involved using PySpark to determine if there was any bias toward favorable reviews from Vine members in your dataset. </p>

## Results
The challenge instructions directed me to first filter the Vine_table to only those reviews that received at least 20 
votes and those reviewed that had a “helpful_vote” to “total_votes” equal to or greater than 50% in order to pick reviews 
that are more likely to be helpful and to avoid having division by zero errors later in the analysis. I created a dataframe 
called Helpful_votes_50_df” to hold these results. See “Helpful_votes_50_df” image below.</p>

![Helpful_votes_50_df.png]( https://github.com/Robertfnicholson/Amazon_Vine_Analysis/blob/2eb57f4d849261ec1d1230b900a5a473eece991d/Helpful_votes_50_df.png)

•	There were 4,825 total reviews in the “Helpful_votes_50_df.” 
•	Of those, 109 or 2.3% were paid Vine reviews and 4,716 or 97.7% were non-Vine reviews.
•	There were 2,288 total five-star reviews.
•	Of those 65 or 2.8% were paid Vine reviews and 2,223 or 97.2% were non-Vine reviews.</p>

## Summary
A slight positivity bias may exist for the reviews in the Vine program since the percentage of Vine five-star ratings, 2.8%, 
is slightly higher than the total percentage of Vine ratings, 2.3%  I would recommend performing a one sample t-test to 
determine if the percentage of Vine five-star rating is statistically different of the population percentage of Vine ratings. 
</p>
