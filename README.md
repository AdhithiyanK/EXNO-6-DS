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
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![323212197-18a0f3c8-10a6-42b4-9eb3-45770f741ac3](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/1ec8ed70-3b35-41ad-8f94-bbc736db7452)

```
df = sns.load_dataset("tips")
df
```
![323212387-0124fef5-dcba-4c31-9831-db85384d9c5a](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/ed2268d7-b8c9-4280-8952-b4dfe046104d)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![323212532-1bbe2d28-735c-4114-aff7-9030d334c830](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/d33d691f-ed3d-43ab-bf60-0fac2b5d739f)

```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![323212649-4d6c2a15-2352-4ba4-bd6b-97a54cd93ce7](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/7d629415-e144-4e84-9df4-96bafc0278d3)
```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![323212764-86b30955-7bb2-44af-92d1-39e8be4b56ea](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/e8732863-782e-4bf5-95ba-15809a46f367)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![323212867-27a32e9f-e734-4f47-adf1-bafddba998c3](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/906d6367-98e2-4884-81e3-f990a73dc3fd)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![323213027-31f5b45b-5a80-4259-a259-a4cecee25ee5](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/523857a8-e3db-4056-a6c3-0baa8a8f20f9)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![323213184-359daca3-3920-4c78-b593-7d660c09cc36](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/92c6f26c-7030-4a1e-9679-2488611bce25)

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![323213349-b749f1ee-b0a6-4a67-a340-f9cae8a8290a](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/c2ac4260-4a4f-4c97-9e8b-9ee5b8c5ba51)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![323213630-03dbd087-2a3e-4bfa-8847-bc2e9bbe7cc3](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/5ad0d8bc-c648-4910-a27d-2e306086ac28)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![323213737-090114ac-6d91-4117-80ca-2bb2fe72af26](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/70c18311-c3ea-4c44-afe6-c4f41d59994b)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![323213860-b7984ccc-60c8-4cf2-ba31-0dafe6119b91](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/f88fc29d-fd73-4894-8ddb-c97e3d7fd758)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![323213974-5e149370-320f-4c4b-b6e9-93839011d166](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/7c391581-dfaa-48b7-a609-2468a75274d5)
```
sns.histplot(data = num_var, kde = True)
```
![323214138-39b3d5fa-e8af-45f5-afb2-2875c766a5e6](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/1dbe4d59-a44d-4c99-8ddb-5761714a5b41)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![323214244-e8b91ede-1cc0-4087-beb6-c3c56d8137ee](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/d1534481-eb08-47eb-b9f9-d65b30da3019)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![323214357-c7d0ff3a-e9a0-4369-a9c9-9229d84776c3](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/fcd0de14-31fd-40d7-9c26-774c77dfbe2c)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "lineidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![323214462-dc5777c4-83cf-47d2-ba0c-b6bb81547441](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/e5354042-c53d-44f8-9426-7d61409abd3c)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![323214570-8dec8878-d0bb-46ca-bc17-095aba86cffd](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/a504f568-97d9-4efe-bd6c-009f78567d20)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![323214740-32c63c42-35dc-47df-b851-c13e54c166aa](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/50e79c21-d201-459f-a0d4-287ee775f9e7)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![323214850-bcbe61b9-5739-4853-a186-302272133266](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/c327815e-552f-429b-9198-e2d766d3f5ed)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![323214956-727482e0-5b45-47e4-8542-93ebc9cfb5b7](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/5adc95c4-5e94-48e8-af1b-62e94162fc37)

```
sns.kdeplot(data=mart,x='Age')
```
![323215089-9bb955c9-ba97-48ab-b158-35a44931ccf6](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/280bcae3-9839-47ce-8cfa-e6dfd2bd1e7a)
```
sns.kdeplot(data=mart)
```
![323215191-8cc57d95-8df2-4483-8c98-2edbcfb68b0c](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/882bc16d-8b2e-49e7-99f1-04f8d4f823dc)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![323215343-f56e128b-5393-46e8-acb6-33bfd6fde4a9](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/3558c33e-e50e-4cc6-bc31-fc8ee20cbf9b)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![323215571-4f66d13f-770e-4b17-b29d-74f42cb4395e](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/27587279-8301-4984-aafa-89b38d9489fd)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![323215754-5eba9f52-3c11-4640-b78f-451463d24415](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/fe1d5689-ed74-4f0f-852c-6cc464ddaf7a)
```
hm=sns.heatmap(data=data)
```
![323215874-4bbbf59a-e638-4c7b-bf5c-5298f9bada3b](https://github.com/AdhithiyanK/EXNO-6-DS/assets/121029258/dd007adf-aba9-4a57-9324-a6f15a35f013)

# Result:

Thus, all the data visualization techniques of seaborn has been implemented.
