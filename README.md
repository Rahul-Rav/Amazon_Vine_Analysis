# Amazon_Vine_Analysis

## Overview
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies can pay a small fee to Amazon and provide products to Amazon Vine members, who are required to publish a review. Through the use of Pandas and PySpark, we perform an ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. We then used PySpark and Pandas to determine if there is any bias toward favorable reviews from Vine members in the dataset.

## Results

### Paid

#### Paid 5-Star reviews
<img width="547" alt="paid_5star_counts" src="https://user-images.githubusercontent.com/95504135/163742858-5e3a92f6-2f65-4f28-b441-997c4f5c9014.png">

#### Percentage of Paid 5-Star reviews
<img width="485" alt="paid_5star_percentage" src="https://user-images.githubusercontent.com/95504135/163742864-afcc406b-5ec4-438f-a79f-9ab345dcbdd5.png">

* 48 out of the 94 paid reviews are 5-Star reviews

* 51% of the paid reviews have been given 5-Star reviews.

### Unpaid

### Unpaid 5-Star reviews
<img width="590" alt="unpaid_5star_counts" src="https://user-images.githubusercontent.com/95504135/163742890-6b8ebefe-bec0-4c8e-a754-ba19ed8243d5.png">


### Percentage of Unpaid 5-Star reviews
<img width="548" alt="unpaid_5star_percentage" src="https://user-images.githubusercontent.com/95504135/163742900-c308fc7f-2637-4939-95bb-9ec6d3538942.png">

* 15,663 out of 40,471 paid reviews are 

* 38.7% of the unpaid reviews have been given 5-Star reviews.

## Summary
Based on the data that was filtered we see that among the paid reviews, there are only a total of 94 with 48 of them being 5-Star reviews. Looking at the unpaid reviews, there are a total of 40,471 reviews which is significantly more than the total of paid reviews. The percentage of 5-Star unpaid reviews is 38.7%, which is less than the paid reviews, but one must keep in mind the sheer total amount of unpaid reviews vs. paid reviews. At a glance, we can infer that there is a bias towards paid reviews, as the 5-Star reviews are 12.3% higher than the unpaid reviews.
To support the potential bias statement, further analyses through filtering could be done. Filtering 'verified_purchase' to only 'Y' or confirmed verified purchases could give us an insight to whether some of these unpaid reviews have biases of their own and possibly close or widen the gap between 5-star review percentages between paid and unpaid reviews.
