# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
# NAME:MAGESHKUMAR U
# REGNO:212224240085

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
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="1233" height="314" alt="image" src="https://github.com/user-attachments/assets/3e077bb2-eb76-48f5-a527-2fea814b9b38" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="695" height="583" alt="image" src="https://github.com/user-attachments/assets/3138e1cd-8542-410c-a070-5df8b14477d7" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="680" height="575" alt="image" src="https://github.com/user-attachments/assets/74cc2e49-e527-453d-9424-2bec690ddcff" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="870" height="621" alt="image" src="https://github.com/user-attachments/assets/dfb9ae28-191d-41f6-a16e-402644f69b80" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```


<img width="732" height="588" alt="image" src="https://github.com/user-attachments/assets/bfadbc3b-f6b8-4bcd-aba4-1ae24dd521c9" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```


<img width="733" height="585" alt="image" src="https://github.com/user-attachments/assets/82955e99-881f-47c3-b8fd-014a00b2785d" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="739" height="576" alt="image" src="https://github.com/user-attachments/assets/ffb15f2c-b3b8-426b-8652-74120409d550" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```


<img width="716" height="631" alt="image" src="https://github.com/user-attachments/assets/f5523305-3b25-4f10-b033-b35890b8bc96" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```


<img width="728" height="590" alt="image" src="https://github.com/user-attachments/assets/f23597db-3b44-43b5-a55f-54555dbe8383" />

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```


<img width="758" height="610" alt="image" src="https://github.com/user-attachments/assets/ae91fff6-2d00-4214-aebe-8f83acac177d" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```


<img width="741" height="627" alt="image" src="https://github.com/user-attachments/assets/34350381-44e4-42f5-a30e-fdc3df7ac0b4" />


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
