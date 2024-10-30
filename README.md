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
### DEVELOPED BY: V DIVYASHREE
### REGISTER NO: 212223230051
```
import seaborn as sns
import matplotlib.pyplot as plt
```
```
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/0265c41e-e622-425a-b54b-92a16dc2a0a0)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```

![image](https://github.com/user-attachments/assets/b3d13f94-703e-4125-902d-2da434efb124)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
```

![image](https://github.com/user-attachments/assets/989d9b1e-09dd-41af-9cdc-acd6268dff82)

```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Amount Total Bill and Tip by Day')
plt.legend()
```

![image](https://github.com/user-attachments/assets/a99e85ad-25ba-421e-9757-fb28aa4606ca)

```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
```
![image](https://github.com/user-attachments/assets/921a22c0-c7d8-45d1-bcf5-4f2e33f8f004)

```
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip",width=0.4)
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```


```
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
```
![image](https://github.com/user-attachments/assets/688ca9c0-2baa-411f-aeda-75ce4bbe0c25)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![image](https://github.com/user-attachments/assets/b481c943-6566-4f4c-b953-b014cd9e93fd)

```
sns.boxplot(x='day',y='total_bill',hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"pink","edgecolor":"yellow"},
whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```

![image](https://github.com/user-attachments/assets/6e9b0c52-ced1-4640-a461-e6a6ba5c4b2f)


```
df=sns.load_dataset("tips")
```

```
import seaborn as sns

import matplotlib.pyplot as plt
sns.violinplot(x="day", y="total_bill", hue="smoker", data=df, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

![image](https://github.com/user-attachments/assets/e23ed86f-231f-4104-bab8-7c557458c683)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)
```

![image](https://github.com/user-attachments/assets/796aa75b-37be-4c60-aeb3-fd6ecd428e00)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```

![image](https://github.com/user-attachments/assets/47d3db29-9ff5-4463-8d45-c8e6e45cad05)


```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```

![image](https://github.com/user-attachments/assets/d50a0a85-01bd-4a82-81a0-56954c874cbc)

```
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='stack', linewidth=3, palette='Set2', alpha=0.8)
```

![image](https://github.com/user-attachments/assets/c38e2fea-5675-4f38-ac34-b32e907e3747)

```
import numpy as np
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted")
print(data)
```

![image](https://github.com/user-attachments/assets/da7b3f5a-d890-4894-b89a-eccf63b4ff58)


```
hms=sns.heatmap(data=data)
```

![image](https://github.com/user-attachments/assets/61a01f5b-09b2-4450-937f-2a4574615e74)

```
hms=sns.heatmap(data=data,annot=True)
```

![image](https://github.com/user-attachments/assets/34229625-f2e8-49a7-8e55-064ac614ba4a)

```
import numpy as np
df=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted")
print(df)
```

![image](https://github.com/user-attachments/assets/aa02fd09-1647-42e7-82d5-6d15939cf3ad)


```
hms=sns.heatmap(data=df)
```

![image](https://github.com/user-attachments/assets/9a23501d-d3d5-4b10-8be2-3d8d43cb8a54)

```
hms=sns.heatmap(data=df,annot=True)
```

![image](https://github.com/user-attachments/assets/6f8bc912-868f-4a8b-bc88-069d8e1bd284)

```
import seaborn as sns
import numpy as np
import matplotlib.pyplot as plt
```
```
tips=sns.load_dataset("tips")
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()
```
```
sns.heatmap(corr,annot=True,cmap="plasma",linewidths=0.5)
```

![image](https://github.com/user-attachments/assets/de213782-303a-4f3b-a0a1-070507eb9f73)




# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
