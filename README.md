## 🎯 Goal  
Conduct **customer personality analysis** to gain a deeper understanding of different customer types. This helps businesses tailor their products to meet the needs and behaviors of various customer segments, improving marketing efficiency and boosting sales.

## 📝 Tasks  
- Fill missing values and identify new informative features from the original 29 features.  
- Simplify categorical features, e.g., reduce the "education" feature from 6 to 3 categories to avoid excessive detail and improve model quality.  
- Analyze distributions of continuous features and apply Box-Cox transformation for normalization (instead of ineffective logarithmic transformation).  
- Handle outliers and remove correlated features to obtain a cleaner, more informative dataset.  
- Encode categorical features using Label Encoding and One-Hot Encoding.  
- Standardize all features to improve model performance.  
- Apply clustering algorithms (KMeans, DBSCAN, Agglomerative Clustering) with hyperparameter tuning.  
- Visualize data distribution with Self-Organizing Map (SOM) and evaluate cluster quality using statistical methods.

## 🛠 Solution  
- Simplified categorical variables for clearer, more manageable data during model training.  
- Applied Box-Cox transformation to bring distributions closer to normal, improving model results.  
- Removed outliers and correlated features to reduce noise and redundancy.  
- Encoded categorical variables and standardized data for better algorithm performance.  
- Ran multiple clustering algorithms and found DBSCAN unsuitable for this task; Agglomerative Clustering gave the best results.  
- Used SOM for data density visualization and structure discovery.  
- Analyzed cluster differences using boxplots, mean barplots, and statistical tests (ANOVA, Mann-Whitney).

## 📊 Results  
Dataset source: [Kaggle: Customer Personality Analysis](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis) 😊

| Method                          | Number of Clusters | Silhouette Score | Calinski-Harabasz Index | Davies-Bouldin Index | Significant Features |
|--------------------------------|--------------------|------------------|------------------------|----------------------|---------------------|
| K-Means                        | 2                  | 0.2479           | 835.77                 | 1.5574               | 19                  |
| Agglomerative Clustering (ward) | 2                  | **0.3446**       | 628.01                 | 1.6289               | 22                  |

- Feature correlation threshold: ≤ 0.75  
- Agglomerative Clustering showed the best performance with a higher Silhouette Score, indicating better clustering quality.

## 🚀 Next Steps  
- Explore the impact of different preprocessing methods (e.g., varying correlation thresholds) on clustering quality.  
- Implement cross-validation to assess stability and reproducibility of identified segments.
