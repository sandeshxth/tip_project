# Detect Fraudulent Credit Card Transactions

## Project Overview
The objective of this project is to develop a robust and efficient machine learning model to detect fraudulent credit card transactions. Credit card fraud is a significant issue in the financial industry, leading to substantial financial losses for banks and consumers. By leveraging data science and machine learning techniques, this project aims to identify fraudulent transactions with high accuracy, thus minimizing the impact of fraud on the financial ecosystem.

### Dataset Acquisition and Initial Exploration
- **Tasks:**
  - Received the dataset `fraudTest.csv` from the client.
  - Started initial exploration of the dataset to understand its structure and content.

- **Details:**
  - The dataset includes various features related to credit card transactions.
  - Initial observations about the data structure, missing values, and data types.

- **Initial exploration of the dataset 'fraudTest.csv':** 
  ![Dataset Overview](Images/dataset_overview_image.png)

### Exploratory Data Analysis (EDA)

#### Data Understanding and Overview
- **Tasks:**
  - Investigated the distribution of classes in the dataset.
  - Analyzed the feature types and the presence of missing values.

- **Details:**
  - **Class Distribution:** The dataset has a class imbalance problem with a significantly lower number of fraudulent transactions compared to legitimate ones.
  - **Feature Types:** Features include categorical variables, numerical features, and possibly timestamps.

### Class Distribution

<p float="left">
  <img src="Images/class_distribution_image.png" alt="Class Distribution" width="45%" />
</p>

This image illustrates the distribution of classes (fraudulent vs. non-fraudulent transactions) in the dataset.

### Feature Types and Missing Values

<p float="left">
  <img src="Images/feature_types_and_missing_values_image.png" alt="Feature Types and Missing Values" width="45%" />
</p>

This image provides insights into the types of features present in the dataset and highlights any missing values. There were no missing values found in the provided dataset.

#### 2.2 Data Visualization
- **Tasks:**
  - Created visualizations to identify patterns or anomalies in the data.
  - Calculated Fraud rate per category
  - Calculated Fraud rate by time of day
  - Calculated Fraud rate by day of the week

- **Details:**
  - **Distribution of Transaction Amounts:** Visualized the differences in transaction amounts between fraudulent and non-fraudulent transactions.
  - **Fraud rate per category:** Explored the relationships between different categories and their findings on why certain categories might have higher fraud rates compared to others.
  - **Fraud rate by time of day:** Early and late hour showed significant increase in fraud rates compared to normal hours.
  - **Fraud rate by day of the week:** Weekends had lower fraud rates than that of weekdays

### Visualizations

<p float="left">
  <img src="Images/category.png" alt="Fraud Rate per Category" width="45%" />
  <img src="Images/timeofday.png" alt="Fraud Rate by Time of Day" width="45%" />
</p>

<p align="center">
  <img src="Images/dayofweek.png" alt="Fraud Rate by Day of Week" width="65%" />
</p>


#### Handling Missing Data
- **Tasks:**
  - Identified and handled missing values in the dataset.
  - Dropped non-numeric or irrelevant columns.
  - Encoded categorical variables.

#### Applying SMOTE
SMOTE (Synthetic Minority Over-sampling Technique) is used to address class imbalance in datasets by generating synthetic samples for the minority class. This helps balance the class distribution, improving the performance of machine learning models in detecting rare events, such as fraudulent transactions.
- **Tasks:**
  - Applied SMOTE to address class imbalance.
<p float="left">
  <img src="Images/aftersmote.png" alt="Data Balanced after performing smote" width="45%" />
  <img src="Images/smotegraph.png" alt="Fraud Rate by Time of Day" width="45%" />
</p>

#### Key Steps in SMOTE:
1. **Select Minority Instances:** Randomly choose instances from the minority class.
2. **Find Nearest Neighbors:** Identify the k-nearest neighbors for each selected instance.
3. **Generate Synthetic Samples:** Create new samples by interpolating between the selected instance and its neighbors.








