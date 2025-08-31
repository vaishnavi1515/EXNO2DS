# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
~~~
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df
~~~
<img width="1508" height="614" alt="image" src="https://github.com/user-attachments/assets/b1c45a40-9654-4cbf-b77b-0038765c108f" />

df.isnull().sum()

<img width="374" height="623" alt="image" src="https://github.com/user-attachments/assets/24ed761d-6982-4e3f-8504-d00aaa8e86e7" />

df.nunique()

<img width="390" height="633" alt="image" src="https://github.com/user-attachments/assets/669b6647-791f-409a-b44f-fca61d42f67a" />

df['Survived'].value_counts()

<img width="414" height="287" alt="image" src="https://github.com/user-attachments/assets/e4d32c9c-06f1-4e9b-9bfb-f1619ddb38f4" />

df.Survived.unique()

<img width="296" height="103" alt="image" src="https://github.com/user-attachments/assets/e56142d6-cb70-442e-a6f3-23ee9f37f65c" />

sns.countplot(x='Gender',hue='Pclass',data=df)

<img width="899" height="644" alt="image" src="https://github.com/user-attachments/assets/94fdd3d5-a2be-48da-ad3d-7bf750a1c015" />

~~~
df.rename(columns={'Sex':'Gender'},inplace=True)
df
~~~
<img width="1531" height="588" alt="image" src="https://github.com/user-attachments/assets/42e9721e-c924-4fca-9bb9-2bfdc95833da" />

sns.catplot(x='Survived',col='Gender',data=df,kind='count')

<img width="1542" height="723" alt="image" src="https://github.com/user-attachments/assets/705e6b7b-41cc-4496-b928-6b98b8aa90ec" />

sns.boxplot(data=df)

<img width="841" height="626" alt="image" src="https://github.com/user-attachments/assets/64c4cb03-46aa-40c2-9af6-541e3f561101" />

df.boxplot(column='Age',by='Pclass')

<img width="798" height="668" alt="image" src="https://github.com/user-attachments/assets/21c5c4dc-06dc-40c4-b863-05e039e9d8c3" />

sns.scatterplot(x='Age',y='Fare',data)

<img width="894" height="632" alt="image" src="https://github.com/user-attachments/assets/8edb9e24-2622-4fd9-a876-0f7cba1e26db" />






# RESULT
    We have performed Exploratory Data Analysis on the given data set successfully


