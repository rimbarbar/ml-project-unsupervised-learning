# machine_learning_project-unsupervised-learning

## Project Overview
This project applies unsupervised learning techniques to segment wholesale customers based on purchasing behavior. Using clustering methods such as K-Means and Hierarchical Clustering, the goal is to uncover distinct customer groups that businesses can use for targeted marketing strategies and inventory management.

## Dataset
The dataset used in this project is the Wholesale Dataset, which contains features such as annual spending in different product categories (e.g., Fresh, Milk, Grocery, Frozen, Detergents, Paper, and Delicassen).

## Project Workflow

### 1. Data Understanding and Exploratory Data Analysis
- Conducted statistical analysis and visualized distributions.
- Identified outliers using a boxplot.
- Observed correlations between features using a heatmap.
- **Key Insights:**
  - Strong correlation between Grocery and Detergents_Paper indicates potential redundancy in features.
  - Some features have skewed distributions requiring transformation or normalization.

### 2. Data Cleaning and Preprocessing
- No missing values were present in the dataset.
- Standardized the data using StandardScaler to ensure equal weighting for clustering.
- Applied PCA to visualize variance across dimensions.
- **Insights:**
  - PCA revealed that the first two components explain most of the variance, confirming that dimensionality reduction was useful.

### 3. Clustering Methods and Evaluation

#### **K-Means Clustering**
- Used the elbow method and silhouette score to determine the optimal number of clusters.
- Chose K=3 as it balances within-cluster variance and interpretability.
- Why not a higher K? While increasing K reduces inertia, the silhouette score indicates that K=3 provides a reasonable cluster separation without over-segmentation.

#### **Hierarchical Clustering**
- Compared Agglomerative Clustering to K-Means.
- Dendrogram suggested a different number of clusters.
- **Why the difference?** Hierarchical clustering is more sensitive to data distribution, and it doesn’t assume cluster shapes, which explains the variation.

### 4. Results and Business Insights

- **Segment Characteristics:**
  - Cluster 1: High spenders across all categories (likely hotels/restaurants).
  - Cluster 2: Moderate spenders, mostly on groceries and detergents (small retailers).
  - Cluster 3: Low spenders, focused on fresh produce (cafes, small food businesses).
- **Practical Applications:**
  - Businesses can target high spenders with premium offers.
  - Low spenders may require cost-effective product bundles and specialized discounts. 
  - Understanding segments allows for better marketing strategies.

## Future Improvements
- Experiment with different distance metrics for hierarchical clustering.
- Use DBSCAN for density-based clustering.
- Fine-tune hyperparameters for improved cluster separation.

## Conclusion
This project successfully identified meaningful customer segments using unsupervised learning techniques. The insights can aid businesses in decision-making related to marketing and product inventory optimization.

