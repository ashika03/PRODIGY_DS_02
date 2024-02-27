import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

# Load your dataset
df = pd.read_csv(r'C:\Users\Administrator\Document\titanic3.csv')
print(df)

# print summmary of the dataframe
print(df.info())

# print first few rows of the dataframe
print(df.head())

# generate descriptive statistics of the dataframe
print(df.describe())

# print the count of missing values for each column in the dataframe
print(df.isnull().sum())

# create a pairplot and visualize
sns.pairplot(df)
plt.show()

# calculate correlation matrix and visualize
correlation_matrix =df.corr()
sns.heatmap(correlation_matri dataframe,annot=True,cmap='coolwarm')
plt.show

# create countplot
categorical_columns= df.select_dtypes(include='object').columns
for column in categorical_columns:
    sns.countplot(x=column, data=df)
    plt.show()


