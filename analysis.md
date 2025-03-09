# Summary of Mall Customer Segmentation Analysis

## **1. Data Exploration**

The dataset, `Mall_Customers.csv`, contains customer details such as CustomerID, Gender, Age, Annual Income, and Spending Score. The dataset was explored through various statistical and visualization techniques to understand its structure and patterns.

### **Key Observations:**

- The dataset comprises multiple numerical and categorical variables.
- Initial checks confirmed the absence of null values.
- The `CustomerID` column was removed as it was not relevant for clustering.

## **2. Data Visualization**

### **Gender Distribution:**

- A count plot revealed that female customers are more frequent shoppers than male customers.

### **Age Distribution:**

- A histogram of age showed three dominant age groups: 15-22 years, 30-40 years, and 45-50 years, indicating these groups visit the mall more frequently.

### **Age vs. Spending Score:**

- Customers aged 15-42 had the highest spending scores.
- Female customers were observed to have a higher spending score than males.
- Customers with moderate spending scores (40-60) were distributed across all age groups.

### **Annual Income vs. Spending Score:**

- A scatter plot highlighted five distinct customer clusters based on income and spending habits:
  - **High Income, High Spending Score**: Ideal customers for targeted promotions.
  - **High Income, Low Spending Score**: Could be encouraged to spend more through marketing.
  - **Average Income, Average Spending Score**: Potential segment for financing options.
  - **Low Income, High Spending Score**: May or may not be a profitable target based on business policies.
  - **Low Income, Low Spending Score**: Not an ideal target group for promotions.

## **3. Data Preprocessing**

- Selected **Annual Income** and **Spending Score** as key features for clustering.
- Standardized the data using **StandardScaler** to enhance clustering performance.

## **4. Finding Optimal Clusters (Elbow Method)**

- The **Elbow Method** was applied to determine the optimal number of clusters.
- The elbow point was observed at **5 clusters**, suggesting a natural grouping within the dataset.

## **5. Model Building (K-Means Clustering)**

- Implemented **K-Means clustering** with `n_clusters=5`.
- Clustered customers based on their income and spending habits.

## **6. Clustering Results & Business Implications**

### **Identified Clusters:**

- **Cluster 1 (Low Income, High Spending Score)**: Frequent but lower-income spenders.
- **Cluster 2 (Average Income, Average Spending Score)**: Moderate spending behavior.
- **Cluster 3 (High Income, Low Spending Score)**: High-income but conservative spenders.
- **Cluster 4 (Low Income, Low Spending Score)**: Customers unlikely to contribute much revenue.
- **Cluster 5 (High Income, High Spending Score)**: Loyal and high-spending customers.

### **Business Recommendations:**

- **Focus on Cluster 5**: These are loyal and high-spending customers who should receive exclusive promotions.
- **Convert Cluster 3 to Cluster 5**: Implement personalized marketing strategies to increase spending behavior.
- **Encourage Cluster 2**: Offer flexible payment options to improve purchasing power.
- **Evaluate Cluster 1**: Monitor profitability before targeting promotions.
- **Exclude Cluster 4**: These customers have low spending habits and limited income, making them less ideal for targeting.

## **Conclusion**

This analysis successfully segmented customers into five distinct groups based on their spending behavior and income levels. These insights can help businesses implement targeted marketing strategies to maximize revenue and improve customer engagement.
