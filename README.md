# TASK2-DATA-MANIPULATION-WITH-PANDAS-
This task involves using the Pandas library to manipulate data 


import pandas as pd

# Step 2: Load CSV file into DataFrame
df = pd.read_csv('data.csv')

# Step 3: Explore and understand the data
print(df.head())

print(df.info())

print(df.describe())

# Step 4: Filtering data based on conditions
filtered_df = df[df['age'] > 30]
female_df = df[df['gender'] == 'Female']

# Step 5: Handling missing values
df.dropna(inplace=True)
df['age'].fillna(df['age'].mean(), inplace=True)

# Step 6: Calculating summary statistics
mean_age = df['age'].mean()
median_income = df['income'].median()
total_sales = df['sales'].sum()

# Optional Step 7: Exporting DataFrame to CSV
df.to_csv('modified_data.csv', index=False)
