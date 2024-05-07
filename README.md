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
![Screenshot 2024-05-04 100012](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/1c8ab253-15f0-4b45-8caa-13ab87b620d0)


```
df=sns.load_dataset("tips")
df
```
![Screenshot 2024-05-04 100022](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/95a2ed6d-ef61-4344-be6d-175b073b5192)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![Screenshot 2024-05-04 100028](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/99b1f75a-f56a-48fe-91c7-4b6d4cca4c62)

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
![Screenshot 2024-05-04 100039](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/adfd7f45-e3a9-4f98-8e45-89bb247187dc)

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
![Screenshot 2024-05-04 100046](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/fd7c2a3a-b168-44b2-8892-0ac6d388adf9)

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
![Screenshot 2024-05-04 100053](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/5c9a4aca-7887-4bab-9bf7-a441a31ed425)

```
years=range (2000, 2012)
apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![Screenshot 2024-05-04 100102](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/6fdee4e0-c832-43c3-9917-afff4e1375f8)

```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![Screenshot 2024-05-04 100109](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/e9a48fc4-a932-4043-87ed-c46d30d52d7c)

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
![Screenshot 2024-05-04 100116](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/3694fb1b-176a-4696-aa5d-c3b1fc7b4260)

```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)
marks
```
![Screenshot 2024-05-04 100123](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/eee0727e-d897-4540-ae5a-83cb6f59b847)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
# Add labels and title
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![Screenshot 2024-05-04 100128](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/98fb5506-36c4-4824-bfdd-7b260a2a2752)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)
```
![Screenshot 2024-05-04 100136](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/29596560-6a54-4051-9c55-0903af5c0665)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![Screenshot 2024-05-04 100142](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/7323ef13-38b2-472b-9146-e68f7f5049df)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```
![Screenshot 2024-05-04 100149](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/322e04f2-b84b-4477-be92-23e22385feac)

```
sns.histplot(data=marks, bins=10, kde=True, stat='count', cumulative=False, multiple='stack', element='bars', palette='Set1', shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of students Marks')
```
![Screenshot 2024-05-04 100157](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/b95a290d-8aa5-421b-910f-a8d05f0db533)
![Screenshot 2024-05-04 100205](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/15ad7faa-d749-4ae6-8540-e56e79949db3)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
