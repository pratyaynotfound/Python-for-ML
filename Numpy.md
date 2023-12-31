# Numpy

### Installation:

To install Numpy, you can use the following command in your terminal:

```
pip3 install numpy

```

Numpy is a popular Python library used for working with arrays and matrices. It provides a large collection of mathematical functions to operate on these arrays.

## Creating a basic data:

```python
import numpy as np

array = np.array([1,7,9,56,98,99,145])
array1 = np.array([1,7,9,56,98,99,145],dtype=float)
print(array)
print(array1)
```

### Output:

```python
[  1   7   9  56  98  99 145]
[  1.   7.   9.  56.  98.  99. 145.]
```

## Some methods:

```python
import numpy as np

array = np.array([1,7,9,56,98,99,145])
array1 = np.array([1,7,9,56,98,99,145],dtype=float)
print(array)
print(array1)
print(type(array))
print(array.ndim)
print(array.shape)
print(array.mean())
print(array.max())
print(array.min())
```

### Output:

```python
[  1   7   9  56  98  99 145]
[  1.   7.   9.  56.  98.  99. 145.]
<class 'numpy.ndarray'>
1
(7,)
59.285714285714285
145
1
```

### Make a array of Shape (3,3,4,5)

```python
import numpy as np

array = np.array(
    [
        [
            [
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5]
            ],
            [
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5]
            ],
            [
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5]
            ]
        ],
        [
            [
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5]
            ],
            [
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5]
            ],
            [
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5]
            ]
        ],
        [
            [
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5]
            ],
            [
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5]
            ],
            [
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5],
               [1,2,3,4,5]
            ]
        ]
    ]
)
print(array.shape)
```

### Output:

```python
(3, 3, 4, 5)
```

## Arange function:

```python
import numpy as np
arr = np.arange(12)
arr1 = np.arange(10,30,2)

print(arr)
print(arr1)
```

### Output:

```python
[ 0  1  2  3  4  5  6  7  8  9 10 11]
[10 12 14 16 18 20 22 24 26 28]
```

## Reshape:

```python
import numpy as np
arr = np.arange(10,30)
arr = arr.reshape((4,5))
print(arr)
```

### Output:

```python
[[10 11 12 13 14]
 [15 16 17 18 19]
 [20 21 22 23 24]
 [25 26 27 28 29]]
```

## Identity:

```python
import numpy as np
identity = np.eye(5)
print(identity.shape)
print(identity)

identity2 = np.eye(4,6)
print(identity2.shape)
print(identity2)
```

### Output:

```python
(5, 5)
[[1. 0. 0. 0. 0.]
 [0. 1. 0. 0. 0.]
 [0. 0. 1. 0. 0.]
 [0. 0. 0. 1. 0.]
 [0. 0. 0. 0. 1.]]

(4, 6)
[[1. 0. 0. 0. 0. 0.]
 [0. 1. 0. 0. 0. 0.]
 [0. 0. 1. 0. 0. 0.]
 [0. 0. 0. 1. 0. 0.]]
```

## All ones or all zeros:

## Zeros & Ones:

```python
import numpy as np
zeros = np.zeros((4,6))
ones = np.ones((4,6))
print(zeros)
print(ones)
```

### Output:

```python
[[0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0. 0.]]

[[1. 1. 1. 1. 1. 1.]
 [1. 1. 1. 1. 1. 1.]
 [1. 1. 1. 1. 1. 1.]
 [1. 1. 1. 1. 1. 1.]]
```

## Check Zero or non-zero values:

```python
print(zeros.all()) #if all the values are zero
print(identity.any()) #if any value is zero
```

### Output:

```python
False
True
```

## Generate a matrix with any values:

```python
any_val = np.full((5,6),5)
```

### Output:

```python
[[5 5 5 5 5 5]
 [5 5 5 5 5 5]
 [5 5 5 5 5 5]
 [5 5 5 5 5 5]
 [5 5 5 5 5 5]]
```

## Updating the value of one matrix:

```python
ones.fill(8)
```

### Output:

```python
[[8. 8. 8. 8. 8. 8.]
 [8. 8. 8. 8. 8. 8.]
 [8. 8. 8. 8. 8. 8.]
 [8. 8. 8. 8. 8. 8.]]
```

## Dot matrix multiplication:

```python
import numpy as np

x = np.array([[1,2],[4,5]])
y = np.array([[6,7],[8,9]])
z = 10 * np.dot(x,y)

print(z)

# z=10*[[1 2]]   [[6 7]]
#      [[4 5]] . [[8 9]]
```

### Output:

```python
[[220 250]
 [640 730]]
```

## Slicing of the array:

```python
import numpy as np

arr = np.arange(1,17).reshape((4,4))

print(arr[0,1:3])
#   for only getting output [2 3]

#   for [[6 7]   
#       [10 11]]
print(arr[1:3,1:3])
```

## Join 2 arrays:

```python
import numpy as np

arr = np.arange(1,17).reshape((4,4))
arr1 = np.arange(17,33).reshape((4,4))

print(arr)
print(arr1)

print(np.concatenate((arr,arr1)))
```

### Output:

```python
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]
 [13 14 15 16]]

[[17 18 19 20]
 [21 22 23 24]
 [25 26 27 28]
 [29 30 31 32]]

[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]
 [13 14 15 16]
 [17 18 19 20]
 [21 22 23 24]
 [25 26 27 28]
 [29 30 31 32]]
```

## Concatinate Sideways:

```python
import numpy as np

arr = np.arange(1,17).reshape((4,4))
arr1 = np.arange(17,33).reshape((4,4))

print(arr)
print(arr1)

print(np.concatenate((arr,arr1),axis=1))
```

### Output:

```python
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]
 [13 14 15 16]]

[[17 18 19 20]
 [21 22 23 24]
 [25 26 27 28]
 [29 30 31 32]]

[[ 1  2  3  4 17 18 19 20]
 [ 5  6  7  8 21 22 23 24]
 [ 9 10 11 12 25 26 27 28]
 [13 14 15 16 29 30 31 32]]
```

## Transpose:

```python
arr1 = np.arange(17,33).reshape((4,4))
print(arr1.T)
```

## Random Values in array:

```python
import numpy as np

arr = np.random.random(12).reshape((3,4))
print(arr)
arr1 = np.random.randint(1,10,16).reshape((4,4))
print(arr1)
```

### Output:

```python
[[0.20196779 0.90356296 0.98985798 0.57627894]
 [0.93208766 0.27371222 0.84561931 0.72160621]
 [0.61985613 0.02480519 0.39803434 0.66842008]]

[[6 5 7 5]
 [3 7 3 8]
 [8 3 8 8]
 [3 7 1 2]]
```

## For creating & load a file fom arrays:

```python
array.tofile("data.txt",sep = ',')
array = np.loadtxt("data.txt",delimeter = ',')
```

# Task:

```
https://www.teachoo.com/9723/1412/Trigonometry-Formulas/category/2-sin-x-sin-y-formula/
```
