# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

### Import required libraries 

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1334" height="319" alt="image" src="https://github.com/user-attachments/assets/201320e7-a5fd-4c81-b288-95a7e68a9794" />

### 1.Line Plot

```python
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="1050" height="572" alt="image" src="https://github.com/user-attachments/assets/8ed66883-4381-4d52-950e-edd782869a81" />

###  2.Multi Line Plot

```python
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="960" height="584" alt="image" src="https://github.com/user-attachments/assets/75173ccf-ffbf-401d-b98c-5eb35fe9e7bb" />

## TO VISUALIZE RELATIONSHIPS 

###  1.Bar Chart

```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="1391" height="696" alt="image" src="https://github.com/user-attachments/assets/2a701e79-a739-44bf-a44e-7c1bd6a28fb9" />

###  2.Scatter Plot 

```python
sns.scatterplot(x="Age", y="Fare", data=df,color='green')
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="1003" height="534" alt="image" src="https://github.com/user-attachments/assets/870ae2ee-1e63-4102-b7bc-5302b58ac67e" />

### 3.Bubble Chart

```python
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200),color='red')
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="1019" height="538" alt="image" src="https://github.com/user-attachments/assets/97a6641a-f863-4b90-9027-85b7b61c09ec" />

## TO CAPTURE DISTRIBUTIONS

###  1.Histogram

```python
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="967" height="527" alt="image" src="https://github.com/user-attachments/assets/01195f78-d691-42f7-8d75-a56619a75598" />

###  2.Box Plot

```python
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="1385" height="660" alt="image" src="https://github.com/user-attachments/assets/0a2f575c-9c12-4ddc-890a-9baeaf119fe7" />

### 3.Violin Plot

```python
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="980" height="541" alt="image" src="https://github.com/user-attachments/assets/a1a3fef5-4956-447b-8d57-2fe4fbedf09b" />

### 4.Density Plot

```python
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="909" height="656" alt="image" src="https://github.com/user-attachments/assets/31e25697-8311-483d-a3e7-112aae2ea2db" />

###  5.Heatmap

```python
num= df.select_dtypes(include=['float64', 'int64'])
cor_mat= num.corr()
sns.heatmap(cor_mat, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="921" height="579" alt="image" src="https://github.com/user-attachments/assets/0f5e51bd-9579-43cb-84ad-98d85a9096c2" />

# Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
