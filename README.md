# Ex-09-Data-Visualization

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

### Developed by:Deepika S
### Register number:212222230028
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
![dd1](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/30674bab-ad97-49dd-b173-74c7413ed3a6)
### tips.head():
![dd2](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/d5df2a3a-f455-4559-a912-6bcfa5a122c1)
### tips.info():
![dd3](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/cad6b7fe-7aa9-4419-b228-d19935d12b54)
### Barplot:
![dd4](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/36dfe8dc-6947-4abe-aeb8-52dce4e76ca0)
![dd5](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/d228d387-622e-4b18-ab2a-68fc0f790f5a)
### Boxplot:
![dd6](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/06df1e05-396b-4277-801c-cb0fffc0a421)
![dd7](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/85aae2b9-9c39-4e7f-ac05-13f55f67c917)
### Plot:
![dd8](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/6d5d6eb4-7107-4846-86f6-b985133ce70c)
### Violinplot:
![dd9](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/6517f467-b25e-4b23-b635-f45db6d6e3d3)
### Barplot:
![dd10](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/a7b71024-0c18-494b-bc88-4e1f10fa9313)
### Boxplot:
![dd11](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/a6d7ee28-593d-417f-b99d-a79f922dc3f9)
### Violinplot:
![dd12](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/089ad0c1-ed69-4d75-a4b1-bfac9f2a0a4c)
### Scatterplot:
![dd13](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/d48f7d46-a19f-492a-918d-e07c4d9c6ad6)
### Heatmap:
![dd14](https://github.com/deepikasrinivasans/ODD2023-Datascience-Ex-09/assets/119393935/75a550b0-bb56-4fec-afe1-66c91144e51e)
## RESULT:
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully based on tips dataset and the data is saved to file
