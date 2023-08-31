# String Methods

## Lower Case:

```python
message = 'Hello'
print(message.lower()=="hello") #True

#Python is case sensitive
```

## Upper Case:

```python
message = 'hello'
print(message.upper()=="HELLO") #True

#Python is case sensitive
```

## Capitalize:

```python
message = 'Hello'
print(message=="hello".capitalize()) #True

#Python is case sensitive
```

## Format:

The `format()` method formats the specified value(s) and insert them inside the string's placeholder. The placeholder is defined using curly brackets: {}. The `format()` method returns the formatted string.

```python
txt = "I have {an:.2f} Rupees!"
print(txt.format(an = 4))
```

### Output:

```
I have 4.00 Rupees!
```

```python
# using format option in a simple string
print("{}, A computer science portal for geeks."
      .format("GeeksforGeeks"))
 
# using format option for a
# value stored in a variable
str = "This article is written in {}"
print(str.format("Python"))
 
# formatting a string using a numeric constant
print("Hello, I am {} years old !".format(18))
```

### Output:

```
GeeksforGeeks, A computer science portal for geeks.
This article is written in Python
Hello, I am  18 years old!
```

## Indexing:

Gives the fist index of the sub string.

Gives error when not found.

```python
message = 'Hello everybody'
print(message.index('Hello'))
```

### Output:

```
0
```

### Example 2:

```python
# list of items
list2 = ['cat', 'bat', 'mat', 'cat', 'pet']
 
# Will print the index of 'bat' in list2
print(list2.index('bat'))
```

### Output:

```
1
```

## Find:

Works like index but gives -1 when a value is not found.

```python
message = 'Hello everybody'
print(message.find('Hello'))
print(message.find('hello'))
```

### Output:

```
0
-1
```

## Replace:

The `replace()` method replaces a specified phrase with another specified phrase.

**Note:** *All* occurrences of the specified phrase will be replaced, if nothing else is specified.

```python
message = 'Hello everybody'

print(message.replace("Hello","Hi"))
#Replace 'Hello' with 'Hi'

print(message.replace('o','i',1))
# Replace o with i 1 time
```

### Output:

```
Hi everybody
Helli everybody
```

## Ends With:

Finds is the string is ending with that given character or substring.

```python
message = 'Hello everybody'
print(message.endswith('y')) #true
```

### Output:

```
True
```

### Split:

The `split()` method splits a string into a list. You can specify the separator, default separator is any whitespace.

**Note:** When maxsplit is specified, the list will contain the specified number of elements *plus one*.

### Example:

```python
txt = "hello, my name is Pratyay, I am 20 years old"

x = txt.split(", ")

print(x)
```

### Output:

```
['hello', 'my name is Pratyay', 'I am 20 years old']
```

## Join:

Joins a list with a seperator default is space. 

```python
txt = "hello, my name is Pratyay, I am 20 years old"

x = txt.split(", ")

print(','.join(x))
```

### Output:

```
hello,my name is Pratyay,I am 20 years old
```
