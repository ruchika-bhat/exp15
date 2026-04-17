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

This method rescales values to a fixed range (0 to 1). It maintains the relative differences between values but removes the effect of scale, making different features comparable.

# Z-Score Normalization:

(df[col] - df[col].mean()) / df[col].std()

Z-score normalization standardizes data by centering it around the mean (0) and scaling it using standard deviation. It is useful when data has variation or outliers.

# Decimal Scaling:

df[col] / 10^n

This technique reduces the magnitude of values by shifting the decimal point. It simplifies large numbers while preserving their proportions.

# Label Encoding:
LabelEncoder()

Converts categorical text into numeric form by assigning each category a unique integer. It is suitable when categories have a logical order or ranking.

# One-Hot Encoding:
pd.get_dummies()

Transforms categorical data into multiple binary columns. Each category is represented independently, preventing incorrect ordinal relationships.

# Dummy Encoding:
drop_first=True

Removes one category column to avoid redundancy and multicollinearity, ensuring better performance in statistical models.

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
