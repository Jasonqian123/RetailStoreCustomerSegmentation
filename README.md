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
- **Encode categorical variables** (e.g., Gender) for machine learning compatibility.  

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

---
### 3️⃣ **Clustering Algorithms**
- **K-Means Clustering**: Used for segmenting customers into distinct groups
- **Hierarchical Clustering**: To validate and compare cluster structures

## 📊 **Methodology**  

### 1️⃣ **Data Preprocessing**  
- **Handle missing values**, detect outliers, and **standardize numerical features**.  
- **Encode categorical variables** (e.g., Gender) for machine learning compatibility.  

---

### 2️⃣ **Exploratory Data Analysis (EDA)**  

  #### Visualizing Customer Distributions (Age, Income, and Spending Score)  

  ##### Distribution Plots (Histograms & KDE)  
![Displot Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/distmix.png?raw=true)  

- **Age:** The **left-skewed distribution** indicates that most customers are **young adults (20-40 years old)**, making them the core consumer base.  
- **Annual Income:** The majority earn **$50K-$80K**, followed by a secondary group at **$20K-$50K**, with a smaller segment earning **above $85K**. Given the **2024 U.S. average salary of $59,228**, most customers fall **within or above the national standard**, indicating a **predominantly middle-income audience** with some high earners.  
- **Spending Score:** The **normal distribution** suggests a **balanced spending pattern**, with most customers having **moderate spending habits** and fewer extreme high or low spenders.
  
##### Gender-Based KDE Comparison 
![KDE Plot Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/kdemix.png?raw=true)  

- **Age:** **Females dominate** the younger age group, while **males are more evenly distributed**.  
- **Annual Income:** No major **income disparity**, though **males have a slightly wider income range**.  
- **Spending Score:** **Females tend to spend more**, while **male spending habits are more varied**.  

---
  #### **Correlation analysis** to understand relationships between variables
  ####Pairwise analysis** (e.g., Income vs. Spending Score) to identify patterns

## 📊 Methodology
### 1️⃣ **Data Preprocessing**
- Handle missing values, outliers, and standardize numerical features
- Encode categorical variables (e.g. Gender)

## 2️⃣ **Exploratory Data Analysis (EDA)**  

### **Visualizing Customer Distributions by Age, Income, and Spending Score**  

#### **📊 Distribution Plots (Histograms & KDE)**  
![Displot Image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/distmix.png?raw=true)  

- **Age:** The slightly **left-skewed distribution** suggests that the majority of customers are **young adults (20-40 years old)**, making them the core consumer base.  
- **Annual Income:** Most customers earn **$50K-$80K**, followed by a secondary group at **$20K-$50K**, with few earning **above $85K**. Given the **2024 U.S. average salary of $59,228**, most customers fall **within or above the national standard**, indicating a **primarily middle-income audience** with some high earners.  
- **Spending Score:** A **normal distribution** suggests **balanced spending behavior**, with most customers exhibiting **moderate spending habits** and fewer extreme high or low spenders.  

  #### **Gender-Based KDE Comparison**
![image](https://github.com/Jasonqian123/RetailStoreCustomerSegmentation/blob/main/kdemix.png?raw=true)
    - `Age`: Females dominate the younger age group, while males are more evenly distributed.
    - `Annual Income`: No major difference in earnings, though males have a slightly wider range.
    - `Spending Score`: Females tend to spend more, while male spending habits are more varied.
  


### 3️⃣ **Clustering Algorithms**
- **K-Means Clustering**: Used for segmenting customers into distinct groups
- **Hierarchical Clustering**: To validate and compare cluster structures

## 📊 Visualizations
- Identified **5 key customer segments** based on income and spending behavior.


## 🔍 Key Findings
- Identified **5 key customer segments** based on income and spending behavior.

## 🔊 Recommendations
- Identified **5 key customer segments** based on income and spending behavior.
