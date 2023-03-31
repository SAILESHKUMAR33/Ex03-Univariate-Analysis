# Ex03-Univariate-Analysis
AIM:

To perform Univariate EDA on the given data set

Explanation:

Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis

ALGORITHM:

STEP 1:

Import the built libraries required to perform EDA and outlier removal.

STEP 2:

Read the given csv file

STEP 3:

Convert the file into a dataframe and get information of the data.

STEP 4:

Return the objects containing counts of unique values using (value_counts()).

STEP 5:

Plot the counts in the form of Histogram or Bar Graph.

STEP 6:

Use seaborn the bar graph comparison of data can be viewed.

STEP 7:

Save the final data set into the file

PROGRAM:
Name:saileshkumar A
Reg.No:212222230126

import pandas as pd
import numpy as np
import seaborn as snb
df = pd.read_csv('/content/SuperStore.csv')
df.head(10)
df.info()
df.describe()
df.dtypes
df.isnull().sum()
df['Postal Code'] = df["Postal Code"].fillna(df['Postal Code'].mode()[0])
df.isnull().sum()
df['Postal Code'].value_counts()
snb.boxplot(x="Sales",data=df)
snb.countplot(x="Sales",data=df)
snb.distplot(df["Sales"])
snb.histplot(x="Sales",data=df)
df.skew()
df.kurtosis()
snb.histplot(x="Postal Code",data=df)
snb.displot(x="Postal Code",data=df)
snb.boxplot(x="Postal Code",data=df)
snb.boxplot(x="Row ID",data=df)
snb.histplot(x="Ship Mode",data=df)
snb.countplot(x="Category",data=df)

OUTPUT:
![image](https://user-images.githubusercontent.com/113497410/229032021-382a0d91-e961-4e8b-b908-b15cda848f53.png)
Displaying information about Dataset:

![image](https://user-images.githubusercontent.com/113497410/229032137-52639cb7-ff29-4e74-9403-1c7ea095f209.png)
![image](https://user-images.githubusercontent.com/113497410/229032212-81124a02-3c1a-469d-97b0-c758b15512be.png)


Finding null values and cleaning it:

![image](https://user-images.githubusercontent.com/113497410/229032274-740437ea-d63a-4ebf-a967-feef2c02ae61.png)

Value counts of "Postal Code":

![image](https://user-images.githubusercontent.com/113497410/229032353-99d0f078-2103-4a56-8e58-1d77f56bad80.png)

Distribution of Data:

![image](https://user-images.githubusercontent.com/113497410/229032397-e8973d5f-e015-4c48-add9-59edbb31fe85.png)

Univariate Analysis:

![image](https://user-images.githubusercontent.com/113497410/229032446-ce14ffdc-4baf-4c73-8518-56f3ec15b092.png)

![image](https://user-images.githubusercontent.com/113497410/229032483-19456d1b-edf2-41bf-9573-50b93d269b39.png)
![image](https://user-images.githubusercontent.com/113497410/229032928-b75d1151-0cf7-440b-9bc0-a5349bf57ecc.png)
![image](https://user-images.githubusercontent.com/113497410/229032967-643871bd-0967-4f0f-95f5-9089dfa5db71.png)
![image](https://user-images.githubusercontent.com/113497410/229032979-bde605cc-f219-42cd-827d-cee7e8626e2e.png)

RESULT:

Thus the program to perform EDA on the given data set is successfully executed






