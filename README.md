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
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/e5724636-9da1-4aaa-8656-952eb340e1bd)
```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex", linestyle="solid", legend="auto", palette="Set1")
```
![image](https://github.com/user-attachments/assets/6004686d-affe-4f14-b41b-08c59cafadd1)
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset("tips")
avg_total_bill=tips.groupby("day") ["total_bill"].mean()
avg_tip=tips.groupby("day")["tip"].mean()
```
![image](https://github.com/user-attachments/assets/27f43ee9-5b11-4c60-b120-1b2a205b9a1a)
```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index, avg_total_bill, label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill, label="Tip")
plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/5ae4406b-b7be-4787-9a91-d07e2c4b37a5)
```
avg_total_bill=tips.groupby('time') ['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
```
![image](https://github.com/user-attachments/assets/29837674-c48f-4b1e-8459-2f1822e57032)
```
p1=plt.bar(avg_total_bill.index,avg_total_bill, label="Total Bill",width=0.4)
p2=plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label="Tip", width=0.4)
plt.xlabel("Time of the day")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Time of the Day")
plt.legend()
```
![image](https://github.com/user-attachments/assets/9614163d-6e00-4322-81a0-9707a2227940)
```
df=sns.load_dataset("tips")
sns.barplot(x="day",y="total_bill", hue="sex", data=df,palette='Set3')
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
```
![image](https://github.com/user-attachments/assets/107a1023-251b-4a49-af6f-d2836b0bca62)
```
df=sns.load_dataset("tips")
sns.scatterplot(x="total_bill",y="tip", hue="sex", data=df, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Tip")
plt.title("Scatter Plot of Total Bill vs Tip Amount")
```
![image](https://github.com/user-attachments/assets/d48463be-f4d9-4409-83a8-8e8a6b9c0233)
```
sns.histplot(data=df,x="total_bill", hue="smoker", kde=True, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Gender")
```
![image](https://github.com/user-attachments/assets/bfe09d30-9c31-469a-be74-d4a2a6d1e4c1)
```
df=sns.load_dataset('tips')
sns.boxplot(x='day', y='total_bill', hue='sex', data=df, palette='Set2')
```
![image](https://github.com/user-attachments/assets/35237b99-7f74-4064-9e2d-b9c457e1f659)
```
sns.boxplot (x="day",y="total_bill", hue="smoker",
data=df, linewidth=2,width=0.6,
fliersize=7, flierprops={"marker":"o", "markerfacecolor":"grey"},
boxprops={"facecolor":"red", "edgecolor":"black"},
whiskerprops={"color":"darkblue", "linestyle":"--", "linewidth":2},
capprops={"color":"darkblue","linestyle":"-","linewidth": 2},palette="Set1")
```
![image](https://github.com/user-attachments/assets/b65d3988-4171-48b9-a59a-79f496ae197b)
```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette='Set1',inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/7123e2d8-1e57-48e8-aa9e-632d8f0c4426)
```
sns.set(style="whitegrid")
tip = sns.load_dataset('tips')
sns.violinplot(x = 'day', y = 'tip', data = tip, palette="Set2")
```
![image](https://github.com/user-attachments/assets/0a22ed7e-4464-49a0-b277-0d43727a107f)
```
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"], palette="Set1")
```
![image](https://github.com/user-attachments/assets/7c0a2d2e-898a-4ced-a3d3-544f6d8773da)
```
sns.set(style="whitegrid")
tips = sns.load_dataset("tips")
sns.violinplot(x="tip", y="day", data=tip, palette="rainbow")
```
![image](https://github.com/user-attachments/assets/f7ee158f-aa32-4917-a60c-bef71f8ab8b9)
```
sns.kdeplot(data=tips,x='total_bill', hue='time', multiple="layer", linewidth=3, palette='Set2', alpha=0.8)
```
![image](https://github.com/user-attachments/assets/f8191ef2-2675-4cde-86cb-ee4055a41438)
```
sns.kdeplot(data=tips,x='total_bill', hue='time', multiple='stack', linewidth=3, palette='Set3',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/23702bdc-72e7-4b21-b9e7-ba295acca950)
```
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='fill', linewidth=3, palette='Set1', alpha=0.8)
```
![image](https://github.com/user-attachments/assets/37c01168-1fbf-43e0-84dc-73f725b191c4)
```
tip = sns.load_dataset('tips')
num=tips.select_dtypes (include=['float64', 'int64']).columns
corr=tips[num].corr()
sns.heatmap (corr, annot=True, cmap="YlGnBu")
```
![image](https://github.com/user-attachments/assets/4e82a490-783c-4930-81e6-3d72016c9145)
```
sns.heatmap(corr,cmap="YlGnBu")
```
![image](https://github.com/user-attachments/assets/98bf6f2a-28f9-441b-90e9-8762a3aa57f8)

# Result:
Thus the data visualization techniques of seaborn has been implemented
