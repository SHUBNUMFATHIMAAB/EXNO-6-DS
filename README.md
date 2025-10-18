
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
import seaborn as sns

import matplotlib.pyplot as plt

x=[1,2,3,4,5]

y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)

<img width="638" height="447" alt="image" src="https://github.com/user-attachments/assets/f439fcb2-cd64-44d2-8ed6-6584792d0533" />

df=sns.load_dataset("tips")

df

<img width="552" height="404" alt="image" src="https://github.com/user-attachments/assets/aba5defe-779c-46a4-a828-239e251e3642" />

sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")

<img width="655" height="461" alt="image" src="https://github.com/user-attachments/assets/7ab4cf6e-e848-4997-9d8d-32ff2f703cad" />

x=[1,2,3,4,5]

y1=[3,5,2,6,1]

y2=[1,6,4,3,8]

y3=[5,2,7,1,4]

sns.lineplot(x=x,y=y1)

sns.lineplot(x=x,y=y2)

sns.lineplot(x=x,y=y3)

plt.title('Multi-:Line Plot')

plt.xlabel('X-Label')

plt.ylabel('Y-Label')

<img width="654" height="492" alt="image" src="https://github.com/user-attachments/assets/57670d20-1f20-42b2-9663-bac3bd4ee72c" />

tips=sns.load_dataset('tips')

avg_total_bill=tips.groupby('day')['total_bill'].mean()

avg_tip=tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8,6))

p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')

p2=plt.bar(avg_tip.index,avg_tip,label='Tip')

plt.xlabel('Day of the Week')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Day')

plt.legend()

<img width="859" height="658" alt="image" src="https://github.com/user-attachments/assets/61975ea7-659d-4264-9e76-ee33896e0da4" />

avg_total_bill=tips.groupby('time')['total_bill'].mean()

avg_tip=tips.groupby('time')['tip'].mean()

p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)

p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)

plt.xlabel('Time of Day')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Time of Day')

plt.legend()

<img width="877" height="540" alt="image" src="https://github.com/user-attachments/assets/b0abb00e-9706-4f12-b892-744781aa005f" />

years=range(2000,2012)

apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]

oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]

plt.bar(years,apples)

plt.bar(years,oranges,bottom=apples)

<img width="616" height="445" alt="image" src="https://github.com/user-attachments/assets/4d83ec0e-6f5e-47da-a3d8-925faf46e405" />

import seaborn as sns

dt=sns.load_dataset('tips')

sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')

plt.xlabel('Day of the Week')

plt.ylabel('Total Bill')

plt.title('Total Bill by Day and Gender')

<img width="689" height="484" alt="image" src="https://github.com/user-attachments/assets/02966525-9ce1-42dc-afc6-d822bde9ae14" />

import pandas as pd

tit=pd.read_csv("/content/titanic_dataset (2).csv")

tit

<img width="871" height="750" alt="image" src="https://github.com/user-attachments/assets/a459a460-65fd-4e13-998e-cbf2b9fe0484" />

<img width="830" height="164" alt="image" src="https://github.com/user-attachments/assets/536982c6-cad9-4313-88ef-410e55923525" />

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')

plt.title("Fare of Passenger by Embarked Town")

<img width="882" height="594" alt="image" src="https://github.com/user-attachments/assets/f9a535c9-c772-43b7-958a-c2ba2da45a06" />

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow',hue='Pclass')

plt.title("Fare of Passenger by Embarked Town,Divided by Class")

<img width="834" height="501" alt="image" src="https://github.com/user-attachments/assets/88fc6496-ac1c-48ae-a94d-ffbba4ce1c31" />

tips=sns.load_dataset('tips')

sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)

plt.xlabel('Total Bill')

plt.ylabel('Tip Amount')

plt.title('Scatter Plot of Total Bill vs. Tip Amount')

<img width="697" height="492" alt="image" src="https://github.com/user-attachments/assets/b0601994-de1a-46be-b926-034a7a8eecbb" />

import seaborn as sns

import numpy as np

import pandas as pd

np.random.seed(1)

num_var=np.random.randn(1000)

num_var=pd.Series(num_var,name="Numerical Variable")

num_var

<img width="272" height="446" alt="image" src="https://github.com/user-attachments/assets/acbad605-51f7-4ed2-a11f-23909c766994" />

sns.histplot(data=num_var,kde=True)

