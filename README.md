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
Developed by Mohanish.K
Reference no: 22002294
```
```python
## Data_set Code:
import pandas as pd
df = pd.read_csv("Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name'] = df['show_name'].fillna(df['aired_on'].mode()[0]) 
df['aired_on'] = df ['aired_on'].fillna(df ['aired_on'].mode()[0]) 
df[ 'original_network' ] = df['original_network'].fillna(df['aired_on'].mode()[0]) 
df.head()
df ['rating'] = df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df[ 'watchers']=df["watchers"].fillna (df['watchers'].median()) 
df.head()
df.info()
df.isnull().sum()
```
```python
## Loan_data Code:
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```

# OUTPUT
## DATA - 1 :
![Screenshot (118)](https://user-images.githubusercontent.com/118708024/226648604-135e5ef4-77e7-4867-bd57-8f8083ece8da.png)

## NON NULL BEFORE :
![Screenshot 2023-03-21 203709](https://user-images.githubusercontent.com/118708024/226649645-c795d3e6-81f7-4f98-8657-7e60673e04ea.png)

## MODE :
![Screenshot 2023-03-21 203937](https://user-images.githubusercontent.com/118708024/226650781-693dcd0d-cd48-4c9f-becb-30477e7c0406.png)

## MEAN :
![Screenshot 2023-03-21 203918](https://user-images.githubusercontent.com/118708024/226650567-4776c4ba-6966-405c-b6ec-c0f8347fb04a.png)

## MEDIAN :
![Screenshot 2023-03-21 203959](https://user-images.githubusercontent.com/118708024/226650660-da60bdd3-f670-4e70-95a6-09db8fd54cbe.png)

## NON NULL AFTER:
![Screenshot 2023-03-21 204507](https://user-images.githubusercontent.com/118708024/226652329-0bf93fa7-9463-422c-b0b9-12007bfcb503.png)

## DATA - 2 :
![image](https://user-images.githubusercontent.com/118708024/226658721-34c8ffae-23af-442b-bcad-43474e1de6bd.png)

## NON NULL BEFORE :
![image](https://user-images.githubusercontent.com/118708024/226662409-c9f3e0cd-baf8-4543-9cea-bb1d229d2809.png)

## MODE :
![image](https://user-images.githubusercontent.com/118708024/226660807-d315a496-427a-4cb8-bc07-0bb5fa088643.png)

## MEAN :
![image](https://user-images.githubusercontent.com/118708024/226660379-45293bde-4e68-4048-aacd-c06b8c2fee9a.png)

## MEDIAN :
![image](https://user-images.githubusercontent.com/118708024/226661206-44f017b6-f150-4d69-a347-8b17c6d1604f.png)

## NON NULL AFTER :
![image](https://user-images.githubusercontent.com/118708024/226663564-301e61e3-4fd9-44f9-a2b6-dcb18bda5d1f.png)

# RESULT
Thus the given data is readed and data cleaning is performed on it and the cleaned data is saved into the file.
