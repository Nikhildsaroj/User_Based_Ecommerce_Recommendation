# User-Based E-commerce Recommendation System

## Overview
This project implements a user-based recommendation system for eCommerce using collaborative filtering techniques. The primary goal is to enhance the shopping experience by recommending products tailored to individual users based on the purchasing behaviors of similar users. By analyzing patterns in user transactions and preferences, the system identifies correlations between users to deliver personalized product suggestions.

## Key Features
- **User-Based Recommendations:** Products are recommended based on purchases made by similar users.
- **KMeans Clustering:** Users are clustered by Age, Gender, Location, and Interests to enhance recommendations.
- **Data Visualization & EDA:** Exploratory data analysis (EDA) was conducted to identify trends in demographics and purchase frequency.
- **Model Testing:** Collaborative filtering is applied within each user cluster for tailored recommendations.

## Technologies Used
- **Programming Language:** Python
- **Development Environment:** Jupyter Notebook
- **Libraries:**
  - `Pandas`: For data manipulation and analysis.
  - `Scikit-learn`: For implementing clustering and filtering algorithms.
  - `Matplotlib`: For data visualization.
  - `Seaborn`: For enhanced visualizations.

## Project Workflow
1. **Data Collection:** Gather user transaction data and relevant features.
2. **Data Preprocessing:** Clean and preprocess the data to ensure quality and integrity.
3. **Exploratory Data Analysis (EDA):** Analyze trends in demographics and purchase frequency to inform the recommendation strategy.
4. **Clustering:** Apply KMeans clustering to segment users based on demographic information.
5. **Recommendation Generation:** Use collaborative filtering techniques within each user cluster to provide personalized product recommendations.
6. **Visualization:** Display key findings and recommendations using visualizations.

## Detailed Breakdown

### 1. Introduction
In the competitive field of eCommerce, providing personalized product recommendations is crucial to enhance customer satisfaction and drive sales. This project aims to recommend products based on collaborative filtering, focusing on what similar users have purchased. The recommendation process is enhanced by clustering users with similar characteristics using KMeans clustering. 

### 2. Data Preparation

#### Data Importing
The dataset for this project was imported from a CSV file titled `Ecommerce_product_recommendation.csv`.

#### Data Cleaning
- **Missing Values:** Handled missing values by filling them with appropriate statistical measures (e.g., median for age, mean for income, zeros for total spending, and purchase frequency).
- **Encoding Categorical Variables:** Encoded categorical variables such as Gender, Location, Interests, Product Category Preference, and User ID using LabelEncoder.
- **Normalization:** Numerical features like Age, Income, Total Spending, and Purchase Frequency were normalized using MinMaxScaler.

#### Exploratory Data Analysis (EDA)
The dataset was explored to understand the distribution of features, identify trends, and detect any anomalies, including analyzing user demographics, spending habits, and purchase frequencies.

### 3. Model Building

#### KMeans Clustering
The KMeans algorithm was applied to cluster users based on selected features: Age, Gender, Location, Income, and Interests.

### 4. Model Testing
Collaborative filtering was applied within clusters to recommend products based on purchases by similar users. Example recommendations for User ID 324 included:
- Books
- Clothing
- Sports
- Home & Kitchen
- Electronics

### 5. Model Evaluation

#### Silhouette Score
The clustering model's performance was evaluated using the Silhouette Score, calculated to be 0.3985, indicating a moderate level of cohesion and separation within clusters.

#### Evaluation with Different Cluster Numbers
The clustering model was evaluated with varying numbers of clusters (from 2 to 10), assessing metrics like Silhouette Score, Davies-Bouldin Score, Calinski-Harabasz Score, and Within-cluster Inertia.

### 6. Feature Selection & Hyperparameter Tuning
- **Adding New Features:** The dataset was expanded to include behavioral features such as `Time_Spent_on_Site_Minutes` and `Pages_Viewed`.
- **Hyperparameter Tuning:** Different numbers of clusters were evaluated on the expanded dataset to fine-tune the clustering algorithm.

### 7. Testing the Tuned Model
The refined clustering model was tested again using the expanded dataset, demonstrating improved quality in recommendations.

### 8. Conclusion
This project showcases the effectiveness of using collaborative filtering enhanced by clustering for recommending products in eCommerce. By leveraging user similarities within clusters, the system provides relevant and personalized suggestions. Future work could focus on integrating more complex behavioral patterns and testing additional machine learning models to enhance recommendation accuracy.

## Installation
To run this project, ensure you have Python installed. Then, install the required libraries:

```bash
pip install pandas scikit-learn matplotlib seaborn
