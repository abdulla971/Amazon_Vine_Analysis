# Amazon_Vine_Analysis
ETL and Sentiment Analysis of Amazon reviews with AWS, PySpark, postgresql, NLP.

## Analysis Overview
In this project an analysis is performed on Amaozon Vine program to check if there exist a bias toward favorable reviews from Vine memebers. In order to complete the analysis PySpark is used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, load the transformed data into pgAdmin and calculate different metrics. It is noted that we focused on the US reviews for video games.

## Resources
- Data Source: [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), [Video Games Review dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz)
- Software: Google Colab Notebook, PostgreSQL 11.9, pgAdmin 4, AWS

## Results
A paid and unpaid DataFrame is created, after the data is cleaned and sorted. The first 20 rows of each is shown below:

![Paid Dataframe](Resources/paid_df.png)

Paid DataFrame

![Unpaid DataFrame](Resources/unpaid_df.png)

Unpaid DataFrame

A count of each DataFrame yielded 90 paid (Vine) reviews and 37,831 unpaid reviews.

![Paid and Unpaid Review Count](Resources/paid_unpaid_reviews.png)

The number of 5 Star reviews was calculated for each, 44 5 Star paid reviews and 14704 5 Star unpaid reviews.
![Five Star Reviews](Resources/each_review_count.png)

And the percentage of 5 Star reviews was 48.89% for paid and 38.87% for unpaid.
![Five Star Review Percentage](Resources/percent_reviews.png)

## Summary
The conclusions that can be obtained from the dataset include: there apears to be some form of bias for posisitve paid reviews, with a 10% higher for paid versus unpaid reviews. It is well noted that there is 90 paid reviews, compared to the much higher 37,000 unpaid. To put it into persepctive there is one piad review for each 420 unpaid ones; therefore seeking a larger paid sample set may be better for the analhysis.

To further improve our analysis we might be intrested in stdying another category of reviews other than video games such as electronics to help mitigate numerical differences.
