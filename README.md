# Karan
import pandas as pd
df = pd.read_csv('Hospitals.csv')
df.head()
df.isnull().sum()
mean_df = df['Number of hospitals in public sector'].mean
df['Number of hospitals in public sector'] = df['Number of hospitals in public sector'].fillna(mean_df)
df.isnull().sum()
mean_col2 = df['Number of hospitals in private sector'].mean
df['Number of hospitals in private sector'] = df['Number of hospitals in private sector'].fillna(mean_col2)
df.isnull().sum()
mean_col3 = df['Total number of hospitals (public+private)'].mean
df['Total number of hospitals (public+private)'] = df['Total number of hospitals (public+private)'].fillna(mean_col3)
df.isnull().sum()
