# **Project Plan: Identifying Key Sellers on Mercado Libre**

## **Objective**
The goal of this project is to analyze and enhance the segmentation of sellers on Mercado Libre by focusing on their performance within a specific category. While sellers are already grouped by `reputation` and `status`, this analysis aims to provide actionable insights by aggregating data and applying clustering to identify distinct profiles.

---

## **Steps to Approach the Problem**

### **1. Data Extraction**
Using Mercado Libre’s public APIs, I will extract relevant information about sellers and their products in a chosen category. The process involves:
- Selecting a specific category to focus the analysis.
- Extracting product details such as:
  - Total number of items listed.
  - Ranking of items (e.g., positions in search results).
  - Additional metrics like free shipping and MercadoPago acceptance.

#### API Endpoints:
- **Category Data**: `https://api.mercadolibre.com/sites/MLA/search?category={CATEGORY_ID}`
- **Seller Data**: `https://api.mercadolibre.com/items?ids={ITEM_ID_1},{ITEM_ID_2},...`

### **2. Data Aggregation**
Aggregate data at the seller level to generate meaningful metrics:
- **Total Articles**: Count of items listed by the seller in the selected category.
- **Top 1000 Percentage**: Proportion of items appearing in the top 1000 search results.
- **Average Rank**: Mean position of items in search results.
- **Additional Indicators**: Presence of free shipping or MercadoPago usage.

This aggregated data will form the foundation for profiling sellers.

---

### **3. Exploratory Data Analysis (EDA)**
Conduct an in-depth analysis of the aggregated data:
- **Identify Patterns**:
  - Which sellers dominate the top ranks?
  - Are there clusters of sellers with similar characteristics?
- **Outlier Detection**:
  - Sellers with unusually high or low metrics, such as sales volume or average rank.

Visualizations (e.g., histograms, scatter plots) will be used to communicate findings effectively.

---

### **4. Clustering Analysis**
Apply clustering to group sellers into meaningful profiles:
- **Algorithm Selection**:
  - Use K-Means for simplicity and interpretability.
  - Optionally explore DBSCAN for identifying density-based clusters.
- **Clustering Features**:
  - Total articles.
  - Percentage of articles in the top 1000.
  - Average rank.
- **Cluster Validation**:
  - Evaluate clusters using metrics such as the Silhouette Score.

---

### **5. Insights and Recommendations**
Interpret the results of the clustering to derive actionable insights:
- **Key Profiles**:
  - High-performing sellers: Dominant in the category with high-ranking items.
  - Promising sellers: Sellers with potential to grow based on performance indicators.
  - Low-impact sellers: Sellers with minimal presence or performance in the category.
- **Actionable Recommendations**:
  - Focused commercial strategies for each seller profile.
  - Suggestions for improving seller visibility and performance.

---

### **6. Deliverables**
1. **Code Repository**:
   - A public GitHub repository containing:
     - Data extraction scripts.
     - Aggregation and clustering notebooks.
     - Documentation for replicability.
2. **Presentation**:
   - A 20-minute walkthrough of:
     - Problem definition and approach.
     - Key findings from EDA.
     - Clustering methodology and results.
     - Final insights and next steps.

---

### **7. Next Steps**
- Expand the analysis to additional categories for broader insights.
- Develop predictive models to forecast seller performance and recommend targeted strategies.

---
