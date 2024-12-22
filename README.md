# Exploratory Data Analysis in Python

A company has collected New York housing rental data from the Airbnb app during 2019. This dataset was used to train Machine Learning models during that year, in an open competition. We will now use it to conduct a study about the variables that make up the dataset in order to understand it and draw conclusions about it.

<br><br>

<div align="center">
  <img src="https://github.com/user-attachments/assets/8efb7830-7de7-4153-b9b6-8a09e409f364" alt="New York City - Exploratory Data Analysis">
</div>

<br><br>

## Steps to Perform EDA

Below is the complete Python code to perform all the steps, including loading the dataset, conducting exploratory data analysis (EDA), and saving the processed dataset:

```python
import pandas as pd

# Step 1: Load the dataset
URL = 'https://raw.githubusercontent.com/4GeeksAcademy/data-preprocessing-project-tutorial/main/AB_NYC_2019.csv'
df = pd.read_csv(URL)

# Step 2: Perform a complete EDA
# Dimensions of the dataset
print("Dataset Dimensions:", df.shape)

# Preview the dataset
print("First few rows of the dataset:")
print(df.head())

# Descriptive statistics
print("Descriptive statistics:")
print(df.describe())

# Null value inspection
print("Missing values per column:")
print(df.isnull().sum())

# Analyzing distributions (example: room types)
print("Distribution of room types:")
print(df['room_type'].value_counts())

# Step 3: Save the processed dataset
output_file = 'processed_dataset.csv'
df.to_csv(output_file, index=False)
print(f"Processed dataset saved to {output_file}")



