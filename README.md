# Retail Store Customer Segmentation
## 📌 Overview
This project focuses on segmenting customers of a retail store based on their purchasing behaviors. Using clustering techniques, it aim to identify distinct customer groups to help the business tailor marketing strategies and drive more revenue.

<div align="center">

![Seg Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/seg.png?raw=true)

</div>

## 📂 Dataset
- **Source:** [https://absentdata.com/wp-content/uploads/2023/03/Mall_Customers.csv]
- **Columns:**
  - `CustomerID`: Unique identifier for each customer
  - `Age`: Age of the customer
  - `Gender`: Male/Female
  - `Annual Income (k$)`: Annual income in thousands
  - `Spending Score (1-100)`: A score assigned based on spending behavior, reflecting customer purchasing power and engagement

## 📊 **Methodology**  

### 1️⃣ **Data Preprocessing**  
- **Handle missing values**, detect outliers, and **standardize numerical features**.  
- **Encode categorical variables** (e.g., Gender) for segmentation analysis.  

---

### 2️⃣ **Exploratory Data Analysis (EDA)**  

#### **Visualizing Customer Distributions** (Age, Income, and Spending Score)  

##### **Distribution Plots (Histograms & KDE)**  
![Displot Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/distmix.png?raw=true)  

- **Age:** The **left-skewed distribution** indicates that most customers are **young adults (20-40 years old)**, making them the core consumer base.  
- **Annual Income:** The majority earn **$50K-$80K**, followed by a secondary group at **$20K-$50K**, with a smaller segment earning **above $85K**. Given the **2024 U.S. average salary of $59,228**, most customers fall **within or above the national standard**, indicating a **predominantly middle-income audience** with some high earners.  
- **Spending Score:** The **normal distribution** suggests a **balanced spending pattern**, with most customers having **moderate spending habits** and fewer extreme high or low spenders.  

##### **Gender-Based KDE Comparison**  
![KDE Plot Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/kdemix.png?raw=true)  

- **Age:** **Females dominate** the younger age group, while **males are more evenly distributed**.  
- **Annual Income:** No major **income disparity**, though **males have a slightly wider income range**.  
- **Spending Score:** **Females tend to spend more**, while **male spending habits are more varied**.  

#### **Correlation Analysis** (Understanding Relationships Between Variables)  

<div align="center">

![KDE Plot Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/corr.png?raw=true)

</div>

- Age vs. Spending Score (-0.33): A negative correlation suggests that younger customers tend to have higher spending scores, while older customers are less likely to make high purchases.
- Age vs. Annual Income (-0.012): The correlation is very close to zero, indicating no strong relationship between age and income in this dataset.
- Annual Income vs. Spending Score (0.0099): The almost zero correlation means that higher income does not necessarily lead to higher spending scores.
  
---
### 3️⃣ **Clustering Algorithms**
Annual Income helps define a customer’s purchasing capability. Spending Score helps measure actual spending behavior. Combining these two variables allows businesses to create more precise customer segments and improve marketing strategies. Therefore, it adopt the bivariate clustering method to segment customers.

#### **Elbow Method for Optimal Cluster Selection**: Used to determine the optimal number of clusters (K)

<div align="center">

![Elbow Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/elbow.png?raw=true)

</div>

The Elbow Method was used to determine the optimal number of clusters. A for loop was employed to calculate the inertia score for cluster numbers ranging from 1 to 10. The inertia values were then visualized using a line chart. The plot indicates that when the number of clusters (K) = 5, an elbow point appears, suggesting that 5 clusters may be an optimal choice for segmenting customers effectively.

#### **K-Means Clustering**: Used for segmenting customers into distinct groups

<div align="center">

![Seg Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/seg.png?raw=true)

</div>

Using the K-Means clustering algorithm from the sklearn library, we performed a bivariate clustering analysis based on Annual Income and Spending Score. By setting the number of clusters to 5 (n_clusters = 5), the algorithm grouped all data points into five distinct customer segments.<br>

Each data point was assigned a cluster label, and we visualized the results by plotting the data points, colored according to their assigned cluster, along with the center points (*) of each group. This segmentation clearly categorizes customers into five distinct groups based on their income levels and spending behavior.<br>

Customers represented by the green (Cluster 2) and purple (Cluster 4) groups exhibit high spending scores, indicating that they are the most engaged and profitable customer segments. These two groups should be prioritized as primary target audiences for marketing campaigns, loyalty programs, and personalized promotions to maximize revenue.


## 🔍 Key Findings

- Gender Distribution in High-Value Segments:<br>
  By analyzing the gender proportions across clusters, we observe that Cluster 2 (53.8% female) and Cluster 4 (59.1% female), which represent the most profitable customer segments, have a higher percentage of female customers. This suggests that marketing efforts should focus on female-oriented products and promotions, such as fashion, beauty, and lifestyle items, to maximize engagement and revenue.
  
- Younger Customers Have Higher Purchase Intentions:<br>
  By analyzing the average age and spending score across clusters, we find that younger customers exhibit the highest purchase intention(Cluster 2: Average age = 32.6, Average spending score = 82.1; Cluster 4: Average age = 25.2, Average spending score = 79.3). This indicates that younger consumers tend to spend more actively, whereas older customers have relatively lower purchase intentions. Targeting younger demographics with trend-driven promotions and digital engagement strategies could enhance profitability.
  
- Annual Income Does Not Directly Influence Spending:<br>
  Despite common assumptions, higher income does not necessarily correlate with higher spending scores. For instance, Cluster 1 (avg income = $88.2k) has a low spending score (17.1), while Cluster 4 (avg income = $25.7k) maintains a high spending score (79.4). This suggests that marketing strategies should focus on behavioral segmentation rather than income levels, emphasizing factors such as shopping habits, brand engagement, and lifestyle preferences.

<div align="center">

![Seg_gender Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/seg_gender.png?raw=true)

</div>

<div align="center">

![Seg_avg Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/seg_avg.png?raw=true)

</div>

## 🔊 Recommendations
### **1️⃣ Focus on Female-Oriented Marketing**
Since high-spending clusters (2 & 4) are predominantly female, prioritize fashion, beauty, and lifestyle promotions. Implement personalized discounts, influencer partnerships, and loyalty programs to drive engagement. 

### **2️⃣ Target Younger Consumers with Digital Campaigns**  
With younger customers showing the highest spending intent, invest in social media marketing (TikTok, Instagram), app-exclusive deals, and trend-driven promotions like curated product bundles and flash sales.

### **3️⃣ Shift from Income-Based to Behavioral Segmentation**  
Since income doesn’t predict spending, use AI-driven profiling to tailor promotions based on shopping habits. Optimize personalized recommendations, omnichannel engagement, and data-driven pricing strategies to boost conversions.
