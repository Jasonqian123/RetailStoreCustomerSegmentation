# Retail Store Customer Segmentation
## 📌 Overview
This project focuses on segmenting customers of a retail store based on their purchasing behaviors. Using clustering techniques, it aim to identify distinct customer groups to help the business tailor marketing strategies and drive more revenue.

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

![Elbow Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/elbow.png?raw=true)

</div>

Using the K-Means clustering algorithm from the sklearn library, we performed a bivariate clustering analysis based on Annual Income and Spending Score. By setting the number of clusters to 5 (n_clusters = 5), the algorithm grouped all data points into five distinct customer segments.
Each data point was assigned a cluster label, and we visualized the results by plotting the data points, colored according to their assigned cluster, along with the center points (*) of each group. This segmentation clearly categorizes customers into five distinct groups based on their income levels and spending behavior.


## 📊 Visualizations
- Identified **5 key customer segments** based on income and spending behavior.


## 🔍 Key Findings
- Identified **5 key customer segments** based on income and spending behavior.

## 🔊 Recommendations
- Identified **5 key customer segments** based on income and spending behavior.
