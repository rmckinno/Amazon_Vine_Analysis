<img src=images/df.png align=right height=400 width=500 >
<img src=images/vine_df.png align=right height=400 width=500 ><br></br>
<img src=images/filter_total_votes.png align=right height=400 width=500 >
<img src=images/clean_vine_filtered.png align=right height=400 width=500 >
<img src=images/Vine_vs_nonVine.png align=right height=400 width=1000 > <br></br>
<img src=images/calculations.png align=right height=400 width=500 >
<img src=images/print.png align=right height=400 width=500 >

# Amazon_Vine_Analysis
Extracting a large dataset from AWS to transform and perform analysis 

## Overview of the analysis 
The luggage reviews dataset from Amazon Review datasets is extracted from AWS and transformed using PySPark in Google's CoLab. Multiple dataframes are created. The vine_table DataFrame is used to determine if there is any bias between the reviews that are part of the Vine program versus reviews received that are not from the Vine program. Amazon Vine is a product review program. A small fee to Amazon allows companies to provide trusted reviewers with their product and those customers must provide a review. The images to right contains all code for extracting, filtering, and performing calculations on the luggage dataset.

## Tools
- Spark
- PySpark
- Google Colab Notebook
- AWS (RDS, S3)

## Results
The luggage dataset was read into a dataframe using pyspark. Multiple filters were applied to give a clean, usable dataset for analysis. Rows were filtered by total_votes of 20 or more and where the number of helpful_votes divided by total_votes was equal to or greater than 50%. Once the luggage data set was filtered the reviews were split into those from the Vine program and those that were not part of the Vine program. Using these dataframes the analysis resulted in:

- A total number of 6711 reviews.
- There were 21 Vine reviews and 6690 non-Vine reviews.
- There were 3458 5-star reviews from the filtered dataset:
    - 10 5-star Vine reviews
    - 3448 5-star non-Vine reviews
- 0.29% of 5-star reviews were from the Vine program.
- 99.71% of 5-star reviews were not from the Vine Program.
- Overall, 5-star Vine reviews accounted for 0.15% of all reviews in the filtered luggage dataset, while 5-star non-Vine reviews accounted for 51.38% of all reviews.

## Summary
Bias reviews appear to be unsupported according to the results. Non-Vine reviews account for far more 5-star reviews than those from the Vine program. Only 21 vine reviews were included in this set and 10 of those resulted in 5-star reviews resulting in 47.62% 5-2tar reviews. For non-Vine reviews, about 51.62% resulted in 5-stars. Again, this does not support a bias review argument.
