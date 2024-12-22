# Exploratory Data Analysis in Python

A company has collected New York housing rental data from the Airbnb app during 2019. This dataset was used to train Machine Learning models during that year, in an open competition. We will now use it to conduct a study about the variables that make up the dataset in order to understand it and draw conclusions about it.

<br><br>

<div align="center">
  <img src="https://github.com/user-attachments/assets/8efb7830-7de7-4153-b9b6-8a09e409f364" alt="New York City - Exploratory Data Analysis">
</div>

<br><br>

---

## Step 1: Load the Dataset
The dataset is loaded from a public URL.

- **Dataset URL:** `AB_NYC_2019.csv`
- **Command used:** `pd.read_csv()`
- **Assigned variable:** `df`

---

## Step 2: Data Exploration
EDA is performed to understand the dataset's structure and content.

### 2.1. Dataset Dimensions
- **Command:** `df.shape`
- **Description:** Returns the number of rows and columns in the dataset.

### 2.2. Initial Preview
- **Command:** `df.head()`
- **Description:** Displays the first few rows to provide an overview of the dataset.

### 2.3. Descriptive Statistics
- **Command:** `df.describe()`
- **Description:** Generates summary statistics for numerical columns, including mean, standard deviation, and percentiles.

### 2.4. Missing Values Inspection
- **Command:** `df.isnull().sum()`
- **Description:** Shows the count of missing values for each column.

### 2.5. Data Distributions
- **Example:** Distribution of Room Types
- **Command:** `df['room_type'].value_counts()`
- **Description:** Displays the frequency of each category in the `room_type` column.

### 2.6. Data Visualization
- **Example:** Matrix Correlation
- **Command:** `sns.heatmap(data).corr()`
- **Description:** Helps to identify correlation between categories.
---

## Step 3: Save the Processed Dataset
After analysis, the processed dataset is saved to a CSV file:

- **Output file:** `processed_dataset.csv`
- **Command used:** `df.to_csv('processed_dataset.csv', index=False)`

The processed file is ready for further analysis or modeling.
