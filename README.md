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
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/186fe4ad-7a71-41fd-89a5-7dec67658e91)


```
df=sns.load_dataset("tips")
df
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/7e032dab-b465-4c37-93a2-31a5a45e05a7)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/a59400d6-2620-46f1-bc89-1c41f26cb580)

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-line Plot")
plt.xlabel('X Label')
plt.ylabel('Y Label')
```

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/dc819923-bb03-415a-b541-f3c56dfe4993)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip = tips.groupby('time')['tip'].mean()
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip', width=0.4)

plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/0ddec754-f4e8-45d4-b1de-42c3bd0ab7f9)

```
years=range (2000, 2012)
apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/eb832361-8868-406f-b112-b1c714c566b8)

```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/edd97515-2c0f-4b47-b3ad-5c34ee0a382c)

```
import seaborn as sns
# Load the tips dataset
tips = sns.load_dataset('tips')
# Scatter plot of total bill vs. tip amount
sns.scatterplot(x= 'total_bill', y='tip', hue='sex',data=tips)
# Set labels and title
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/3b66d58b-7df1-4c0a-a53b-a22b63d33d45)

```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)
marks
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/64d3f2ab-36ae-42bf-8a8c-42507f5f79aa)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
# Add labels and title
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/69107b19-bf8c-4f2e-84f7-afab5549376a)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/471e06a4-5d45-4a37-8d79-2f5560e60eaf)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/78b67313-9f6c-4f7d-b0cc-1ab2ca64ffd1)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/5b836d51-98f7-4393-a8ae-2aa7766635a7)

```
sns.histplot(data=marks, bins=10, kde=True, stat='count', cumulative=False, multiple='stack', element='bars', palette='Set1', shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of students Marks')
```
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/3d7e742b-fe5e-4036-96d5-7abedfb1318e)
![image](https://github.com/silambarasan2004/EXNO-6-DS/assets/119559917/dea708a4-7e89-4a71-aba1-f4c616860c58)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
