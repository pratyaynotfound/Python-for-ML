# Pandas

# Series in Python:

Series is a one-dimensional labeled array capable of holding data of any type (integer, string, float, python objects, etc.). The axis labels are collectively called index.

A pandas Series can be created using the following constructor:

```python
pandas.Series( data, index, dtype, copy)
```

## Example:

```python
series = pd.series([1,2,3,4,5,6])
#or
series = pd.series([1,2,3,4,5,6],index=['a','b','c','d','e'])
```

# ****Create a Series from ndarray:****

```python
#import the pandas library and aliasing as pd
import pandas as pd
import numpy as np
data = np.array(['a','b','c','d'])
s = pd.Series(data)
print s
```

### Output:

```python
0   a
1   b
2   c
3   d
dtype: object
```

## Update a series:

```python
series['e'] = 0 #updates
```

# Dataframe:

DataFrames in Python are a way to represent data in a tabular format. They are a core feature of the pandas library, which is a popular data analysis library in Python. DataFrames allow you to manipulate and analyze data, perform operations like filtering and aggregation, and visualize data using charts and graphs.

## Creating a Dataframe:

```python
# import pandas as pd
import pandas as pd
 
# list of strings
lst = ['Geeks', 'For', 'Geeks', 'is', 
            'portal', 'for', 'Geeks']
 
# Calling DataFrame constructor on list
df = pd.DataFrame(lst)
print(df)

#or
dataframe = pd.DataFrame([[1,2,3,10],
             [4,5,6,11],
             [7,8,9,12]],index = ['d','e','f'],columns=['a','b','c','d'])
```

dataframe is a combination of series.

```python
#by default locations
dataframe.iloc[1:] #[4,5,6,11]

#defined data type
dataframe.loc['e',:] # 4 5 6 11
```

## Apply in Dataframe:

Apply to a dataframe.

In Pandas, apply() is used to apply a function along an axis of the DataFrame. The function can be used on a single column or multiple columns of the DataFrame. It is a powerful tool for data transformation and cleaning.

Example:

```python
import pandas as pd
import numpy as np

df = pd.DataFrame({'A': [1, 2, 3],
                   'B': [4, 5, 6],
                   'C': [7, 8, 9]})

df.apply(np.sqrt)

```

This will apply the square root function to each element in the DataFrame.

Output:

```python
          A         B        C
0  1.000000  2.000000  2.645751
1  1.414214  2.236068  2.828427
2  1.732051  2.449490  3.000000

```

You can also use apply() to apply a custom function to a DataFrame. For example, if you want to add two columns together:

```python
def add_columns(x):
    return x['A'] + x['B']

df.apply(add_columns, axis=1)

```

Output:

```python
0     5
1     7
2     9
dtype: int64

```

Here, we define a custom function add_columns() that takes a row of the DataFrame as input, and returns the sum of columns A and B. We pass this function to apply() along axis=1 (i.e. apply the function to each row), and it returns a new Series containing the sum of columns A and B for each row.

# Create a dataframe using a dictionary:

To create a dataframe from a dictionary, you can use the `pandas.DataFrame()` function. The keys of the dictionary will become the column names and the values will become the data in the columns.

## Example:

```python
import pandas as pd

data = {'name': ['Alice', 'Bob', 'Charlie', 'David'],
        'age': [25, 30, 35, 40],
        'city': ['New York', 'Paris', 'London', 'Tokyo']}

df = pd.DataFrame(data)
print(df)

```

### Output:

```python
       name  age      city
0     Alice   25  New York
1       Bob   30     Paris
2   Charlie   35    London
3     David   40     Tokyo

```

In this example, we create a dictionary with three keys (`name`, `age`, and `city`) and their corresponding values. We then pass this dictionary to the `pandas.DataFrame()` function to create a dataframe. The resulting dataframe has one row for each entry in the dictionary and three columns for each of the keys.

# Convert to CSV:

To convert a Pandas dataframe to a CSV file, you can use the `to_csv()` method. This method allows you to specify the file path and name as well as other parameters such as the separator, index, and header.

## Example:

```python
import pandas as pd

# Create a dataframe
data = {'name': ['Alice', 'Bob', 'Charlie', 'David'],
        'age': [25, 30, 35, 40],
        'city': ['New York', 'Paris', 'London', 'Tokyo']}
df = pd.DataFrame(data)

# Convert dataframe to CSV file
df.to_csv('mydata.csv', index=False, sep=',')

```

## Additional parameters:

There are several additional parameters that you can use with the `to_csv()` method to customize the output. Here are some common ones:

- `header`: whether or not to include the column names in the output (default is `True`)
- `index_label`: the label for the index column (default is `None`)
- `na_rep`: the string to use for missing values (default is an empty string)
- `decimal`: the character to use for the decimal separator (default is `.`)
- `encoding`: the character encoding to use for the output (default is `utf-8`)
- `mode`: the file mode to use when writing the output (default is `w`)

For more information on these parameters and others, refer to the Pandas documentation on the `to_csv()` method.

# To read a CSV file into a dataframe, use the following code:

