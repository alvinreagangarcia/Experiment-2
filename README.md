1. NORMALIZATION PROBLEM

The first step was to import numpy as np so that certain codes can be done.
```python
import numpy as np
```
The next step was to create an array that generates random values by using .random.random(())
```python
x = np.random.random ((5,5))
```
Then the input for the mean and std given in the problem
```python
mean = x.mean ()
std = x.std ()
```
Then the input equation for the normalization of x
```python
Normalize_x = (x - mean) / std
```
By using print(), the output for the Normalize_x will show
```python
print(Normalize_x)
```
Finally saving the Normalized_x with the file name of X_normalized.npy
```python
np.save('X_Normalized.npy', Normalize_x)
```

2. DIVISIBLE BY 3
Initial step was to import numpy
```python
import numpy as np
```
Then setting up the array by using .arange() for the array to have a start and stop, then using .reshape to have a 10x10 array
```python
a = np.arange(1,101).reshape((10,10))
```
To square all the array, the use of ** in the equation was done, then setting a new variable with the copy of of the array
```python
a2 = a **2
a3 = a2.copy()
```
For the equation, by using a3 % 3 this divides the all the array by 3, then using the boolean mask !=0 sets whether the number is TRUE/FALSE if the number is divisible by 3, then =0 so that the numbers that are marked as FALSE will result as 0 in the output, thus showing only those that are divisible by 3
```python
a3[ a3 % 3 != 0 ] = 0
```
Then finally printing and saving the file with the name div_by_3
```python
print(a3)
np.save ('div_by_3',a3)
```

