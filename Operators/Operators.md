# Operators

## Arithmetic Operators

- Addition(+)
- Subtraction(-)
- Multiplication(*)
- Division(/)
- Modulo(%)
- Power(**)

  This operator can be used to perform the exponent arithmetic in Python.
    
    ```python
    x = (a**3) #this means x^3
    ```
    
- Floor Division(//)
    
    Floor division is **a division operation that rounds the result down to the nearest whole number or integer, which is less than or equal to the normal division result**.
    
    ```python
    a = 56
    b = 6
    print(a//b)
    # Result is 9
    ```
    

# Type Operator

```python
print(type(4))
print(type(5.8))
print(type("Hello"))
```

![Operator Types](Operators%203ac146a8840247e799dfa3f6c21b99f3/Untitled.png)

# Type Casting

```python

a = '10.5'
b = int(a)
```

### Input Statement

For user input.

```python
user_input = input("Please enter a statement")
```

# Comparison Operators

- Greater Than(>)
- Less than(<)
- Greater Than Equal To(≥)
- Less than Equal to(≤)
- Not Equal To(≠)
- Equal To(==)

# Logical Operators

- or
- and
- not

```python
a = 6
b = 5
c = 7

print((a<b)and(a<c)) #false
print((a<b)or(a<c)) #true
print(not(a<b)) #true
```

# Membership Operators

It test for membership in a sequence, such as strings, lists, or tuples. in operator : The 'in' operator is used to check if a value exists in a sequence or not.

- in
- not in

```python
print('hell' in "hello") #true
print('hell' not in "hello") #false
```

# Logical Statements

- if
- elif
- else

```python
a = 5
b = 6
c = 7

if a>b:
	if a>c:
		print(a, "Greatest")
	else:
		print(c, "Greatest")
else:
	if b>c:
		print(b,"Greatest")
	else:
		print(c,"Greatest")
```

### Simple User Id login:

```python
user, id = "Admin",12345
user_inp = input("Please Enter User id:")
if user == user_inp:
    pass_inp = int(input("Enter the Password:"))
    if id == pass_inp:
        print("Login Successful!")
    else:
        print("Incorrect Password!")
else:
    print("Invalid user!")
```

# String Slicing

In this example, we will see **slicing in python list** the index start from 0 indexes and ending with a 2 index(stops at 3-1=2 ).

```python
# String slicing
String = 'GEEKSFORGEEKS'
 
# Using indexing sequence
print(String[:3])
```

Output: `GEE`

```python
message = 'How are you all?'

print(message[0]) #H
print(message[-1]) #?

#middle 
print(message[(int((len(message)-1)/2))]) #'space'
#multiple [start:end-1]

print(message[0:2]) #Ho

#alternative
print(message[0::2]) #Hwaeyual

#Every second
print(message[0::3]) #H eoa?

#reverse
print(message[::-1]) #?lla uoy era woH
```

# Adam Number

Adam number is **a number for which the square of its reverse is equal to the reverse of the square of the number**.

1. 12^2 = 144
2. reverse(144) = 441
3. reverse(12) = 21
4. (21)^2 = 441

```python
num = int(input("Enter a number:"))
num1 = int(str(int(int(str(num**2)[::-1])**0.5))[::-1])
if num==num1:
    print("Adam number.")
else:
    print("Not an adum number.")
```

# Homework

## Palindrome Check

```python
num = input("Enter a number:")
rev_num = num[::-1]
if num == rev_num:
    print("Palindrome!")
else:
    print("Not a palindrome!")
```

## Month Print

```python
month="JanFebMarAprMayJunJulAugSepOctNovDec"
i = int(input("Enter a number(1-12):"))
print(month[((i-1)*3):(((i-1)*3)+3)])
```
