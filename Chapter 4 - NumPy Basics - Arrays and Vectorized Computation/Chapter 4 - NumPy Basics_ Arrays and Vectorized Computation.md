# Numpy Basics: Arrays and Vectorized Computation

* * *


**NumPy**

* NumPy, short of Numerical Python, is one of the most important foundational packages for numerical computing in Python.

* Most computational packages providing scientific functionality use NumPy’s array objects as the *lingua franca *for data exchange.

* Here are some of the things you’ll find in NumPy:

    * Ndarray, an efficient multidimensional array providing fast array-oriented arithmetic operations and flexible *broadcasting *capabilities.

    * Mathematical functions for fast operations on entire arrays of data without having to write loops

    * Tools for reading/writing data to disk and working with memory-mapped files.

    * Linear Algebra, random number generation, and Fourier transform capabilities.

    * A C API for connecting NumPy with libraries written in C, C++, or FORTRAN

* One of the reasons NumPy is so important for numerical computations in Python is because it is designed for efficiency on large arrays of data. There are a number of reasons for this:

    * NumPy internally stores data in a contiguous block of memory, independent of other built-in Python objects. NumPy arrays also use much less memory than built-in Python sequences.

    * NumPy operations perform complex computations on entire arrays without the need for Python *for *loops.

**The NumPy ndarray: A Multidimensional Array Object**

