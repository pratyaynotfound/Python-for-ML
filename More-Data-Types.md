# More Data Types

# List:

Lists are used to store multiple items in a single variable. Lists are created using square brackets:

```python
thislist = ["apple", "banana", "cherry"]
print(thislist)
```

### Output:

```python
['apple', 'banana', 'cherry']
```

# Tuple:

Tuples are used to store multiple items in a single variable. A tuple is a collection which is ordered and **unchangeable**.

```python
thistuple = ("apple", "banana", "cherry")
print(thistuple)
```

### Output:

```python
('apple', 'banana', 'cherry')
```

# Dictionary:

Dictionaries are used to store data values in key:value pairs. A dictionary is a collection which is ordered*, changeable and do not allow duplicates. Dictionaries are written with curly brackets, and have keys and values:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
```

### Output:

```python
{'brand': 'Ford', 'model': 'Mustang', 'year': 1964}
```

## #Print from a dictionary:

```python
print(thisdict["brand"])
print(thisdict.get('brand'))
```

### Output:

```python
Ford
Ford
```

## #POP

The `pop()` method removes the specified item from the dictionary.

The value of the removed item is the return value of the `pop()` method.

### Syntax:

```python
dictionary.pop(keyname, defaultvalue)
```

### Example:

```python
car = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

x = car.pop("model")

print(x)
```

### Output:

```python
Mustang
```

## #Add key to dictionary:

### Syntax:

```python
dictionary['d'] = 88 # New key
dictionary.update({0:1,1:2,2:3})
```

## Additional:

For listing only keys(all) we use `dictionary.keys()`

For listing only values(all) we use `dictionary.values()`

For listing keys and values we use `dictionary.items()`

# Sets:

Sets are used to store multiple items in a single variable. Set is one of 4 built-in data types in Python used to store collections of data, the other 3 are [List](https://www.w3schools.com/python/python_lists.asp), [Tuple](https://www.w3schools.com/python/python_tuples.asp), and [Dictionary](https://www.w3schools.com/python/python_dictionaries.asp), all with different qualities and usage. A set is a collection which is *unordered*, *unchangeable**, and *unindexed*.

**Note:** Set *items* are unchangeable, but you can remove items and add new items.

### Example:

```python
thisset = {"apple", "banana", "cherry"}
print(thisset)
```

### Output:

```python
{'banana', 'apple', 'cherry'}
```

Suppose 2 sets we can perform intersection, union,pop,remove and some other methods:

```python
x = {"apple", "banana", "cherry","pear"}
y = {"google", "microsoft", "apple"}

#intersection
print(x.intersection(y))

#union
print(x.union(y))

#pop
print(x.pop())

#remove
print(x.remove("pear"))
print(x)

```

### Output:

```python
{'apple'}
{'apple', 'cherry', 'google', 'microsoft', 'pear', 'banana'}
apple
None
{'cherry', 'banana'}
```

# Difference:

The `difference()` method returns a set that contains the difference between two sets.

Meaning: The returned set contains items that exist only in the first set, and not in both sets.

### Syntax:

```python
set.difference(set)
```

## Example:

```python
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

z = y.difference(x)

print(z)
```

### Output:

```python
{'microsoft', 'google'}
```

# Difference_update:

The `difference_update()` method removes the items that exist in both sets.

The `difference_update()` method is different from the `difference()` method, because the `difference()` method *returns a new set*, without the unwanted items, and the `difference_update()` method *removes* the unwanted items from the original set.

### Syntax:

```python
set.difference_update(set)
```

# Example:

```python
# Python code to get the difference between two sets
# using difference_update() between set A and set B
 
# Driver Code
A = {10, 20, 30, 40, 80}
B = {100, 30, 80, 40, 60}
 
# Modifies A and returns None
A.difference_update(B)
 
# Prints the modified set
print (A)
```

### Output:

```python
{20, 10}
```
