# Loyalty

Select customers to enter a loyalty program

# 1. Business Problem.

An online retail store wants to launch a loyalty program. To identify valuable customers, the company gathered sales data over a period of one year. The data used here is available at [kaggle](https://www.kaggle.com/vik2012kvs/high-value-customers-identification).

# 2. Solution Strategy

Clustering algorithms were used to find groups of similar customers based on their purchase history. The solution was built following the steps below:

**Step 01. Data description:** Identify relevant data, handle missing and inconsistent data.

**Step 02. Feature engineering:** Derive new attributes describing the customers based on their purchase history.

**Step 03. Exploratory data analysis (EDA):** Explore the data to gain insights that may be relevant later during machine learning modeling.

**Step 04. Data preparation:** Prepare the data before applying machine learning models. Normalization, rescaling, and encoding are performed when necessary.

**Step 05. Feature selection:** Select the most relevant features for the training step.

**Step 06. Determining the number of clusters:** Most clustering algorithms need the number of clusters as input. This number was determined for each ML model employed, using the silhouette score as relevant metric. The feasibility is also considered: 40 clusters, for instance, would be counterproductive from the operational point of view.

**Step 07. Machine learning modelling:** Train machine learning models.

**Step 08. Final EDA:** A new EDA is performed to characterize the average behavior of the clusters.

# 3. Top 3 Data Insights

From now on, the cluster selected to enter the loyalty program is referred to as the *Insider* cluster.

* The income from the *Insider* cluster is 42% of the total income.
* *Insider* customers purchase the widest product assortment, 1.6x greater than the assortment of the second cluster.
* *Insider* customers purchase products 13% cheaper than the global average price.

# 4. Machine Learning Model Applied

The following clustering models were trained:

* K-means
* Gaussian Mixture Model
* Hierarchical Clustering
* DBSCAN

# 5. Machine Learning Model Performance

The final model consisted of a Hierarchical Clustering on a UMAP (2D) embedding space. The images below show the silhouette plot of the final 10 clusters and the clusters on the embedding space (cluster #4 is the *Insider* cluster)

<img src="/reports/figures/silhouette.png" width="500">
<img src="/reports/figures/embedding.png" width="500">

# 6. Business Results

The number of customers in the *Insider* cluster represent 24% of the company’s customers, and the revenue those customers generate is 42% of the global revenue. *Insider* customers purchase a wide variety of cheaper products: the average product price is 13% lower than the company’s catalog average price. *Insider* customers have been customers for at least 10 months, their average purchase recency is 46 days. To conclude, the *Insider* loyalty program should favor actions to increase customers purchase frequency. Given the high income from the cluster, discount coupons can be an effective action.
