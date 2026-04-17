# AIM: DATA NORMALIZATION AND DATA TYPE CONVERSION

# THEORY:
Data conversion is the process of transforming data from one format or type into another so that it can be effectively used for analysis and processing.

pd.read_csv() → Converts external file data into a DataFrame.
LabelEncoder() → Converts categorical (text) data into numeric form.
pd.get_dummies() → Converts categorical variables into binary (0/1) columns.

Data normalization is the process of scaling numerical data into a consistent range to improve comparability and performance.
1. Min-Max Normalization
2. Z-Score Normalization
3. Decimal Scaling
4. Label Encoding
5. One-Hot Encoding
6. Dummy Encoding

# Data Handling (Pandas & NumPy):
import pandas as pd, import numpy as np
These libraries are used to manage and process data. Pandas organizes data into tables (DataFrames), 
while NumPy supports numerical calculations required for transformations.

pd.DataFrame(data)
Converts raw data into structured tabular form, enabling easier analysis and manipulation.

# Min-Max Normalization:

(df[col] - df[col].min()) / (df[col].max() - df[col].min())

Min-Max normalization is a scaling technique that transforms data into a fixed range, usually between 0 and 1.
It works by subtracting the minimum value and dividing by the range of the dataset.
This method preserves the relative distribution of the data while eliminating the influence of different scales.
It is particularly useful when features have different units or ranges, ensuring fair comparison across variables.

# Z-Score Normalization:

(df[col] - df[col].mean()) / df[col].std()

Z-score normalization standardizes data by converting it into a distribution with a mean of 0 and a standard deviation of 1.
This transformation indicates how far a value deviates from the mean in terms of standard deviations.
It is highly effective when dealing with datasets that contain outliers, as it reduces their impact compared to Min-Max scaling. 
This method is commonly used in statistical analysis and machine learning algorithms.

# Decimal Scaling:

df[col] / 10^n

Decimal scaling is a normalization method that reduces the magnitude of data by shifting the decimal point. 
The values are divided by a power of 10 based on the maximum value in the dataset.
This method is simple and effective for handling large numerical values while maintaining their proportional relationships. 
It is often used when a quick scaling technique is required.

# Label Encoding:
LabelEncoder()

Label encoding is a data conversion technique used to transform categorical data into numerical form by assigning each category a unique integer value.
For example, categories like "Male" and "Female" may be encoded as 1 and 0.
This method is efficient and memory-saving but should be used carefully, as it may introduce an unintended ordinal relationship between categories.

# One-Hot Encoding:
pd.get_dummies()

One-hot encoding converts categorical variables into multiple binary columns, where each category is represented by a separate column with values 0 or 1.
This technique ensures that no ordinal relationship is assumed between categories, making it suitable for nominal data.
Although it increases the number of columns, it improves the accuracy of many machine learning models.

# Dummy Encoding:
drop_first=True

Dummy encoding is a variation of one-hot encoding where one category column is dropped to avoid redundancy.
This is done to prevent the dummy variable trap, which can lead to multicollinearity in statistical models.
By removing one column, the dataset retains all necessary information while ensuring mathematical stability in regression-based models.

# Reading Dataset:
pd.read_csv()

Used to import external datasets into Python for processing, enabling real-world data analysis.

# Multi-Column Operations:
Applying normalization on multiple columns together.
Improves efficiency and consistency by performing transformations across several features simultaneously instead of individually.


# CONCLUSION:
This experiment focuses on transforming raw data into a structured and standardized format.
Normalization techniques (Min-Max, Z-score, Decimal Scaling) adjust numerical values, while encoding techniques convert categorical data into machine-readable form.
These processes ensure that data becomes consistent, comparable, and suitable for analysis and machine learning applications.
