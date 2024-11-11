# MachineLearning

Customer Segmentation using Clustering
Project Overview
This project involves customer segmentation using clustering algorithms on a dataset containing customer demographics and behavioral attributes. The goal is to group customers into segments based on their purchasing behaviors and demographics, allowing for targeted marketing and personalized customer service.

Dataset
The dataset contains the following features:

CustomerID: Unique identifier for each customer
Gender: Customer gender
Age: Age of the customer
Annual Income: Customer’s yearly income
Spending Score: Score assigned based on customer spending behavior
Profession: Customer’s profession
Work Experience: Number of years of work experience
Family Size: Number of family members
Data Preprocessing
Outlier Removal: Outliers were identified and removed to improve clustering results.
Feature Scaling: Data was scaled to ensure uniformity across features.
PCA for Dimensionality Reduction: Principal Component Analysis (PCA) was applied to reduce the dataset to the most significant components, with PCA=5 found to be optimal based on silhouette score.
Clustering Algorithms
Three clustering algorithms were implemented and evaluated to determine the best segmentation strategy:

K-Means Clustering

Optimal Number of Clusters: Determined by using the Elbow method, Silhouette score, and PCA. A value of K=6 with PCA=5 gave the best silhouette score and was chosen for the final clustering.
Performance Metrics: Silhouette score, inertia, and cluster visualization were used to evaluate the clustering quality.
Observation: K-Means provided clear customer segments with relatively fast computation, ideal for larger datasets.
Gaussian Mixture Model (GMM)

Cluster Evaluation: Model selection was based on AIC (Akaike Information Criterion) and BIC (Bayesian Information Criterion) to identify the optimal number of clusters.
Performance Insights: GMM performed well on the data, accommodating customers who did not fit well within fixed K-Means boundaries, thus offering flexibility in clusters.
Comparison with K-Means: While GMM offered improved flexibility, it had higher computational cost compared to K-Means.
DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

Parameter Tuning: Epsilon (ε) and minimum samples were carefully tuned to capture the natural density of customer groups while identifying and excluding noise (outliers).
Benefits: DBSCAN effectively identified high-density clusters and classified low-density areas as noise, making it useful for finding distinct segments where clusters may vary significantly in density.
Limitations: DBSCAN was sensitive to ε values, and performance varied with different density patterns within the data.
Results and Observations
Clustering Results with and without Outlier Removal: The clustering results with outlier removal yielded better-defined clusters, improving the silhouette score and overall segmentation quality.
Optimal Clustering: After evaluating all three algorithms, K-Means (K=6, PCA=5) was selected as the primary model due to its performance and interpretability, though GMM and DBSCAN provided valuable insights into customer behavior.
Performance Comparison: The best clustering results were summarized in a table comparing each method in terms of silhouette scores, inertia, AIC/BIC, and execution time.
Conclusion
This project successfully segmented customers based on demographic and behavioral data, revealing valuable customer segments. The combination of clustering methods allowed for flexible and insightful segmentation, supporting data-driven marketing strategies.

Future Improvements
Implement additional clustering methods to refine segment analysis.
Explore hierarchical clustering for deeper insights into sub-group structures within each segment.
