# BigData_BigMarket


## Objectives

- Perform ETL on one of the review datasets
- Store your results on an AWS RDS database
- Determine if reviews are biased using PySpark or SQL with the appropriate statistical methods

## Technologies

- AWS account
    -  Rational DataBase Servive (PostgreSQL engine version 12.3)

 - Google Colaboratory Notebook
    - PySpark (version 3.0.1)

- pgAdmin (version 4.21)

## Resources
- SQL schema: cf. *schema.sql* file under [Challenge](/Challenge) folder
- Dataset: Cameras reviews (https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Camera_v1_00.tsv.gz
) choose (additonal info on dataset: https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)
- Google Colaboratory Notebook: https://colab.research.google.com/drive/1FZv33RkxwfoAixncdUHtlqvp3-VB79H4?usp=sharing


## Results
> Results are also available in the last cell of the Google Colaboratory Notebook

> **NB**: as mentioned in the Notebook, only reviews linked to verified purchases were selected to avoid fake reviews


|Type of review|Number of reviews|Number of 5-star reviews|Average Rating|Number of helpful votes|Average number of helpful votes per review|Ratio of 5-star reviews|
|--------------|-----------------|------------------------|--------------|-----------------------|------------------------------------------|-----------------------|
|Vine|23|13|4.48|784|34.0|0.57|
|Non-Vine|1494378|904347|4.18|2877663|2.0|0.61|


Our dataset (on Camera reviews) contained very few Vine reviews (23 over 1,494,401 total reviews).

Vine reviews have an average rating above the others (4.48 vs. 4.18 | + about 7%) but have a less important ratio of 5-stars ratings: about 57% of Vine reviews ended with the maximum notation whereas other reviews gave in 61% of the case a 5-star review.

In addition, Vine reviews received in average 34 helpful votes while non-paid reviews were voted in with only about 2 votes.

**These two points tend to lead than cameras Vine reviews posted on Amazon seem fair and helpful. On the other hand, our very little Vine reviews population should incite us to be cautious about this assertion.**
