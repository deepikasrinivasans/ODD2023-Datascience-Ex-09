# Ex-09-Data-Visualization-

## AIM
To Perform Data Visualization on a complex dataset and save the data to a file. 

## Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.

## CODE

### Developed by:ABINAYA S
### Register number:212222230002
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
tips

tips.head()

tips.info()
```
#### Which day of the week has the highest total bill amount?
```
sns.barplot(x='day',y='total_bill',data=tips)
plt.title("Weekly highest total bill amount")
```
### What is the average tip amount given by smokers and non-smokers?
```
sns.barplot(x='smoker',y='tip',data=tips, palette='rainbow')
plt.title("Average tip amount given by smokers and non-smokers")
```
### How does the tip percentage vary based on the size of the dining party?
```
sns.boxplot(x='size', y='tip',data=tips)
plt.title("Tip percentage based on the sizes of the dining party")
```
### Which gender tends to leave higher tips?
```
sns.boxplot(x='sex', y='tip',data=tips)
plt.title("Higher tips based on gender")
```
### Is there any relationship between the total bill amount and the day of the week?
```
plt.plot(tips['day'],tips['total_bill'])
plt.title("Relationship between the total bill amount and the day of the week")
plt.show()
```
### How does the distribution of total bill amounts vary across different time periods (lunch vs. dinner)?
```
sns.violinplot(x='time',y='total_bill',data=tips)
plt.title("Distribution of total bill amounts vary across different time periods(lunch vs. dinner)")
```
### Which dining party size group tends to have the highest average total bill amount?
```
sns.barplot(x='size',y='total_bill',data=tips)
plt.title("Highest average total bill amount based party size")
```
### What is the distribution of tip amounts for each day of the week?
```
sns.boxplot(x='day',y='total_bill',data=tips)
plt.title("Distribution of tip amounts for each day of the week")
```
### How does the tip amount vary based on the type of service (lunch vs. dinner)?
```
sns.violinplot(x='time',y='tip',data=tips)
plt.title("Tip based on the type of service ")
```
### Is there any correlation between the total bill amount and the tip amount?
```
sns.scatterplot(data=tips, x='total_bill', y='tip')
correlation_coefficient = tips['total_bill'].corr(tips['tip'])
print("Correlation Coefficient:", correlation_coefficient)
```
### heatmap
```
tips.corr()
plt.subplots(figsize=(7,5))
sns.heatmap(tips.corr(),annot=True)
```
## OUPUT
### Initial dataset:
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/66aa6ce0-ac5a-4e0d-b9e9-679fc472bf9e)


### tips.head():
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/d81d6d7f-9155-4ca7-9851-f5c2cc9005da)


### tips.info():
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/8688c2e6-287a-4e9d-ad27-07b4c123cbc2)

### Barplot:
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/0db7fb54-27ef-48c2-a1d7-da949ae11691)

![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/54bd1077-c2f2-40b4-8646-ce9a1cf6d425)


### Boxplot:
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/2e14ddc7-7d51-4af4-bbd7-093cb71ae858)

![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/1829429d-cdc7-4601-9270-18286b68b224)


### Plot:
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/9836e0e9-3368-40b6-9874-7108f3007e88)


### Violinplot:
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/67b4c41a-109c-4d2d-a272-bc4cdff99690)

### Barplot:
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/c358567c-1db6-4286-a6c8-fdbeb264c5eb)

### Boxplot:
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/0aabf0ff-3e44-4d5f-90b6-4e0dd799612a)

### Violinplot:
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/ac2bee7e-5d99-47f8-8cf1-f8c0dc6ccf78)

### Scatterplot:
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/38599dfa-b1ce-4c08-87cd-f1c6fb7f0aa9)


### Heatmap:
![image](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex-09/assets/119393675/14f34705-4a03-4bec-9425-ad4094228e06)

## RESULT:
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully based on tips dataset and the data is saved to file
