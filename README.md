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

```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()

```
<img width="1385" height="217" alt="image" src="https://github.com/user-attachments/assets/1c1cfb2a-be34-412e-8fcd-935c2bd52475" />


```

 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')


```
<img width="798" height="479" alt="image" src="https://github.com/user-attachments/assets/efae6e7b-d8f7-4ea5-a581-e4249bca9564" />


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
<img width="683" height="476" alt="image" src="https://github.com/user-attachments/assets/b329e762-9f16-4b38-9cc0-50f2dc4cd141" />


```

plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")

```
<img width="1440" height="600" alt="image" src="https://github.com/user-attachments/assets/0be1bb43-3463-4f79-ac58-a28aab30fc41" />


```

 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()

```
<img width="788" height="473" alt="image" src="https://github.com/user-attachments/assets/f9917626-caf7-49f7-814f-ceb50a215cad" />


```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()

```
<img width="846" height="472" alt="image" src="https://github.com/user-attachments/assets/d3219876-3415-4a1f-bc1a-443296feda68" />


```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="741" height="467" alt="image" src="https://github.com/user-attachments/assets/25e0e3b3-7e5f-4837-b57e-d6e3916cd9b1" />

```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```
<img width="1419" height="588" alt="image" src="https://github.com/user-attachments/assets/a3253314-4ac2-46e7-aae2-c2c11fd04bca" />


```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```
<img width="1095" height="482" alt="image" src="https://github.com/user-attachments/assets/ccd91541-b714-4577-b76a-2ba0dd9beef2" />


```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="942" height="584" alt="image" src="https://github.com/user-attachments/assets/7e1a228a-cae8-4a88-805b-916f375c5718" />


```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="1191" height="559" alt="image" src="https://github.com/user-attachments/assets/fcf8cd94-bb90-4286-952f-6929a50bfc0c" />



# Result:
 Include your result here
