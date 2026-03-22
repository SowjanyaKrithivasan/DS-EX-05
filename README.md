## EX-NO 05-DATA VISUALIZATION USING MATPLOT LIBRARY

### Aim:
  To Perform Data Visualization using matplot python library for the given datas.

### EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

### Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

### Coding and Output:
### import libraries and style
```
# Step 1: Include the necessary libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
# Style
sns.set(style="whitegrid")
```
### Step2: Read dataset
```
# Step 2: Read the dataset
df = sns.load_dataset("titanic") # You can also use: pd.read_csv("your_path.csv")
df.head()
```
<img width="1077" height="226" alt="image" src="https://github.com/user-attachments/assets/d7474e29-b24a-430d-9645-627713a1d888" />

### Step3: Visualize missing data
```
# Step 3: Visualize missing data
plt.figure(figsize=(10,6))
sns.heatmap(df.isnull(), cbar=False, cmap='viridis', yticklabels=False)
plt.title("Missing Values Heatmap")
plt.show()
```
<img width="794" height="621" alt="image" src="https://github.com/user-attachments/assets/b40d175b-8193-49a8-9562-1deca64a6951" />

### Step 4: Countplot - Categorical Feature Visualization
```
# Step 4: Countplot - Categorical Feature Visualization
plt.figure(figsize=(8,5))
sns.countplot(x='sex', data=df, palette='pastel')
plt.title("Passenger Count by Gender")
plt.show()
```
<img width="705" height="479" alt="image" src="https://github.com/user-attachments/assets/63efb8fa-20e6-4ac3-a825-a6d05f51b871" />

###  Countplot - Survival vs Class
```
# Countplot - Survival vs Class
plt.figure(figsize=(8,5))
sns.countplot(x='survived', hue='class', data=df, palette='Set2')
plt.title("Survival Count by Passenger Class")
plt.xlabel("Survived (0 = No, 1 = Yes)")
plt.ylabel("Count")
plt.legend(title="Class")
plt.show()
```
<img width="705" height="479" alt="image" src="https://github.com/user-attachments/assets/fb32d945-dfa5-4689-9f82-e38204d1a436" />

### Step 5: Histogram - Continuous Data Distribution
```
# Step 5: Histogram - Continuous Data Distribution
plt.figure(figsize=(8,5))
sns.histplot(data=df, x='age', kde=True, bins=30, color='skyblue')
plt.title("Age Distribution of Passengers")
plt.xlabel("Age")
plt.ylabel("Frequency")
plt.show()
```
<img width="696" height="479" alt="image" src="https://github.com/user-attachments/assets/f8f47819-568d-4707-93c5-c8505d44f8d1" />

### Step 6: Boxplot - Outlier Detection and Comparison
```
# Step 6: Boxplot - Outlier Detection and Comparison
plt.figure(figsize=(8,5))
sns.boxplot(x='pclass', y='age', data=df, palette='muted')
plt.title("Age Distribution across Passenger Classes")
plt.xlabel("Passenger Class")
plt.ylabel("Age")
plt.show()
```
<img width="696" height="479" alt="image" src="https://github.com/user-attachments/assets/fa7912b4-b30d-4274-948f-935576d2a8b8" />

### Step 7: Pairplot - Multiple Feature Interactions
```
 #Step 7: Pairplot - Multiple Feature Interactions
sns.pairplot(df[['age', 'fare', 'pclass', 'survived']], hue='survived', palette='coolwarm')
plt.suptitle("Pairwise Relationships", y=1.02)
plt.show()
```
<img width="829" height="769" alt="image" src="https://github.com/user-attachments/assets/6d3f6711-79e0-412c-95a1-94070345c94d" />

### Step 8: Correlation Heatmap - Numeric Feature Correlation
```
# Step 8: Correlation Heatmap - Numeric Feature Correlation
plt.figure(figsize=(10,7))
corr_matrix = df.select_dtypes(include=np.number).corr() # Select only numeric columns
sns.heatmap(corr_matrix, annot=True, cmap='Blues', linewidths=0.5)
plt.title("Correlation Matrix Heatmap")
plt.show()
```
<img width="783" height="609" alt="image" src="https://github.com/user-attachments/assets/1df8c170-596b-4751-9296-b865c2799e16" />

# Result:
 Thus, the program to Perform Data Visualization using matplot python library for the given data was
implemented.

