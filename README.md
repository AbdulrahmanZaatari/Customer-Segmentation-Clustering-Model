# Customer Segmentation Clustering Model

This project demonstrates a machine learning-based customer segmentation model using clustering techniques. By analyzing customer data, we group individuals into distinct clusters based on shared characteristics, enabling businesses to better understand and target their customer base.

## Introduction
Customer segmentation is essential for businesses aiming to personalize their marketing strategies. This project applies clustering techniques like K-Means and Hierarchical Clustering to segment customers based on their Recency, Frequency, and Monetary (RFM) metrics derived from transaction data.

## Dataset
The dataset used for this project is available on Kaggle: [Customer Segmentation Dataset](https://www.kaggle.com/datasets/yasserh/customer-segmentation-dataset).

### Key Features:
- **InvoiceDate**: The date of the transaction.
- **Quantity**: The number of products purchased.
- **UnitPrice**: The price per product.
- **CustomerID**: A unique identifier for each customer.
- **Country**: The customer's country.

## Technologies Used
- **Python**: Programming language
- **Jupyter Notebook**: For interactive development
- **Pandas & NumPy**: Data manipulation and analysis
- **Matplotlib & Seaborn**: Visualization
- **Scikit-learn**: Machine learning

### Data Preprocessing
- Removed rows with missing or invalid values for `CustomerID`, `Quantity`, and `UnitPrice`.
- Added a `TotalPrice` column calculated as `Quantity * UnitPrice`.

### RFM Analysis
RFM (Recency, Frequency, Monetary) metrics were calculated for each customer:
- **Recency**: Days since last purchase.
- **Frequency**: Number of unique transactions.
- **Monetary**: Total spending.

### Scaling RFM Data
Scaled the RFM values for clustering using `StandardScaler`.

### Clustering
The optimal number of clusters was determined using the **Elbow Method**, and K-Means clustering was applied. The model's performance was evaluated using the silhouette score.

## Results

1. **Elbow Method**: Used to identify the optimal number of clusters.
2. **Cluster Assignments**: Customers were segmented into meaningful clusters.
3. **Silhouette Score**: The model achieved a silhouette score of **0.616**, indicating well-separated clusters.
4. **Visualizations**:
   - Pairplot of clusters to understand relationships between RFM features.
   - Scatterplot of Monetary vs. Frequency for cluster visualization.

