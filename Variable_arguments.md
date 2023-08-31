# Many Arguments

### In Python, you can specify a variable number of arguments when calling a function by adding `*` or `**` to the beginning of parameter names in the function definition.

```python
def multi_add(*a):
    return sum(a)

print(multi_add(1,2,3,4))
```

# Giving keywords as arguments:

### For keyword arguments we give `**` in th function.

```python
def multi_add(**a):
    print(a)

multi_add(a=1,b=2,c=3,d=4)
```

### Output:

```python
{'a': 1, 'b': 2, 'c': 3, 'd': 4}
```

# Inline Function using Lambda:

We use the `lambda` keyword instead of `def` to create a lambda function. Here's the syntax to declare the lambda function:

```python
lambda argument(s) : expression
```

Here,

- `argument(s)` - any value passed to the lambda function
- `expression` - expression is executed and returned

## Example:

```python
greet = lambda : print('Hello World')
```

Here, we have defined a lambda function and assigned it to the variable named greet.

To execute this lambda function, we need to call it. Here's how we can call the lambda function

```python
# call the lambda
greet()
```

The lambda function above simply prints the text `'Hello World'`.

## Inline Conditional statement:

```python
greater = lambda a,b:print(a,'is greater') if a>b else print(b,'is greater')

greater(1,2)
```

### Output:

```python
2 is greater
```

## Inline for loop:

```python
print([i**2 for i in range(10)])
```

### Output:

```python
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

## Inline Nested for loop(list Comprehension):

```python
print([i**2 for i in range(10) for j in range (i)])
```

### Output:

```python
[1, 4, 4, 9, 9, 9, 16, 16, 16, 16, 25, 25, 25, 25, 25, 36, 36, 36, 36, 36, 36, 49, 49, 49, 49, 49, 49, 49, 64, 64, 64, 64, 64, 64, 64, 64, 81, 81, 81, 81, 81, 81, 81, 81, 81]
```
