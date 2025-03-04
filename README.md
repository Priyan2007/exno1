# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
df=pd.read_csv("/content/SAMPLEIDS.csv")
df
```
![image](https://github.com/user-attachments/assets/f586e4fe-b968-455e-bfeb-9bc26cd9d06a)
```
df.isnull().sum()
```
![image](https://github.com/user-attachments/assets/b4179e09-e8b6-4eb4-8358-171bfb99bc2d)
```
df.isnull().any()
```
![image](https://github.com/user-attachments/assets/c70e44e5-45f6-4f55-916d-7d4ed62a1db3)
```
df.dropna()
```
![image](https://github.com/user-attachments/assets/4914bf38-039f-4b1f-89e6-6e079cbd4105)
```
df.fillna(0)
```
![image](https://github.com/user-attachments/assets/e83389dd-ec1a-4b34-aaa3-7eb5a8914019)
```
df.fillna(method='ffill')
```
![image](https://github.com/user-attachments/assets/81842716-1fb6-42d7-a1ad-6270030f5f21)
```
df.fillna(method='bfill')
```
![image](https://github.com/user-attachments/assets/e5e09564-d4cf-42de-9cc3-664c4d3f85d7)
```
df_dropped = df.dropna()
df_dropped
```
![image](https://github.com/user-attachments/assets/9fc67c07-1cdc-4dfd-a135-4c0d391b3440)
```
df.fillna({'GENDER':'MALE','NAME':'SRI','ADDRESS':'POONAMALEE','M1':98,'M2':87,'M3':76,'M4':92,'TOTAL':305,'AVG':89.999999})
```
![image](https://github.com/user-attachments/assets/48c0b14e-e8d3-4072-aa8e-021cfde991d7)
