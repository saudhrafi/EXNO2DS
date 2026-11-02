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

```
import pandas as pd
df = pd.read_csv("C:/Users/admin/Desktop/Intro to DS/titanic_dataset.csv")
df
```

<img width="1136" height="383" alt="image" src="https://github.com/user-attachments/assets/18c2c429-29fe-4d4e-b8f1-a0ae82f5b708" />


```
df.info()
```

<img width="401" height="427" alt="image" src="https://github.com/user-attachments/assets/24a7c6f7-8bf0-4a86-87f3-48963f903e49" />


```
df.describe()
```
<img width="785" height="316" alt="image" src="https://github.com/user-attachments/assets/0c2b08ff-e6c4-4eb0-8b66-00003fe806e6" />


```
df.shape
```
<img width="228" height="80" alt="image" src="https://github.com/user-attachments/assets/4aba84d2-ecee-44c1-8cef-d785ee463e34" />

```
df.dtypes
```
<img width="260" height="302" alt="image" src="https://github.com/user-attachments/assets/44f57bf8-9357-4f3b-9681-943b0b89636b" />

```
df.value_counts()
```
<img width="1217" height="522" alt="image" src="https://github.com/user-attachments/assets/afc56e4d-4aeb-4ff9-88d5-581254ff4462" />

```
df.nunique()

```

<img width="263" height="302" alt="image" src="https://github.com/user-attachments/assets/07396693-d50f-4d80-981b-1f649ca13433" />

```
df["Survived"].value_counts()
```

<img width="311" height="133" alt="image" src="https://github.com/user-attachments/assets/ee703b6b-5f88-430a-b7b6-5ef467077799" />


```
import seaborn as sns
sns.boxplot(data=df, x ='Fare')
```

<img width="642" height="562" alt="image" src="https://github.com/user-attachments/assets/69119466-911b-4c80-9581-c8a9d725b11f" />


```
sns.countplot(data=df, x = 'Survived')
```


<img width="797" height="568" alt="image" src="https://github.com/user-attachments/assets/8f704a1c-bdca-41ae-a838-cb2c6b492eb0" />

```
sns.histplot(data=df,x="Age")
```

<img width="837" height="566" alt="image" src="https://github.com/user-attachments/assets/1bd37f58-6e8e-43ad-a188-dc40e19da83e" />

```
df.rename(columns={'Sex':'Gender'},inplace=True)
print(df)
```
<img width="1132" height="423" alt="image" src="https://github.com/user-attachments/assets/2a2c7495-e1f7-4710-a91d-bc500a75ff2b" />

```
sns.barplot(x=df["Survived"] , y=df["Age"], data=df)
```

<img width="795" height="567" alt="image" src="https://github.com/user-attachments/assets/0b6c1a9e-70d8-43c9-a125-bdd328e77168" />


```
sns.scatterplot(x=df["Survived"], y=df["Age"],data=df) 
```

<img width="808" height="560" alt="image" src="https://github.com/user-attachments/assets/7334bc30-bcec-43dc-b067-0d33a35b3d3c" />


```
sns.catplot(x='Gender', col='Survived', kind='count',data=df)
```


<img width="1235" height="617" alt="image" src="https://github.com/user-attachments/assets/d7ad7e0c-3b9c-4619-b7ab-57a1e52c3aac" />


```
df.boxplot(column="Age" ,by='Survived')
```


<img width="756" height="592" alt="image" src="https://github.com/user-attachments/assets/fa806d3d-70d5-4683-b693-14370f1a8a42" />


```
sns.boxplot(x='Pclass', y='Age', hue='Gender', data=df)      

```
<img width="855" height="580" alt="image" src="https://github.com/user-attachments/assets/f83ee985-0689-46db-96dc-f9671d7299b0" />

```
sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")
```
<img width="1211" height="603" alt="image" src="https://github.com/user-attachments/assets/e34296fb-5993-4f2f-b231-1822846cbff7" />

```
sns.heatmap(df.corr(),annot=True)
```
<img width="747" height="647" alt="629783406-e661cf48-51de-4d17-b07c-e2a49827364d" src="https://github.com/user-attachments/assets/6a79fe00-8439-45d9-9496-1a723384693c" />


# RESULT:
Successfully performed Exploratory Data Analysis (EDA) by handling missing values, detecting and removing outliers, analyzing categorical and numerical data, and visualizing relationships using countplot, displot, crosstab, and heatmap.
