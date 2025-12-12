# Numpy
![img_2.png](img_2.png)
![img.png](img.png)
First Cell: `2**1000`

This calculation is performed using Python's built-in integers. Python's integers can grow arbitrarily large because they are implemented as arbitrary-precision numbers. Therefore, the result of 2**1000 is displayed correctly as a very large number.

Second and Third Cell:
```python
import numpy as np  
np.int64(2)**1000  
```
Here, you are explicitly converting the number 2 to a NumPy int64 type. Unlike Python's native integers, int64 has a fixed size of 64 bits. The maximum value an int64 can represent is 
2
63
−
1
=
9
,
223
,
372
,
036
,
854
,
775
,
807
2 
63
 −1=9,223,372,036,854,775,807 (positive range for signed integers). Any number exceeding this range will overflow, causing undefined or incorrect results.

In this case, 2**1000 is far larger than the maximum value int64 can handle. The computation overflows and wraps around, eventually resulting in 0.

## Another example
![img_1.png](img_1.png)
![img_3.png](img_3.png)
![img_4.png](img_4.png)


# Numba
![img_5.png](img_5.png)
![img_6.png](img_6.png)
![img_7.png](img_7.png)
![img_8.png](img_8.png)
![img_9.png](img_9.png)

# Cython
![img_10.png](img_10.png)
![img_11.png](img_11.png)
notice the cython version code difference
![img_12.png](img_12.png)
![img_13.png](img_13.png)
compile once code ready
![img_14.png](img_14.png)
![img_15.png](img_15.png)
![img_17.png](img_17.png)
![img_16.png](img_16.png)
Be aware that Cython may not always outperform pure Python, especially for small or simple functions where the overhead of compilation and type declarations may outweigh the benefits.
Besides, Cython adds complexity to the development process, as it requires an additional compilation step and may introduce compatibility issues with pure Python code.
If your platform changes, the Cython-compiled modules may need to be recompiled to ensure compatibility.

# PyPy
# todo: continue