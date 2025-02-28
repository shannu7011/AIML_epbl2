# Artificial Intelligence and Machine Learning

https://colab.research.google.com/drive/1oo_rxfK_T3ZOK68vQpp-qCfMhhBrjv9N#scrollTo=6AIVcVGiS8mI&line=1&uniqifier=1



## Assignment No - 1
string_example = "Hello, World!"
print(string_example.upper())
print(string_example.lower())
print(string_example.split(','))
print(string_example.replace("World", "Python"))
print(string_example.find("World"))
list_example = [1, 2, 3, 4, 5]
list_example.append(6)
list_example.remove(3)
list_example.reverse()
print(list_example)
print(list_example.index(2))
dict_example = {"name": "Alice", "age": 25}
print(dict_example.keys())
print(dict_example.values())
dict_example.update({"city": "New York"})
print(dict_example.get("age"))
print(dict_example.pop("name"))
set_example = {1, 2, 3, 4}
set_example.add(5)
set_example.remove(2)
print(set_example.union({6, 7}))
print(set_example.intersection({3, 4, 5}))
tuple_example = (1, 2, 3, 2, 1)
print(tuple_example.count(2))
print(tuple_example.index(3))
with open("sample.txt", "w") as file:
    file.write("Hello, File!")
with open("sample.txt", "r") as file:
    print(file.read())
class SampleClass:
    def __init__(self, value):
        self.value = value
    
    def show(self):
        return f"Value: {self.value}"
obj = SampleClass(10)
print(obj.show())


## Assignment No - 2
# NumPy 100 Examples
import numpy as np

# Generating arrays
arr1 = np.array([1, 2, 3])
arr2 = np.zeros((3,3))
arr3 = np.ones((4,4))
arr4 = np.eye(3)
arr5 = np.linspace(0, 10, 5)
arr6 = np.arange(10, 50, 5)
arr7 = np.random.randint(1, 100, (5, 5))
arr8 = np.random.randn(5, 5)
arr9 = np.tile([1, 2], (3, 2))
arr10 = np.clip(arr7, 10, 50)

# Mathematical operations
arr11 = np.add(arr1, 10)
arr12 = np.subtract(arr1, 5)
arr13 = np.multiply(arr1, 3)
arr14 = np.divide(arr1, 2)
arr15 = np.power(arr1, 2)
arr16 = np.sqrt(arr1)
arr17 = np.exp(arr1)
arr18 = np.log(arr1 + 1)
arr19 = np.sin(arr1)
arr20 = np.cos(arr1)

# Matrix operations
mat1 = np.dot(arr1.reshape(3,1), arr1.reshape(1,3))
mat2 = np.linalg.inv(np.eye(3))
mat3 = np.linalg.det(np.eye(3))
mat4 = np.linalg.eigvals(np.eye(3))
mat5 = np.linalg.norm(arr1)

# Sorting and filtering
arr21 = np.sort(arr7)
arr22 = np.argsort(arr7)
arr23 = np.where(arr7 > 50, 1, 0)
arr24 = np.unique(arr7)
arr25 = np.argmax(arr7)

# Aggregation
arr26 = np.sum(arr7)
arr27 = np.mean(arr7)
arr28 = np.std(arr7)
arr29 = np.var(arr7)
arr30 = np.median(arr7)

print("NumPy examples completed.")

# Pandas 100 Examples
import pandas as pd

# Creating DataFrames
df1 = pd.DataFrame(np.random.rand(100, 5), columns=['A', 'B', 'C', 'D', 'E'])
df2 = pd.DataFrame({'Name': ['Alice', 'Bob', 'Charlie'], 'Age': [25, 30, 35], 'Salary': [50000, 60000, 70000]})

# Data Selection
first_row = df1.iloc[0]
column_B = df1['B']
subset = df1[['A', 'C']]

# Data Manipulation
df1['F'] = df1['A'] + df1['B']
df1.drop(columns=['E'], inplace=True)
df1.rename(columns={'A': 'Alpha'}, inplace=True)
df1.fillna(0, inplace=True)

# Grouping and Aggregation
grouped = df2.groupby('Age').sum()
average_salary = df2['Salary'].mean()

# Merging and Joining
df3 = df2.merge(df1, left_index=True, right_index=True, how='inner')
concat_df = pd.concat([df2, df2], ignore_index=True)

# Data Analysis
df1.describe()
df1.corr()
df1.value_counts()
df1.sort_values(by='Alpha', ascending=False)
df1.apply(lambda x: x * 2)

print("Pandas examples completed.")

# Matplotlib Graphs (10 Examples with Use Cases)
import matplotlib.pyplot as plt

# 6. Area Chart - Used for visualizing cumulative trends
x = np.linspace(0, 10, 100)
y = np.sin(x)
plt.fill_between(x, y, color="skyblue", alpha=0.4)
plt.title("Area Chart - Cumulative trends")
plt.show()

# 7. Stem Plot - Used for showing discrete data points
plt.stem(x, y)
plt.title("Stem Plot - Showing discrete signals")
plt.show()

# 8. Error Bar Plot - Used for representing uncertainty
errors = np.random.rand(10)
x_vals = np.arange(10)
y_vals = np.random.rand(10) * 10
plt.errorbar(x_vals, y_vals, yerr=errors, fmt='o')
plt.title("Error Bar Plot - Representing uncertainties")
plt.show()

# 9. Polar Plot - Used for representing angular data
r = np.linspace(0, 10, 100)
theta = np.linspace(0, 2*np.pi, 100)
plt.polar(theta, r)
plt.title("Polar Plot - Angular data representation")
plt.show()

# 10. Violin Plot - Used for visualizing distribution
import seaborn as sns
sns.violinplot(y=data)
plt.title("Violin Plot - Distribution visualization")
plt.show()

# Seaborn Graphs (10 Examples with Use Cases)
df = sns.load_dataset("tips")

# 4. Seaborn KDE Plot - Used for estimating data distribution
sns.kdeplot(df['total_bill'], shade=True)
plt.title("KDE Plot - Estimating distribution")
plt.show()

# 5. Seaborn Joint Plot - Used for visualizing two-variable relationships
sns.jointplot(x='total_bill', y='tip', data=df, kind='hex')
plt.show()

# 6. Seaborn Pair Plot - Used for comparing multiple variables
sns.pairplot(df[['total_bill', 'tip', 'size']])
plt.show()

# 7. Seaborn Swarm Plot - Used for showing categorical distribution
sns.swarmplot(x='day', y='total_bill', data=df)
plt.title("Swarm Plot - Showing categorical distribution")
plt.show()

# 8. Seaborn Count Plot - Used for counting categorical occurrences
sns.countplot(x='day', data=df)
plt.title("Count Plot - Counting categorical values")
plt.show()

# 9. Seaborn Boxen Plot - Used for high-dimensional data distribution
sns.boxenplot(x='day', y='total_bill', data=df)
plt.title("Boxen Plot - Handling large datasets")
plt.show()

# 10. Seaborn Regression Plot - Used for showing trends
sns.regplot(x='total_bill', y='tip', data=df)
plt.title("Regression Plot - Showing linear trends")
plt.show()

print("All examples completed.")
