# Array Broadcasting in NumPy
Description: Learn about the powerful concept of array broadcasting in NumPy, which allows for efficient arithmetic operations on arrays of different shapes.
Subjects: NumPy, Python, Data Science
Tags: NumPy, Array Broadcasting, Python

## Introduction
**Array broadcasting** in NumPy is a powerful mechanism that allows arithmetic operations on arrays of different shapes. It enables NumPy to handle element-wise operations without explicitly replicating the data, making calculations more efficient both in terms of memory and computation.

## Syntax
Broadcasting follows a set of rules to determine how arrays of different shapes are adjusted to match each other:
1. If arrays have a different number of dimensions, the shape of the smaller-dimensional array is padded with ones on its left side.
2. If the shapes of the arrays do not match in any dimension, the array with shape equal to 1 in that dimension is stretched to match the shape of the other array.
3. If in any dimension the sizes disagree and neither is 1, an error is raised.

## Example
Here's a simple example demonstrating broadcasting with two arrays of different shapes:

```python
import numpy as np

# Creating a 1D array
a = np.array([1, 2, 3])

# Creating a 2D array
b = np.array([[10], [20], [30]])

# Broadcasting the arrays
result = a + b

print(result)
Output:

[[11 12 13]
 [21 22 23]
 [31 32 33]] 
