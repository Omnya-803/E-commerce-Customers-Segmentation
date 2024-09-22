# E-commerce-Customers-Segmentation
**Project Overview**

This project aims to segment customers of an e-commerce platform based on their demographic and transactional behavior using unsupervised machine learning techniques. By clustering customers into groups, we can better understand their behavior patterns, which can be used to tailor personalized offers, improve customer loyalty, and increase satisfaction with the store.

**Goals**

To identify distinct customer segments based on their demographics and transactional behavior.

To provide actionable insights for marketing strategies, including personalized coupon distribution and customer retention initiatives.

**Dataset**

The dataset includes various features related to customer demographics, transaction details, coupon usage, and merchant/branch information. The tables used include:

customers: Contains customer demographics.
genders: Contains gender information.
cities: Contains city information.
transactions: Contains transactional data.
branches and merchants: Contains details about the branches and merchants involved in transactions.
The tables were merged into a single dataset with transactions as the primary table.

**Feature Selection**

The following features were selected for clustering:

transaction_count: Number of transactions per customer.

coupons_claimed: Number of coupons claimed by each customer.

coupons_burnt: Number of coupons redeemed by each customer.

branch_id: The branch where the transaction occurred.

merchant_id: The merchant involved in the transaction.

gender: Gender of the customer (encoded as Male/Female).

city: One-hot encoded city information.

**Model Approach**

We used the K-Means clustering algorithm for customer segmentation. The following steps were performed:

Data Preprocessing: Cleaned and prepared the data, handling null values and standardizing the features.

Feature Selection: Used the selected features mentioned above to train the model.

Choosing the Optimal Number of Clusters: Used the Elbow Method and Silhouette Score to determine the optimal number of clusters.

Elbow Method: Plotted inertia values (sum of squared distances) for different values of k and chose the point where the curve bends.

Silhouette Score: Used to measure how well each point is clustered, with a higher score indicating better-defined clusters.

**Model Evaluation**

Inertia: Measures how tightly grouped the clusters are (lower is better). We plotted inertia across a range of cluster sizes using the Elbow Method to choose the optimal number of clusters.

Silhouette Score: For our K-Means model, we calculated a silhouette score of 0.08, which suggests that the clusters are relatively overlapping but still offer some distinction in customer behaviors.

**Model Insights**

We tested multiple cluster values (k = 2 through k = 10) and settled on 6 clusters based on the Elbow Method and insights from the data.

**Key Findings**

The following insights were drawn from the clustering model:

Cluster 0:

Customers with low transaction count and low coupon engagement.
These customers may need targeted marketing efforts, such as time-sensitive offers or special discounts, to improve engagement.

Cluster 1:

High transaction count but low coupon usage.
This group appears loyal but less sensitive to coupons. Consider offering exclusive deals to reward their loyalty and encourage further engagement.

Cluster 2:

High coupon claim and burn rate.
These customers are actively using coupons and are a prime target for promotional campaigns to maintain their loyalty.

Cluster 3:

Predominantly customers from specific cities with medium transaction counts.
City-specific offers or branch-centric deals could further engage this segment.

Cluster 4:

A mix of low transaction count and high coupon claiming, indicating potential for engagement with a better offer strategy.

Cluster 5:

High transaction count and high coupon usage, indicating loyal customers highly engaged with offers.
These customers should be given exclusive deals to maximize their lifetime value.

**Segment Recommendations**

Cluster 2 and Cluster 5 should be the primary targets for coupon-based loyalty programs. They are already highly engaged with offers and can be incentivized further with personalized promotions.

Cluster 1 represents a loyal customer base that could benefit from non-coupon rewards such as exclusive membership perks or early access to new products.
Cluster 0 should be the focus of retention efforts, offering introductory coupons to encourage higher transaction counts.

City-Specific Targeting: Clusters with high concentrations in specific cities can benefit from regional promotions and partnerships with local merchants.

**Visualization**

Visualizations were used to better understand customer distribution across clusters:

Bar plots to show the average transaction count, coupons claimed, and coupons burnt for each cluster.

Stacked bar charts to represent gender and city distributions within each cluster.

**Next Steps**

Further Optimization: Test other unsupervised learning models like Hierarchical Clustering to see if they provide better-defined customer segments.

Customer Profiling: Develop deeper customer profiles by incorporating time-based analysis to see how customers' behaviors change over time.

Implementation: Use the insights from segmentation to design tailored marketing campaigns, reward programs, and promotions.

**Conclusion**

This project successfully segmented customers based on their demographic and transactional behaviors. By analyzing each segment, we were able to provide recommendations for coupon distribution and loyalty programs to enhance customer satisfaction and retention.
