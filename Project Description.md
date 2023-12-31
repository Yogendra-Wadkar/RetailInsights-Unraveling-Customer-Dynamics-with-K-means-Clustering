# Project Description

## 📋Jupyter Notebook File Data

### 1. Importing Libraries

The project begins with the essential step of importing libraries, including NumPy, Pandas, Matplotlib, Seaborn, and scikit-learn. These libraries lay the foundation for data analysis and clustering using the K-means algorithm.

### 2. Problem Statement

The dataset, sourced from Kaggle, contains information about mall customers, including ID, age, gender, income, and spending score. The objective is to apply the K-means clustering algorithm to segment customers based on their behavior and spending patterns.

### 3. Data Gathering

Data is loaded into a Pandas DataFrame using the `pd.read_csv` function. The dataset is obtained from Kaggle, adding context to the mall customer characteristics.

## 4. Exploratory Data Analysis (EDA)

Explore the dataset using key functions:

### 4.1 Checking Columns

This function provides an overview of the columns present in the dataset, aiding in understanding the variables available for analysis.

### 4.2 Dataset Information  

The `df.info()` function offers details about the data types, non-null counts, and memory usage, providing insights into the dataset's structure.

### 4.3 Descriptive Statistics  

Utilize `df.describe()` to generate descriptive statistics, including measures of central tendency, dispersion, and shape of the distribution.

### 4.4 Missing Values Check  

Identify and quantify missing values in the dataset using `df.isnull().sum()`. This step is crucial for handling or imputing missing data effectively.

Gain insights into the structure, characteristics, and identify potential missing values in the data.

## 5. Feature Engineering

Enhance the dataset through the following feature engineering steps:

### 5.1 Handling Outliers

Implement the Interquartile Range (IQR) method to identify and handle outliers. The custom function (`Finding_outliar1`) specifically targets outliers in the 'Annual Income (k$)' column.

### 5.2 Scaling

Apply scaling to 'Age,' 'Annual Income (k$),' and 'Spending Score (1-100)' using appropriate techniques. Scaling ensures compatibility with distance-based algorithms like K-means, contributing to the robustness of the model.

## 6. Model Training

Apply the K-means algorithm for 2D clustering based on age and spending score, 2D clustering based on annual income and spending score, and 3D clustering on age, annual income, and spending score.

**Elbow-Method using WCSS**: This is based on principle that while clustering performance as measured by WCSS increases (i.e. WCSS decreases) 
with increase in k, rate of increase is usually decreasing. So performance improvement for increasing number of cluster 
from, say, 3 to 4 is higher than that for increasing from 4 to 5.

### 6.1 2D Model  

Create a variable `x` representing the features for 2D clustering. Utilize the Elbow Method to determine the optimal number of clusters (K). Visualize the resulting clusters through scatter plots.

### 6.2 3D Model 

Generate a 3D scatter plot depicting clusters formed by the K-means algorithm on age, annual income, and spending score. Evaluate clustering quality using inertia and silhouette_score.

## 7. Final Note

The project concludes with a summary of the analysis of mall customer data, insights gained through clustering, and the potential for designing effective customer acquisition strategies. Feedback on the notebook is welcomed, fostering a spirit of continual exploration and learning in the field of data science.
