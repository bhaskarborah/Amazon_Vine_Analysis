#   Amazon-Vine-Review-Analysis

## Overview of Project
The objective of this project is analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.


## Purpose

The required input data is in approximately 50 similar files. We have to consider one of these files.

The link to the files is as below:
https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt

The purpose of this project is to provide the below deliverables:

Deliverable 1: Perform ETL on Amazon Product Reviews
Deliverable 2: Determine Bias of Vine Reviews
Deliverable 3: A Written Report on the Analysis

## Results

### Reading and processing the dataset

The required file has been read from AWS:

![Screen Shot 2021-09-24 at 12.12.01 PM](https://i.imgur.com/nfM6WhL.png)

The required customer dataframe has been created:

![Screen Shot 2021-09-24 at 12.12.36 PM](https://i.imgur.com/hbfpXSU.png)

The required products dataframe has been created:

![Screen Shot 2021-09-24 at 12.13.19 PM](https://i.imgur.com/d3ZTU7Z.png)

The required review dataframe has been created:

![Screen Shot 2021-09-24 at 12.13.57 PM](https://i.imgur.com/a8Hu03K.png)


The required vine dataframe has been created:

![Screen Shot 2021-09-24 at 12.14.31 PM](https://i.imgur.com/k7Q9nbR.png)

The connectivity to AWS RDS has been set up:

![Screen Shot 2021-09-24 at 12.23.46 PM](https://i.imgur.com/RpcWopm.png)

The required tables are loaded into the AWS RDS - Postgres Instance:

![Screen Shot 2021-09-24 at 12.29.34 PM](https://i.imgur.com/PRrF0Ps.png)

The required results are as below:

### How many Vine reviews and non-Vine reviews were there?

#### Vine

![Screen Shot 2021-09-24 at 12.42.38 PM](https://i.imgur.com/DADcADH.png)

#### Non-Vine

![Screen Shot 2021-09-24 at 12.43.36 PM](https://i.imgur.com/FrD7Qft.png)

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

#### Vine

![Screen Shot 2021-09-24 at 12.44.32 PM](https://i.imgur.com/zyU2DBq.png)

#### Non Vine

![Screen Shot 2021-09-24 at 12.45.22 PM](https://i.imgur.com/fZtAhPM.png)

### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

#### Vine

![Screen Shot 2021-09-24 at 12.46.03 PM](https://i.imgur.com/U5p3taj.png)

#### Non Vine

![Screen Shot 2021-09-24 at 12.46.50 PM](https://i.imgur.com/2fG9WTx.png)


#   Amazon-Vine-Review-Summary

It can be seen that the percentage of  Non-Vine (Unpaid) 5 star reviews is 52%, whereas the percentage of Vine (Paid) 5 star reviews is only 18%.

Hence there does not seem that there is any positivity bias.

I think we can calculate the average and median vales to further support the conclusion.






