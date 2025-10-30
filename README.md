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
<img width="1225" height="202" alt="Screenshot 2025-10-23 235543" src="https://github.com/user-attachments/assets/7220a694-ff0d-4aed-9d56-6d610c2abaef" />

## 1.LINE PLOT
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="616" height="451" alt="Screenshot 2025-10-23 235608" src="https://github.com/user-attachments/assets/d118631f-53de-4a21-a747-9f65c980f341" />

2.MULTI LINE PLOT
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
<img width="622" height="462" alt="Screenshot 2025-10-23 235642" src="https://github.com/user-attachments/assets/0eb6cd7d-425d-4574-b908-edf9d07cc49d" />

# TO VISUALIZE RELATIONSHIPS
## 1.BAR CHART
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="787" height="517" alt="Screenshot 2025-10-23 235705" src="https://github.com/user-attachments/assets/7a5d550c-cb0e-4a1a-80da-a7120df06d8e" />

## 2.SCATTER PLOT
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="704" height="477" alt="Screenshot 2025-10-23 235728" src="https://github.com/user-attachments/assets/12db13cb-9353-45f1-a919-c820b60ce4ab" />

## 3.BUBBLE CHART
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="721" height="463" alt="Screenshot 2025-10-23 235808" src="https://github.com/user-attachments/assets/ca5393d5-f037-4610-8fa9-7ee58af4ed93" />

# TO CAPTURE DISTRIBUTIONS
## 1.HISTOGRAM
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="719" height="465" alt="Screenshot 2025-10-23 235827" src="https://github.com/user-attachments/assets/bb8a8eab-530f-4655-a698-8b538faf44a1" />

## 2.BOX PLOT
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="699" height="501" alt="Screenshot 2025-10-23 235847" src="https://github.com/user-attachments/assets/6dc79df0-ef3b-4c17-912b-1fe6f4fc17f2" />

## 3.VIOLIN PLOT
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="749" height="469" alt="Screenshot 2025-10-23 235912" src="https://github.com/user-attachments/assets/1c9708a2-f65c-47a2-9ec4-b2caa6169613" />

## 4.DENSITY PLOT
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="747" height="470" alt="Screenshot 2025-10-23 235933" src="https://github.com/user-attachments/assets/5398aefe-f066-4f1a-8aef-7850333e94fa" />

## 5.HEATMAP
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="695" height="511" alt="Screenshot 2025-10-23 235952" src="https://github.com/user-attachments/assets/3cb96c01-c085-4900-80f3-16d13a137696" />


# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
