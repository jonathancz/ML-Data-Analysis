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

* One of the key features of NumPy is its N-dimensional array object, or ndarray

* Fast, flexible container for large datasets in Python

* Refer to Jupyter Notebook "Chapter 4" for examples

* An ndarray is a generic multidimensional container for homogenous data

* In other words, all of the elements must be the same type

* Every array has a *shape*

**Creating ndarrays**

* For code, refer to jupyter notebook

**Data Types for ndarrays**

* The *data type *is a special object containing the information (or *metadata*, data about data) the ndarray needs to interpret a chunk of memory as a particular type of data

* dtypes are a source of NumPy’s flexibility for interacting with data from other systems.

* The numerical dtypes are named the same way: a type name, like *float *or *int*, followed by a number indicating the number of bits per element.

* A standard double-precision floating-point value takes up 8 bytes or 64 bits. 

* Thus, this type is known in NumPy as *float64*

* You can explicitly convert or *cast* an array from one dtype to another using ndarray’s *astype* method

* Calling *astype* always creates a new array (a copy of the data), even if the new dtype is the same as the old type.

**Arithmetic with NumPy Arrays**

* Arrays are important because they enable you to express batch operations on data without any *for *loops.

* NumPy users call this *vectorization*. 

* Any arithmetic operations between equal-size arrays applies the operation element-wise

**Basic Indexing and Slicing**

* NumPy array indexing is a rich topic

* You may want to select a subset of your data or individual elements

**Fancy Indexing**

* *Fancy indexing *is a term by NumPy to describe indexing using integer arrays.

* Keep in mind that fancy indexing, unlike slicing, always copies that data into a new array.

**Transposing Arrays and Swapping Axes**

* Transposing is a special form of reshaping that similarly returns a view on the underlying data without copying anything.

