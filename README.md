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
<img width="1510" height="286" alt="image" src="https://github.com/user-attachments/assets/437ebaeb-fef9-4139-957d-9ac2f74cb57a" />

# 1.Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="749" height="588" alt="image" src="https://github.com/user-attachments/assets/e19f6ddd-4200-4ccf-bb52-c0fb93df5241" />

# 2.Multi Line Plot
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
<img width="754" height="566" alt="image" src="https://github.com/user-attachments/assets/81b437f1-e25b-4b6b-9c21-1224e54cc33b" />

# TO VISUALIZE RELATIONSHIPS
# 1.Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="1681" height="721" alt="image" src="https://github.com/user-attachments/assets/0b1a15c0-366d-4fca-b5eb-39ab44ab80f3" />

# 2.Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="1443" height="603" alt="image" src="https://github.com/user-attachments/assets/7ece16e0-6979-416c-a7e0-55fdad0d8c46" />

# 3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="1328" height="604" alt="image" src="https://github.com/user-attachments/assets/9ed6cf48-2e34-425a-ab41-fc2a11af0276" />

# TO CAPTURE DISTRIBUTIONS
# 1.Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="1005" height="588" alt="image" src="https://github.com/user-attachments/assets/9abec3f7-def3-4927-b507-e0881289aee5" />

# 2.Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="1789" height="729" alt="image" src="https://github.com/user-attachments/assets/e20967f5-4e28-450c-952e-4ed55789817d" />

# 3.Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="1072" height="600" alt="image" src="https://github.com/user-attachments/assets/2794a31a-cf35-4824-b5ed-d841891258db" />

# 4.Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="1303" height="720" alt="image" src="https://github.com/user-attachments/assets/f92a7451-75fe-47ea-895d-7efa16374cbe" />

# 5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="1360" height="647" alt="image" src="https://github.com/user-attachments/assets/4f444efe-5cf6-418a-bbca-a38d2957d610" />

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
