# Ex-08-Data-Visualization-
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Clean the Data Set using Data Cleaning Process

## STEP 3
Apply Feature generation and selection techniques to all the features of the data set

## STEP 4
Apply data visualization techniques to identify the patterns of the data.

# CODE
### READING THE GIVEN FILES:
```
import pandas as pd
df=pd.read_csv("/content/Superstore.csv",encoding='unicode_escape')
df.head()
```
# DATA VISUALIZATION USING SEABORN :
```
import seaborn as sns
from matplotlib import pyplot as plt
```
# LINE PLOT:
```
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
```
![281668264-4aab30cb-a4a8-45d1-8bae-aceeb0eca278](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/5b7c067f-0e23-40aa-80de-7f2d5302e4c2)


![281347728-8c02f032-c237-4743-83ef-75a9203c9e47](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/647cd99b-b826-4cc2-a394-f507826eb039)

![281348472-2aecf214-5be9-4594-83dd-1df66e763f21](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/9926a587-ccd9-4efb-8d6f-9d0780584047)

# SCATTERPLOT:

```
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)

```
![281349914-f38352d4-504c-4926-b6e7-512734888392](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/45bac79a-8503-4915-b8a5-eff1ac4aa74f)

![281350142-2bb1b565-0c26-4730-998a-64c6a81ac3ac](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/bdd2e9e6-b475-4b86-b43b-196c76fd6955)
![281350354-4f77f0e1-2fe2-4fb2-900f-6f3940bd6ee9](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/1e05cfdd-bdc7-4148-aa7b-8aa3abf004c0)


### BOXPLOT:
```
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)

```
![281350725-f230a62e-f13f-416a-ae1e-0086c2922bcb](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/2ea9b4c8-0239-46e6-bff5-4f4259b72b7e)

![281350967-e21b3b38-3517-45c6-80ad-f44daf9679f7](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/36f3813b-e346-4c78-87e3-39c5ac84063c)


# VIOLIN PLOT:
```
sns.violinplot(x="Profit",data=df)

```
![281351392-bb267ffa-c369-47d1-be47-05fe4137ea85](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/4ec8059c-98b1-4c71-bc8e-103b184e2102)

# BARPLOT:
```

sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
```

![281351863-69b310d0-7686-465b-8033-7ea17a0833d8](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/1cd40ef2-0db1-47bb-af9e-f738d26d9274)

![281664476-9291dcfb-d723-49fd-b33c-58ad22a16809](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/a9697bcc-b74d-41f2-9604-d3b413c03f4c)


#POINTPLOT:

```

sns.pointplot(x=df["Quantity"],y=df["Discount"])

```

![281665527-b6a6f701-ebda-4fcb-a307-fde1f02045a2](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/7972bf63-b1f7-4c81-8032-105feec6ea85)
# COUNT PLOT:
```
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
```
![281665684-7b9191b4-d75e-4dfe-a051-04b6ba045d96](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/bf755632-d070-44ef-89ed-a4e02407eafa)


![281665754-e3c70bf2-4703-43b1-b695-eab0559eded0](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/6ec64084-d8cd-448b-af80-d748e4e26d6d)

# HISTOGRAM :
```
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')

```

![281666278-73c5c5c3-606e-4030-9406-801e7775649d](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/ef08582c-01d9-406c-8921-67c3154b3682)

# KDE PLOT:
```
sns.kdeplot(x="Profit", data = df,hue='Category')
```
![281666458-253bae47-e0ad-4ca3-9643-648af77da202](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/b3d5ffaf-9ea3-4318-a1d4-994022dc27da)


# DATA VISUALIZATION USING MATPLOTLIB :
# PLOT :
```
plt.plot(df['Category'], df['Sales'])
plt.show()


```

![281666779-0549a345-7dc0-4616-9a29-95accc134733](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/2cb34f9e-eb14-4126-882c-f25c3fcc5e82)

# HEATMAP :

```
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```


![281667059-4a74ae29-1c3c-4745-82ef-dd8167e7feb9](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/24349829-7af9-404b-95b3-2eba14b77981)

# PIECHART:
```
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()

df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
```

![281667217-3bdf032f-371c-4225-aeb6-641d22090907](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/b2a276ac-79b7-4b0c-8471-03516635a5d8)


![281667296-d29ea959-ff0d-490d-9867-68f86406188b](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/8a4dea98-9c1d-4c22-acbc-68acf1f2838d)

# HISTOGRAM: 

```
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
```
![281667422-d40c0a4d-3fec-46b5-828f-7b95db50ee83](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/3d9f14f8-225b-4206-a149-da5a2ee2f555)


### BARGRAPH: 

```
plt.bar(df.index,df['Category'])
plt.show()
```
![281667581-a551d5d6-d08b-4331-8c27-80848cc9992f](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/d7a43426-dac2-4c4a-b251-2cefb1cf2ef2)

# SCATTERPLOT: 

```
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
```
![281667664-b49ce246-8246-4c50-b00e-217ea3ec7c1d](https://github.com/Aravindsamy04/ODD2023-Datascience-Ex-08/assets/113497037/ea53e5b3-99e7-44b6-b956-bbee44ce7412)

# BOXPLOT: 
```
plt.boxplot(x="Sales",data=df)
plt.show()
```

# RESULT:

Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.