```python
import pandas as pd

df = pd.read_csv('filename.csv')

```

## Using index_col = false will remove the column index.

## We can specify a column using index_col = 0.

## We can add label by using index_labal = “index”

## We can get the information about the csv with df.info

![Untitled](Pandas%204dc34bff7e9e42f5a56a5af8febee802/Untitled.png)

## To read some rows or some columns we use nrows=#

![Untitled](Pandas%204dc34bff7e9e42f5a56a5af8febee802/Untitled%201.png)

## To skip rows we can use skiprows=#

![Untitled](Pandas%204dc34bff7e9e42f5a56a5af8febee802/Untitled%202.png)

# Missing values(nan values):

## If we dont want to see the nan values we can use na_filter = false

## We can replace this nan values with any type of data we want with fillna().

```python
df.fillna(df.mean()))
```

## Delete the rows or columns depending on the nan values.

```python
dataframe.drop(dropna)
```

## for updating the data we use inline=True.

## We can simply delete specific rows or columns with drop.

```python
df.drop('index name',axis='#',inplace = True)
```

# Merge 2 data frames:

1. **Inner Join:**
    - An inner join returns only the matching rows from both datasets based on the common key or column.
    - It keeps only the rows where the key value exists in both datasets.
2. **Outer Join (Full Outer Join):**
    - An outer join returns all rows from both datasets, matching rows and non-matching rows.
    - It includes all the rows from both datasets, regardless of whether they have a match in the other dataset.
3. **Left Join (Left Outer Join):**
    - A left join returns all rows from the left dataset and the matching rows from the right dataset.
    - It includes all the rows from the left dataset, regardless of whether they have a match in the right dataset.
4. **Right Join (Right Outer Join):**
    - A right join returns all rows from the right dataset and the matching rows from the left dataset.
    - It includes all the rows from the right dataset, regardless of whether they have a match in the left dataset.
5. **Cross Join (Cartesian Join):**
    - A cross join returns the combination of all rows from both datasets, resulting in a Cartesian product.
    - It does not require a common key or column.

```python
import pandas as pd

# Sample dataframes
df1 = pd.DataFrame({'ID': [1, 2, 3, 4],
                    'Name': ['John', 'Alice', 'Bob', 'Linda'],
                    'Age': [25, 30, 35, 40]})

df2 = pd.DataFrame({'ID': [3, 4, 5, 6],
                    'City': ['London', 'Paris', 'New York', 'Sydney'],
                    'Salary': [5000, 6000, 7000, 8000]})

# Inner Join
inner_join = pd.merge(df1, df2, on='ID', how='inner')
print("Inner Join:")
print(inner_join)
print()

# Outer Join (Full Outer Join)
outer_join = pd.merge(df1, df2, on='ID', how='outer')
print("Outer Join:")
print(outer_join)
print()

# Left Join (Left Outer Join)
left_join = pd.merge(df1, df2, on='ID', how='left')
print("Left Join:")
print(left_join)
print()

# Right Join (Right Outer Join)
right_join = pd.merge(df1, df2, on='ID', how='right')
print("Right Join:")
print(right_join)
print()

# Cross Join (Cartesian Join)
cross_join = pd.merge(df1, df2, on=None, how='cross')
print("Cross Join:")
print(cross_join)
```

### Output:

```python
Inner Join:
   ID   Name  Age    City  Salary
0   3    Bob   35  London    5000
1   4  Linda   40   Paris    6000

Outer Join:
   ID   Name   Age      City  Salary
0   1   John  25.0       NaN     NaN
1   2  Alice  30.0       NaN     NaN
2   3    Bob  35.0    London  5000.0
3   4  Linda  40.0     Paris  6000.0
4   5    NaN   NaN  New York  7000.0
5   6    NaN   NaN    Sydney  8000.0

Left Join:
   ID   Name  Age    City  Salary
0   1   John   25     NaN     NaN
1   2  Alice   30     NaN     NaN
2   3    Bob   35  London  5000.0
3   4  Linda   40   Paris  6000.0

Right Join:
   ID   Name   Age      City  Salary
0   3    Bob  35.0    London    5000
1   4  Linda  40.0     Paris    6000
2   5    NaN   NaN  New York    7000
3   6    NaN   NaN    Sydney    8000

Cross Join:
    ID_x   Name  Age  ID_y      City  Salary
0      1   John   25     3    London    5000
1      1   John   25     4     Paris    6000
2      1   John   25     5  New York    7000
3      1   John   25     6    Sydney    8000
4      2  Alice   30     3    London    5000
5      2  Alice   30     4     Paris    6000
6      2  Alice   30     5  New York    7000
7      2  Alice   30     6    Sydney    8000
8      3    Bob   35     3    London    5000
9      3    Bob   35     4     Paris    6000
10     3    Bob   35     5  New York    7000
11     3    Bob   35     6    Sydney    8000
12     4  Linda   40     3    London    5000
13     4  Linda   40     4     Paris    6000
14     4  Linda   40     5  New York    7000
15     4  Linda   40     6    Sydney    8000
```