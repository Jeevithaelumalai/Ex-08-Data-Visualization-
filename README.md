# Ex-08-Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
# DEVELOPED BY:JEEVITHA.E
# REG NO : 212222230054

# OUPUT:
# Reading the given dataset :
import pandas as pd
df=pd.read_csv("/content/Superstore (3).csv",encoding='unicode_escape')

df.head()
# Data Visualization using Seaborn :
import seaborn as sns
from matplotlib import pyplot as plt
# 1.Line Plot :
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)

sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)

sns.lineplot(x="Category",y="Sales",data=df,marker='o')
# 2.Scatterplot :

sns.scatterplot(x='Category',y='Sub-Category',data=df)

sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)

plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
# 3.Boxplot :

sns.boxplot(x="Sub-Category",y="Discount",data=df)

sns.boxplot( x="Profit", y="Category",data=df)
# 4.Violin Plot :

sns.violinplot(x="Profit",data=df)
# 5.Barplot :
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)

sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
# 6.Pointplot :
sns.pointplot(x=df["Quantity"],y=df["Discount"])
# 7.Count plot :
sns.countplot(x="Category",data=df)

sns.countplot(x="Sub-Category",data=df)
# 8.Histogram :
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
# 9.KDE Plot :
sns.kdeplot(x="Profit", data = df,hue='Category')
Data Visualization Using MatPlotlib :
# 1.Plot :
plt.plot(df['Category'], df['Sales'])
plt.show()
# 2.Heatmap :
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
# 3.Piechart :
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
# 4.Histogram :
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
# 5.Bargraph :
plt.bar(df.index,df['Category'])
plt.show()
# 6.Scatterplot :
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
# 7.Boxplot :
plt.boxplot(x="Sales",data=df)
plt.show()
# OUTPUT :
# Reading the given dataset :
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/4441cdcd-a231-44d7-b04e-2e406dcba01d)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/125fa3d9-d812-4557-85b9-d8d6252346f0)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/32b10f0a-a432-4aa8-aa16-d5c651923017)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/9c8c95d5-f587-43b5-8660-7ee6979a1053)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/e38deb22-cbdb-447e-b729-fda4790f374c)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/a1290cc9-2341-4983-9f49-de5182b8fb61)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/df6cf5b7-831a-413d-815a-c5c232982412)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/69bb23f3-6a17-4aa5-adea-ffdb131e5187)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/28eb5d9d-3ae3-4ef5-8624-657135515c81)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/87f18d4f-a895-4c38-a113-f51641b2c344)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/3e3be074-0f08-4433-9bdd-188f091b9bd3)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/62baaafa-3cf4-44ef-b1d2-8d851b3bcee1)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/4ac57838-40bc-41ea-bf04-7b4afe0b494f)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/ecd1ecc4-4db7-4831-93c9-220193732081)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/11be7c68-1185-43a5-9ab3-92a0bd0b7d4d)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/074fee24-f216-4255-8841-7eb8f48aebdc)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/cfb176c7-62d8-4f4f-a3c1-2d7c8849c188)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/c5f1d819-850f-45b2-a948-a96313fe1ccc)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/c9848681-d9e0-4e99-8f7c-ee9c0ea8e7f2)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/32e72b07-3cc3-4537-9814-18e3b5e81495)
![image](https://github.com/Jeevithaelumalai/Ex-08-Data-Visualization-/assets/118708245/f2f66c01-224b-40d8-b69e-552d9a8554f6)

