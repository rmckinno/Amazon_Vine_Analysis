# Amazon_Vine_Analysis
Taking a large dataset through the ETL process and performing analysis 

# Overview of the analysis 
The luggage reviews dataset from Amazon Review datasets is extracted from AWS and transformed using PySPark in Google's CoLab. Multiple dataframes are created and uploaded into pgAdmin. Afterwards, the vine_table DataFrame is used to determine if there is any bias between the reviews that are part of the Vine program versus reviews received that are not from the Vine program. Amazon Vine is a product review program. A small fee to Amazon allows companies to provide trusted reviewers with their product and those customers must provide a review.

# Tools
- Spark
- PySpark
- Google Colab Notebook
- AWS (RDS, S3)
- pgAdmin

# Results
<img src=images/luggage.jpg align=right>
The luggage dataset was read into a dataframe using pyspark. Multiple filters were applied to give a clean, usable dataset for analysis. Rows were filtered by total_votes of 20 or more and where the number of helpful_votes divided by total_votes was equal to or greater than 50%. Once the luggage data set was filtered the reviews were split into those from the Vine program and those that were not part of the Vine program. Using these dataframes the analysis resulted in:

- A total number of 6711 reviews.
- There were 21 Vine reviews and 6690 non-Vine reviews.
- There were 3458 5-star reviews from the filtered dataset:
    - 10 5-star Vine reviews
    - 3448 5-star non-Vine reviews
- 0.29% of 5-star reviews were from the Vine program.
- 99.71% of 5-star reviews were not from the Vine Program.
- Overall, 5-star Vine reviews accounted for 0.15% of all reviews in the filtered luggage dataset, while 5-star non-Vine reviews accounted for 51.38% of all reviews.


  
