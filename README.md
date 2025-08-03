# Road Accident Analysis Project

This project analyzes road accident data using a Jupyter Notebook for data processing and a Power BI dashboard for visualization. The goal is to provide insights into accident trends, causes, and contributing factors.

## Power BI Dashboard

Here are the two pages of the interactive Power BI dashboard, providing a visual summary of the road accident data.

### Dashboard Page 1

![Dashboard Page 1]([https://private-us-east-1.manuscdn.com/sessionFile/QafYxSHokfV28hAoB7rjVi/sandbox/22aCKO5Ru0ffSxnzhr2VlT-images_1754258540607_na1fn_L3RtcC9wZGZfaW1hZ2VzL3JvYWRwb3dlcmJpLzAwMQ.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvUWFmWXhTSG9rZlYyOGhBb0I3cmpWaS9zYW5kYm94LzIyYUNLTzVSdTBmZlN4bnpocjJWbFQtaW1hZ2VzXzE3NTQyNTg1NDA2MDdfbmExZm5fTDNSdGNDOXdaR1pmYVcxaFoyVnpMM0p2WVdSd2IzZGxjbUpwTHpBd01RLndlYnAiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=AAZLabX0QPDBHzwuJVPSxruLDKi9o1N27Om1g8medRi~ZJtGWtU089PRVNb0pGXOQYHydUrO1sXrcgni4SJGH4Gh7DaFr18aFr8ZAtelKZUvMnZNhX24kU5ugKxsdRASALzSgnOQWrQxUMcu~so2nLzAnGVjJMmjTa4winT5CWHt~wq-yChhZDA2dKCI-W391HTNMRVIfSTc1bB1t7K7-wLrkg~e9nNgXcAyxXiSXIzjLZCFGWOqUq068y3iRPhAFaJLpa5lUfq~1YeEIpGuSrtKeWE45UQM5rpdFbaVHYurZFKK-9JBhTEmJG2zI4qT9LmYs76SmhkzsfXGlRBAuw__](https://raw.githubusercontent.com/aliisnetalive/Road-Accident-Analysis/refs/heads/main/001.webp))

### Dashboard Page 2

![Dashboard Page 2](https://private-us-east-1.manuscdn.com/sessionFile/QafYxSHokfV28hAoB7rjVi/sandbox/22aCKO5Ru0ffSxnzhr2VlT-images_1754258540607_na1fn_L3RtcC9wZGZfaW1hZ2VzL3JvYWRwb3dlcmJpLzAwMg.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvUWFmWXhTSG9rZlYyOGhBb0I3cmpWaS9zYW5kYm94LzIyYUNLTzVSdTBmZlN4bnpocjJWbFQtaW1hZ2VzXzE3NTQyNTg1NDA2MDdfbmExZm5fTDNSdGNDOXdaR1pmYVcxaFoyVnpMM0p2WVdSd2IzZGxjbUpwTHpBd01nLndlYnAiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=i1b5LAAdmQgazJzt78diLkSjReSKX94cjG-xGEVafCA8oCVfezWZaBYMKv6KArQQ10tsb~TIG5N2iNJWz1BD-lC0jJ3SQVSsC477HLepmYddMYz3A2E4e5OYAxkDA4ZLROb-fO~jRaQf4~9mHyuT-yZMN90mCJXSZVbkozGYWaVaw8wJM6Mwh0BrRwKAlZVfyTUdFkocHhv07jG27O58k-zXT0cVuM81gJQErEsLWjyQSOuGGZMPmzHSSEFvgcFG0CYeW~5OKs8uARcld7gORDVwNRZH3GkJ4OkAHvsSudpVWnTiNGjNie~v2uQi4N8KUxx1WriLKC0wcmklClILzA__)

## Jupyter Notebook Analysis

The `road(3).ipynb` Jupyter Notebook performs the following steps:

### 1. Data Loading and Initial Inspection

The notebook starts by loading the `road_accident_data.xlsx` file into a pandas DataFrame. It then displays the first few rows of the DataFrame and provides a summary of its structure and data types.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_excel(\'road_accident_data.xlsx\')

print(df.head())
print(df.info())
print(df.describe())
```

### 2. Data Preprocessing

The `Date` column is converted to datetime objects for proper time-series analysis.

```python
df[\'Date\'] = pd.to_datetime(df[\'Date\']).dt.date
```

## Dataset Overview

The `road_accident_data.xlsx` dataset contains detailed information about road accidents. Key columns include:

- **ID**: Unique identifier for each accident.
- **State**: The state where the accident occurred.
- **Date**: Date of the accident.
- **Day_of_Week**: Day of the week the accident occurred.
- **Time_of_Day**: Time of the day the accident occurred.
- **Weather_Conditions**: Weather conditions at the time of the accident.
- **Road_Conditions**: Road conditions at the time of the accident.
- **Light_Conditions**: Lighting conditions at the time of the accident.
- **Type_of_Road**: Type of road where the accident occurred.
- **Type_of_Junction**: Type of junction where the accident occurred.
- **Type_of_Accident**: Classification of the accident type.
- **Vehicle_Type**: Type of vehicle involved in the accident.
- **Driver_Age_Group**: Age group of the driver involved.
- **Num_Vehicles_Involved**: Number of vehicles involved in the accident.
- **Num_Casualties**: Number of casualties in the accident.
- **Speed_Limit**: Speed limit on the road section.
- **Distance_to_Nearest_Hospital**: Distance to the nearest hospital.
- **Distance_to_Nearest_Police_Station**: Distance to the nearest police station.
- **Visibility**: Visibility conditions.
- **Road_Width**: Width of the road.
- **Road_Surface_Friction_Coefficient**: Friction coefficient of the road surface.
- **Vehicle_Speed**: Speed of the vehicle involved.
- **Time_Taken_for_Emergency_Response**: Time taken for emergency response.

This dataset provides a rich source of information for understanding the various factors contributing to road accidents and can be used to develop strategies for accident prevention and response improvement.




### 3. Data Cleaning and Preprocessing

The data cleaning and preprocessing phase was crucial for ensuring data quality and reliability. The following comprehensive steps were implemented:

#### 3.1 Missing Value Analysis and Treatment

First, missing values were identified across all columns using `df.isnull().sum()`. The analysis revealed missing values in several key columns:
- Weather_Conditions: 149 missing values
- Type_of_Junction: 155 missing values  
- Speed_Limit: 153 missing values
- Road_Width: 157 missing values
- Vehicle_Speed: 177 missing values
- Time_Taken_for_Emergency_Response: 166 missing values

A systematic approach was used to handle missing values based on data type:

```python
for column in df.columns:
    if df[column].dtype in ['float64', 'int64']:
        df[column] = df[column].fillna(df[column].mean())
    else:
        df[column] = df[column].fillna(df[column].mode()[0])
```

This approach fills numerical columns with their mean values and categorical columns with their mode (most frequent value), ensuring that the imputation maintains the statistical properties of the data.

#### 3.2 Duplicate Removal

Duplicate entries were identified and removed to ensure data integrity:

```python
df = df.drop_duplicates()
```

This step ensures that each accident record is unique and prevents any bias that might arise from duplicate entries in the analysis.

#### 3.3 Outlier Detection and Removal

To improve data quality and model performance, outliers were identified and removed using the Interquartile Range (IQR) method:

```python
for column in df.select_dtypes(include=['float64', 'int64']).columns:
    Q1 = df[column].quantile(0.25)
    Q3 = df[column].quantile(0.75)
    IQR = Q3 - Q1
    lower_bound = Q1 - 1.5 * IQR
    upper_bound = Q3 + 1.5 * IQR
    df = df[(df[column] >= lower_bound) & (df[column] <= upper_bound)]
```

This method removes data points that fall outside 1.5 times the IQR from the first and third quartiles, effectively eliminating extreme outliers that could skew the analysis.

#### 3.4 Data Export

After cleaning, the processed dataset was saved for further analysis:

```python
df.to_csv("done_road_accident_data.csv", index=False)
```

#### 3.5 Correlation Analysis

A correlation heatmap was generated to understand relationships between numerical variables:

```python
df_numeric = df.select_dtypes(include=['int64', 'float64'])
corr = df_numeric.corr()

plt.figure(figsize=(14, 10))
sns.heatmap(corr, annot=True, fmt='.2f', cmap="crest", square=True)
plt.title("Correlation Matrix of Numerical Columns")
plt.show()
```

This visualization helps identify potential multicollinearity issues and understand the relationships between different accident factors.



