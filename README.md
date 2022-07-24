# Amazon Vine Analysis

## Overview

In this project, our purpose is to examine Amazon customer reviews. In other words, We analyze Amazon reviews from the paid service Amazon Vine, which allows growers and manufacturers to receive reviews of their products after the vine members try their products.

Some companies, such as SellBy, pay a price to Amazon Vine in order to receive reviews of their products.

To achieve our goal, we use an Amazon URL as the data source. We chose a camera dataset, which is shown below:

For this Challenge, we use PySpark, AWS RDS, PgAdmin, Google Collab, and PostgreSQL as tools. We ran the ETL process with PySpark and Google Collab and collected the data with the support of Amazon RDS and PostgreSQL.

## Results

The following screenshots show the ETL process in Google Collab and the SQL tables.

#### Examples of our ETL process
![Alt text](/Resources/1.png "imagen1")

![Alt text](/Resources/3.png "imagen2")

![Alt text](/Resources/4.png "imagen3")

#### Tables in PgAdmin
![Alt text](/Resources/postgres.png "imagen4")

**How many Vine reviews and non-Vine reviews were there?**

The Camera's dataset has 1,801,974 total reviews. 
Due to the applied criteria, our sample is significantly reduced, because there are only 607 reviews from Vine and 50,522 reviews from Non-Vine or Unpaid reviews. Below we present screenshots of our code:

#### Total reviews, Vine reviews and Non-Vine reviews
![Alt text](/Resources/5.png "imagen5")

**How many Vine reviews were 5 stars?** 

As for 5-Start paid Vine reviews, there were only 257 Vine reviews

#### Vine reviews with 5 Starts
![Alt text](/Resources/vine1.png "imagen6")

**How many non-Vine reviews were 5 stars?**

As we can see in the picture below, the 5-Start Non-Vine reviews were 25,220 unpaid reviews.

#### Non-Vine reviews with 5-Starts
![Alt text](/Resources/unpaid1.png "imagen7")

**What percentage of Vine reviews were 5 stars?** 

There were 257 5-Start Vine reviews of 607 Vine reviews, which means that the percentage of the 5-Starts Vine reviews was 42.33937397034596%

#### Percentage of 5-start Vine reviews
![Alt text](/Resources/vine_percentage.png "imagen8")

**What percentage of non-Vine reviews were 5 stars?**

The percentage of 5-Start Non-Vine reviews was 49.91884723486798%. That is, there were 25,220 5-Start unpaid reviews from 50,522 Non-reviews, which represent 49.91884723486798%.

#### Percentage of 5-Start Non-Vine reviews
![Alt text](/Resources/unpaid_percentage.png "imagen9")

## Summary: 

According to our analysis of Amazon's Camera dataset, there is not enough evidence to say that Vine reviews contain any positivity bias. We can remark that there are fewer Vine reviews and most of the reviews are from Non-Vine reviews.

In addition and regarding the 5-Star Vine reviews, We can note these are almost 42.34% of the total Vine reviews, while the 5-Star Non-Vine reviews have a higher percentage, 49.92% (that is almost half of the total of the others reviews).

To improve our study of this dataset, this analysis should be expanded by looking for new factors to take into account, such as the type of camera. A good option to expand the analysis would be to extract more data and apply Natural Language Processing to study the text of the reviews.