<img width="688" height="463" alt="image" src="https://github.com/user-attachments/assets/5f62cf51-691b-431d-a412-e1609d34e9cd" />

sns.histplot(data=tit,x="Pclass",hue="Survived",kde=True)

<img width="659" height="455" alt="image" src="https://github.com/user-attachments/assets/272efd45-6b84-4838-a18e-78983fdfcdaa" />

import matplotlib.pyplot as plt

np.random.seed(0)

marks=np.random.normal(loc=70,scale=10,size=100)

marks

<img width="659" height="367" alt="image" src="https://github.com/user-attachments/assets/e5f6e89d-99a9-463b-9cfe-e222056d1f96" />

sns.histplot(data=marks,bins=10,kde=True,stat='count',cumulative=False,multiple='stack',element='bars',palette='Set1',shrink=0.7)

plt.xlabel('Marks')

plt.ylabel('Density')

plt.title('Histogram of Student Marks')

<img width="859" height="500" alt="image" src="https://github.com/user-attachments/assets/2f8dc6dd-a91e-4c5a-b6fe-2b4fd564a0f6" />

tips=sns.load_dataset('tips')

sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])

<img width="648" height="463" alt="image" src="https://github.com/user-attachments/assets/20b968b8-6e74-470e-9bc9-1f2a39499cd9" />

sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},

            whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})

 <img width="691" height="475" alt="image" src="https://github.com/user-attachments/assets/d02a84a7-b326-4018-93dd-aaf750b84f0c" />

sns.boxplot(x='Pclass',y='Age',data=tit,palette='rainbow')

plt.title("Age by Passenger Class,Titanic")

<img width="830" height="576" alt="image" src="https://github.com/user-attachments/assets/4ccbdfdf-79e1-4d7c-a80c-39d9e5f2b1d9" />

sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette="Set3",inner="quartile")

plt.xlabel("Day of the week")

plt.ylabel("Total Bill")

plt.title("Violin Plot of Total Bill by Day and Smoker Status")

<img width="676" height="472" alt="image" src="https://github.com/user-attachments/assets/ec0b5b4e-c5fc-4722-abe4-8f1ac208fae8" />

import seaborn as sns

sns.set(style='whitegrid')

tip=sns.load_dataset('tips')

sns.violinplot(x='day',y='tip',data=tip)

<img width="710" height="476" alt="image" src="https://github.com/user-attachments/assets/bf8183b3-0a0c-4bb6-acec-c1ff0e34dc27" />

sns.set(style='whitegrid')

tip=sns.load_dataset('tips')

sns.violinplot(x=tip["total_bill"])

<img width="640" height="467" alt="image" src="https://github.com/user-attachments/assets/305197bd-5304-4c38-9e5e-099fbaca94a3" />

sns.set(style='whitegrid')

tip=sns.load_dataset('tips')

sns.violinplot(x="tip",y="day",data=tip)

<img width="736" height="461" alt="image" src="https://github.com/user-attachments/assets/fe1d5cdb-87ed-420b-b758-5810c120e93b" />

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set3',alpha=0.8)

<img width="730" height="462" alt="image" src="https://github.com/user-attachments/assets/452f1a86-f360-44b8-a27b-2d3506d7abcf" />

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)

<img width="701" height="461" alt="image" src="https://github.com/user-attachments/assets/1aaf4232-a235-491e-bf4f-a78e04fe1206" />

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)

<img width="719" height="487" alt="image" src="https://github.com/user-attachments/assets/7f9cf354-71d7-4c69-b44f-c2a5a673c33f" />

data=np.random.randint(low=1,high=100,size=(10,10))

print("The data to be plotted:\n")

print(data)

<img width="342" height="220" alt="image" src="https://github.com/user-attachments/assets/d55afdf7-314a-4c22-ab69-27bf73338622" />

hm=sns.heatmap(data=data)

<img width="631" height="423" alt="image" src="https://github.com/user-attachments/assets/5a37bc03-42ab-4622-88bc-8011ffb97d2e" />

tips=sns.load_dataset('tips')

numeric_cols=tips.select_dtypes(include=np.number).columns

corr=tips[numeric_cols].corr()

sns.heatmap(corr,annot=True,cmap="plasma",linewidth=0.5)

<img width="614" height="450" alt="image" src="https://github.com/user-attachments/assets/fd509328-295c-438c-9c6a-ac52770e3f95" />








           













# Result:
Data Visualization using seaborn python library foe the given datas has been performed successfully
