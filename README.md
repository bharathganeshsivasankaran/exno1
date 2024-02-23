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

### CODING
```
import pandas as pd
df = pd.read_csv("SAMPLEIDS.csv")
print(df)
df.head(5)
df.tail()
df.info()
df.describe()
df.shape
df.isnull().sum()
x=df.dropna(how='any')
x
tot=df.dropna(subset=['TOTAL'],how='any')
tot
df.fillna(value=10)
mn=df.TOTAL.mean()
mn
df.head()
for x in df.index:
  if df.loc[x,"AVG"]>100:
    df.drop(x,inplace=True)
df
```
### OUTPUT

1) Read and display DataFrame

 ![Screenshot 2024-02-23 154427](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/83210521-de97-46a5-95b1-f2c064301dd7)

2) Display head (df.head(5))



![Screenshot 2024-02-23 154438](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/87c0257e-c524-485b-a5a6-9baa293fc21a)


3) Display tail (df.tail())

 ![Screenshot 2024-02-23 154446](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/9b0b2f17-a959-41e4-9bca-ee6f654b5fe3)


4) Info of datafram (df.info())


![Screenshot 2024-02-23 154455](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/ec7bd5fe-3b86-4d53-9515-71b4041cd3cf)


5) Describe about the dataframe (df.describe())


![Screenshot 2024-02-23 154513](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/ce937ba7-cdf3-4d44-8ede-51b5492b4ad8)


6) Shape of the datafram(df.shape)

 ![Screenshot 2024-02-23 154522](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/28309a53-2a60-4fde-af3e-39a3cf58ec94)


7) Checking tha NUll values(df.isnull().sum())

![Screenshot 2024-02-23 154529](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/9382de89-93d8-4f59-921d-604f01176204)


8) Drop the Null values x=df.dropna(how='any')
                        x

![Screenshot 2024-02-23 154543](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/e32d9ebf-149d-4cd7-948f-589322e29cc3)


9) Drop the Null values in Total   tot=df.dropna(subset=['TOTAL'],how='any')
                                   tot


![Screenshot 2024-02-23 154557](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/775a85cf-abc1-4106-b13b-9fdf6f780f4e)


10) FIll the Null values  (df.fillna(0))


![Screenshot 2024-02-23 154620](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/66a7104d-4bcd-4edc-9bcf-32c39d63d1fb)


11) Finding the mean value

![Screenshot 2024-02-23 154629](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/37be209e-75ec-431d-a8e7-8b9ec51e96b2)

12) Fill Null value with Mean value


![Screenshot 2024-02-23 154637](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/6e795ece-b176-403c-aa37-1609581d2294)


13) Final output


![Screenshot 2024-02-23 154648](https://github.com/bharathganeshsivasankaran/exno1/assets/119478098/cdc526d0-5184-48c2-87e3-2104128bedee)


   

# Result
          The data clearning has beeen done successfully.
