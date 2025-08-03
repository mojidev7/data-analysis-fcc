NumPy Introduction


    Is the fundamental package for the numeric calculations in Python
    NumPy make Py very efficient, for example for a simple variable maybe 
    Py allocate upto 32 bits, but we can use numpy to specify the variable size
    like np.int8 np.int16 ...


    if we want to know how many bits required to store a number:
    2 ** n

    for example 2 ** 3 = 8 will handle the numbers from 0 to 7



NumPy Calculations


    a = np.array([1, 2, 3, 4])
    a[1] #2 
    a[-1] #4 -> last element
    a[1:-1] == a[1:3] #2, 3
    a[1:3] #2, 3, 4
    a[0:] #1, 2, 3, 4
    a[::2] #[start:stop:step] -> 1, 3
    multiple indexing -> a[[1, 2, -1]] #2, 3, 4



NumPy Array Type 

    a = np.array(1, 3, 5)
    a.dtype #dtype("int64")

    b = np.array(1, 0.3, 2)
    b.dtype #dtype("float64")

    b = np.array([1, 0.1, 3], dtype=np.int)
    b #array([1, 0, 3])



Numpy Array Dimensions

    ```python
    import numpy as np
    ```
    ```python
    a = np.array([
        [1,2,3],
        [4,5,6]
    ])
    ```
    ```python
    a.shape #(2, 3)
    ```
    ```python
    a.ndim #2
    ```
    ```python
    a.size #6
    ```