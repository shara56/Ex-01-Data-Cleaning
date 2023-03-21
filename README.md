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
import pandas as pd
df=pd.read_csv("/content/Loan_data (1).csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```
# OUPUT
### DATA:
![image](https://user-images.githubusercontent.com/113497104/226519798-41a6cc7a-26a4-4290-bad3-4205968d4262.png)
### NON NULL BEFORE:
### df.info:
![df info after (1)](https://user-images.githubusercontent.com/113497104/226525466-5f304456-babf-4349-ab11-23e927d77059.jpg)
### MODE:
![modeee](https://user-images.githubusercontent.com/113497104/226526384-f82bc49c-330f-4926-82ad-fab8a12bf181.jpg)
### MEAN:
![MEAN](https://user-images.githubusercontent.com/113497104/226526448-c9dd5ff2-e468-4a72-8a17-395002eda12d.jpg)
### MEDIAN:
![median](https://user-images.githubusercontent.com/113497104/226527351-e410e78c-50fa-48cb-9af9-6d8207175d23.jpg)
### NON NULL AFTER:
### df.info:
![df info after (3)](https://user-images.githubusercontent.com/113497104/226526831-94c2dc0c-6ee0-4d6f-9228-7bfd9e5b9ae4.jpg)
### df.isnull().sum():
![df.isnull()  (1)](https://user-images.githubusercontent.com/113497104/226527136-06ecd7ec-c93f-4174-84ce-1247d0340b16.jpg)
### RESULT:
Thus,the given data is read,cleared and the cleaned data is saved into the file.





