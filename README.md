# Ex-01_DS_Data_Cleansing
# AIM

To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation

Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM

## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
#data_set

import pandas as pd
df = pd.read_csv("Data_set.csv")
df.head(5)
df.info()
df.isnull().sum()
#MODE:
df['show_name'] = df['show_name'].fillna(df['show_name']).mode()[0]
df['aired_on'] = df['aired_on'].fillna(df['aired_on']).mode()[0]
df['original_network'] = df['original_network'].fillna(df['original_network']).mode()[0]
#MEAN:
df['rating'] = df['rating'].fillna(df['rating']).mean()
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank']).mean()
#FORWARD METHOD:
df['watchers'] = df['watchers'].fillna(method='ffill')
df.isnull().sum()

#loan_data

import pandas as pd
df = pd.read_csv("/content/Loan_data.csv")
df.head(5)
df.info()
df.isnull().sum()
#MODE:
df['Gender'] = df['Gender'].fillna(df['Gender'].mode()[0])
df['Self_Employed'] = df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Dependents'] = df['Dependents'].fillna(df['Dependents'].mode()[0])
#MEAN and MEDIAN:
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].median())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].mean())
df.isnull().sum()
```
# OUTPUT:
![o1](https://user-images.githubusercontent.com/118541897/226187157-dcf13c93-ba3e-4387-9365-55eafa3b7217.png)
![o2](https://user-images.githubusercontent.com/118541897/226187170-21661916-c2f7-41c5-a83c-73cfc3a4b888.png)
![o3](https://user-images.githubusercontent.com/118541897/226187177-fc8f37db-c84f-4d82-b17c-0676cc426b08.png)
![o4](https://user-images.githubusercontent.com/118541897/226187187-554fe808-01ca-4585-8e63-e6353c781f99.png)
![o5](https://user-images.githubusercontent.com/118541897/226187247-c3a414d4-998a-49e6-bad1-d7f3e6dec54a.png)
![o6](https://user-images.githubusercontent.com/118541897/226187250-151be34a-70e1-4f97-be71-3dc8bffebe57.png)
![o7](https://user-images.githubusercontent.com/118541897/226187271-51afb3e7-d69b-46cb-b368-83d39d50da4d.png)
![o8](https://user-images.githubusercontent.com/118541897/226187277-54221878-7133-4ce4-8efb-debbecd25006.png)
![o9](https://user-images.githubusercontent.com/118541897/226187285-362f3a67-6899-4dca-872f-4c8e46c575db.png)
![o10](https://user-images.githubusercontent.com/118541897/226187296-24c30b2e-34ea-4c58-8f27-2def581c04f4.png)

# RESULT:

Thus the given data is read,cleansed and cleaned data is saved into the file.
