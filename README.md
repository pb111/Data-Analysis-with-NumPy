# Data Analysis with NumPy

NumPy is the fundamental library of Python which is required for scientific computing. In this project, I will explore NumPy and various data analysis tools of NumPy.


## Table of contents


The table of contents for this project is as follows:-


1.	Introduction to NumPy

2.	Key features of NumPy

3.	Advantages of NumPy

4.	Importing NumPy

5.	Import data

6.	Dataset description

7.	NumPy ndarray object

8.	NumPy data types

9.	NumPy array attributes

10.	NumPy array creation 

11.	NumPy array from existing data

12.	NumPy array from numerical ranges

13.	NumPy array manipulation

14.	NumPy indexing and slicing

15.	NumPy Broadcasting

16.	NumPy binary operators

17.	NumPy string functions

18.	NumPy arithmetic operations

19.	NumPy statistical functions

20.	NumPy sorting

21.	NumPy searching

22.	NumPy copies and views

23.	Input output with NumPy

24.	Random sampling with NumPy


================================================================================


## 1. Introduction to NumPy

**NumPy** is a Python package. It stands for **Numerical Python**. It is the fundamental package for scientific computing in Python. It is the Python library that provides multidimensional array objects, various derived objects and a collection of routines for processing of array. NumPy is used to perform mathematical, logical, shape manipulation, sorting, selecting, input output, linear algebra, statistical operations and random simulation on arrays.

The ancestor of NumPy was Numeric. It was originally created by Jim Hugunin with contributions from several other developers. Another package Numarray was also developed, having some additional functionalities. In 2005, Travis Oliphant created NumPy package by incorporating the features of Numarray into Numeric package. Since, then the NumPy community has grown extensively. So, NumPy is an open source software and has many contributors.

NumPy is the subject matter of this project. I will discuss NumPy and various data analysis tools associated with NumPy.


================================================================================


## 2. Key features of NumPy


The key features of NumPy are as follows:-
1.	NumPy is designed for scientific computation with Python.
2.	NumPy provides tools for array oriented computing.
3.	It efficiently implemented multi-dimensional arrays.
4.	NumPy arrays have a fixed size at creation. We can change the size of the array. It will create a new array and delete the original. 
5.	At the core of the NumPy package, is the ndarray object. This encapsulates n-dimensional arrays of homogeneous data types
6.	The elements in a NumPy array are all required to be of the same data type.


================================================================================


## 3. Advantages of NumPy
      Advantages of NumPy are as follows:-
1.	NumPy enable us to perform mathematical and logical operations on arrays.
2.	It provides tools to perform Fourier transformation and routines for shape manipulation.
3.	NumPy can perform operations related to linear algebra.  NumPy has in-built functions for linear algebra and random number generation.
4.	NumPy arrays facilitate advanced mathematical and other types of operations on large datasets. 
5.	A large number of Python packages uses NumPy arrays. These support Python-sequence inputs. They convert such input to NumPy arrays prior to processing, and they often output NumPy arrays.


================================================================================


## 4. Importing NumPy
In order to use NumPy in our work, we need to import the NumPy library first. We can import the NumPy library with the following command:-
`import numpy`
Usually, we import the NumPy library by appending the alias `as np`.  It makes things easier because now instead of writing `numpy.command` we need to write `np.command`. So, I 
will import the numpy library with the following command:-
`import numpy as np`
Also, I will import Pandas as well which is the open source library for data analysis in Python. I will import Pandas with the following command:-
`import pandas as pd`


================================================================================


## 5. Importing data
In this project, I work with the **Forest Fires Data Set** which is a comma-separated values (CSV) file type. In a CSV file type, the data is stored as a comma-separated values where each row is separated by a new line, and each column by a comma (,).
I use the **pandas read_csv()** function to import the data set as follows:-
`data = 'C:/datasets/forestfires.csv`
`df = pd.read_csv(data)`


================================================================================


## 6. Dataset description
I have used the **Forest Fires** dataset for this project. The dataset represents the burned area of forest fires using meteorological data.
### Attribute Information -
The dataset contains 517 instances and 13 attributes. The attribute information is as follows:-
- 1. X - x-axis spatial coordinate within the Montesinho park map: 1 to 9 
- 2. Y - y-axis spatial coordinate within the Montesinho park map: 2 to 9 
- 3. month - month of the year: 'jan' to 'dec' 
- 4. day - day of the week: 'mon' to 'sun' 
- 5. FFMC - FFMC index from the FWI system: 18.7 to 96.20 
- 6. DMC - DMC index from the FWI system: 1.1 to 291.3 
- 7. DC - DC index from the FWI system: 7.9 to 860.6 
- 8. ISI - ISI index from the FWI system: 0.0 to 56.10 
- 9. temp - temperature in Celsius degrees: 2.2 to 33.30 
- 10. RH - relative humidity in %: 15.0 to 100 
- 11. wind - wind speed in km/h: 0.40 to 9.40 
- 12. rain - outside rain in mm/m2 : 0.0 to 6.4 
- 13. area - the burned area of the forest (in ha): 0.00 to 1090.84 
(area variable is very skewed towards 0.0, thus it may make sense to model with the logarithm transform).


I have downloaded this dataset from the UCI machine learning repository from the following url:-


https://archive.ics.uci.edu/ml/datasets/Forest+Fires
In this project, I will analyze this dataset using NumPy, which is a commonly used Python data analysis package.


================================================================================


## 7. NumPy ndarray object

The most important object defined in NumPy is an N-dimensional array called **ndarray**. It describes the collection of items of the same type. Items in the collection can be accessed using a zero-based index. Each element in ndarray is an object of data-type object (called dtype).

An instance of ndarray class can be constructed by different array creation routines. The basic ndarray is created using an array function in NumPy with the following code snippet as follows:−

`numpy.array(object, dtype=None, copy=True, order=None, subok=False, ndmin=0)`


The above constructor takes the following parameters:−


- object - Any object exposing the array interface method returns an array, or any (nested) sequence.


- dtype - Desired data type of array, optional


- copy - (Optional) - By default (true), the object is copied


- order - C (row major) or F (column major) or A (any) (default)


- subok - By default, returned array forced to be a base class array. If true, sub-classes passed through


- ndmin - Specifies minimum dimensions of resultant array

Now, I will illustrate the concept better with the following examples:-


### one dimensional array

`np.array([1,2,3])`



### two dimensional array

`np.array([[1, 2], [3, 4]])`


### three dimensional array

`np.array([[1,2],[3,4],[5,6]])`


### minimum dimensions 

`np.array([1, 2, 3, 4, 5], ndmin = 2)`


### dtype parameter 

`np.array([1, 2, 3], dtype = complex)`


================================================================================


## 8. NumPy data types

NumPy supports a much greater variety of numerical data types than Python. The following table shows most common data types defined in NumPy.

- bool_ - Boolean (True or False) stored as a byte


- int_ - Default integer type (same as C long; normally either int64 or int32)


- intc - Identical to C int (normally int32 or int64)


- intp - Integer used for indexing (same as C ssize_t; normally either int32 or int64)


- int8 - Byte (-128 to 127)


- int16 - Integer (-32768 to 32767)


- int32 - Integer (-2147483648 to 2147483647)

	
- int64 - Integer (-9223372036854775808 to 9223372036854775807)


- float_ - Shorthand for float64

	
- float16 - Half precision float: sign bit, 5 bits exponent, 10 bits mantissa

	
- float32 - Single precision float: sign bit, 8 bits exponent, 23 bits mantissa

	
- float64 - Double precision float: sign bit, 11 bits exponent, 52 bits mantissa



NumPy numerical types are instances of dtype (data-type) objects, each having unique characteristics. The dtypes are available as np.bool_, np.float32, etc.



A dtype object is constructed using the following syntax:-


`numpy.dtype(object, align, copy)`


The parameters are:−


`Object` − To be converted to data type object.


`Align` − If true, adds padding to the field to make it similar to C-struct.


`Copy` − Makes a new copy of dtype object. If false, the result is reference to builtin data type object.



Each built-in data type has a character code that uniquely identifies it.


'b' − boolean

'i' − (signed) integer

'u' − unsigned integer

'f' − floating-point

'c' − complex-floating point

'm' − timedelta

'M' − datetime

'O' − (Python) objects

'S', 'a' − (byte-)string

'U' − Unicode

'V' − raw data (void)

The following example demonstrate the creation of NumPy data type objects:-

using array-scalar type 
`dt = np.dtype(np.int32)`
`print(dt)`


The following examples show the use of structured data type. The field name and the corresponding scalar data type is to be declared.

first create structured data type 
 
`dt = np.dtype([('age',np.int8)])`

`print(dt)`
now apply it to ndarray object 

`dt = np.dtype([('age',np.int8)])` 

`a1 = np.array([(10,),(20,),(30,)], dtype = dt)`

`print(a1)`


file name can be used to access content of age column 

`dt = np.dtype([('age',np.int8)])`

`a1 = np.array([(10,),(20,),(30,)], dtype = dt)`

`print(a1['age'])`


The following example define a structured data type called student with a string field `name`, an integer field `age` and a float field `marks`. This dtype is applied to ndarray object as follows:-

`student = np.dtype([('name','S20'), ('age', 'i1'), ('marks', 'f4')])`

`print(student)`




`a2 = np.array([('abc', 21, 50),('xyz', 18, 75)], dtype = student)`

`print(a2)`


================================================================================


## 9. NumPy array attributes

In this section, I will discuss the various NumPy array attributes. The attributes are **ndarray.shape**, **ndarray.ndim**, **ndarray.size**, **ndarray.itemsize**, **ndarray.dtype**, **ndarray.data**.

### ndarray.shape

This array attribute returns a tuple consisting of array dimensions. It can also be used to resize the array. For a matrix with n rows and m columns, shape will be (n,m). The length of the shape tuple is therefore the number of axes, ndim.

`x1 = np.array([[1,2,3],[4,5,6]])`
`print(x1.shape)`


resizes the ndarray 

`x2 = np.array([[1,2,3],[4,5,6]])`

`x2.shape = (3,2)`



### ndarray.size

It returns the total number of elements of the array. This is equal to the product of the elements of shape.

print the size of the x1 array

`print(x1.size)`


### reshape function

NumPy also provides a reshape function to resize an array.

`x1 = np.array([[1,2,3],[4,5,6]])`

`x1_reshaped = x1.reshape(3,2)`


### ndarray.ndim

This array attribute returns the number of axes (dimensions) of the array.

create an array of evenly spaced numbers 

`x3 = np.arange(24)`

confirm that the above array is a one dimensional array 
 
`x3 = np.arange(24)`

reshape the above array

`x4 = x3.reshape(2,4,3)`

x4 have three dimensions.


### ndarray.itemsize

This array attribute returns the size in bytes of each element of the array. For example, an array of elements of type float64 has itemsize 8 (=64/8), while one of type complex32 has itemsize 4 (=32/8). It is equivalent to ndarray.dtype.itemsize.

dtype of array is int8 (1 byte) 
 
`x5 = np.array([1,2,3,4,5], dtype = np.int8)`

`print(x5.itemsize)`


dtype of array is now float32 (4 bytes) 

`x6 = np.array([1,2,3,4,5], dtype = np.float32)`

`print(x6.itemsize)`

### ndarray.dtype

It represents an object describing the type of the elements in the array. We can create or specify dtype’s using standard Python types. Additionally NumPy provides its own dtypes as follows:-

`numpy.int32`, `numpy.int16` and `numpy.float64`.


### type of array

We can check the type of the array with the `type()` function.


================================================================================


## 10. NumPy array creation 


A new ndarray object can be constructed by any of the following array creation routines. There are several ways to create arrays. These are listed below:-

- array() function


### array() function

We can create an array from a regular Python list or tuple using the array function. The type of the resulting array is deduced from the type of the elements in the sequences.

create an array

`x7 = np.array([2,3,4])`

check its dtype

`x7.dtype`


### empty function

The function **empty** creates an array whose initial content is random and depends on the state of the memory. By default, the dtype of the created array is float64.

The following code shows an example of an empty array:-

`x9 = np.empty([2,3], dtype = int)`





### zeros function

The function **zeros** creates an array full of zeros. By default, the dtype of the created array is float.

The following examples demonstrate the use of the zeros function:-

array of five zeros

`x10 = np.zeros(5)`

`x11 = np.zeros((5,), dtype = np.int)`


### ones function

The function **ones** creates an array full of ones. The default dtype is float.

`x12 = np.ones(5)`

dtype can also be specified

`x13 = np.ones([2,2], dtype=int)`





### arange function

The **arange** function creates sequences of numbers. It is analogous to range that returns arrays instead of lists.

`x14 = np.arange(10, 20, 2)`

arange function with float arguments

`x15 = np.arange(10, 20, 0.5)`


When **arange** function is used with floating point arguments, it is not possible to predict the number of elements obtained, due to the finite floating point precision. So, it is better to use the **linspace** function that accepts the number of elements argument that we want, instead of the step.


================================================================================


## 11. NumPy array from existing data

In this section, I will discuss how to create an array from existing data.

### numpy.asarray

This function is similar to numpy.array except for the fact that it has fewer parameters. This routine is useful for converting Python sequence into ndarray.

The syntax of this function is as follows:-

`numpy.asarray(a, dtype = None, order = None)`



The constructor takes the following parameters.


- a - Input data in any form such as list, list of tuples, tuples, tuple of tuples or tuple of lists.

	

- dtype - By default, the data type of input data is applied to the resultant ndarray.


	
- order - C (row major) or F (column major). C is default.

The following examples show the use of the asarray function:-

convert list to ndarray 

`u1 = [1,2,3]`

`v1 = np.asarray(u1)`


dtype is set 

`u1 = [1,2,3]`

`v1 = np.asarray(u1, dtype=float)`


ndarray from tuple

`u2 = (1,2,3)` 

`v2 = np.asarray(u2)`


ndarray from list of tuples 

`u3 = [(1,2,3),(4,5)]`

`v3 = np.asarray(u3)`
### numpy.frombuffer


This function interprets a buffer as one-dimensional array. Any object that exposes the buffer interface is used as parameter to return an ndarray. Its syntax is as follows:-


`numpy.frombuffer(buffer, dtype = float, count = -1, offset = 0)`



The constructor takes the following parameters.


	
- buffer - Any object that exposes buffer interface

	
    
- dtype - Data type of returned ndarray. Defaults to float



- count - The number of items to read, default -1 means all data



- offset - The starting position to read from. Default is 0
### numpy.fromiter



This function builds an ndarray object from any iterable object. A new one-dimensional array is returned by this function.


Its syntax is as follows:-


`numpy.fromiter(iterable, dtype, count = -1)`



The constructor takes the following parameters.


	
- iterable - Any iterable object

	
- dtype - Data type of resultant array

	
- count - The number of items to be read from iterator. Default is -1 which means all data to be read.


================================================================================


## 12. Numpy array from numerical ranges


In this section, I will discuss how to create an array from numerical ranges.

### numpy.arange

This function returns an ndarray object containing evenly spaced values within a given range. The syntax of the function is as follows −

`numpy.arange(start, stop, step, dtype)`

The description of the parameters is as follows:-

- start - The start of an interval. If omitted, defaults to 0

- stop - The end of an interval (not including this number)

- step - Spacing between values, default is 1

- dtype - Data type of resulting ndarray. If not given, data type of input is used.

The following examples demonstrate the use of this function.

`y1 = np.arange(5)` 



dtype set

`y1 = np.arange(5, dtype = float)`


start and stop parameters set

`y1 = np.arange(10,20,2)`



### numpy.linspace

This function is similar to arrange () function. In this function, instead of step size, the number of evenly spaced values between the intervals is specified. The syntax of this function is as follows:−

`numpy.linspace(start, stop, num, endpoint, retstep, dtype)`

The description of the parameters is as follows:-

- start - The starting value of the sequence

	
- stop - The end value of the sequence, included in the sequence if endpoint set to true

	
- num - The number of evenly spaced samples to be generated. Default is 50.


- endpoint - True by default, hence the stop value is included in the sequence. If false, it is not included.


- retstep - If true, returns samples and step between the consecutive numbers


- dtype - Data type of output ndarray

The following examples demonstrate the use of linspace function.

create an array

`y2 = np.linspace(10,20,5)`

endpoint set to false 

`y2 = np.linspace(10,20, 5, endpoint = False)`



### numpy.logspace


This function returns an ndarray object that contains the numbers that are evenly spaced on a log scale. Start and stop endpoints of the scale are indices of the base, usually 10. Its syntax as follows:-


`numpy.logspace(start, stop, num, endpoint, base, dtype)`


The description of the parameters is as follows:-


	
- start - The starting point of the sequence is basestart

	
- stop - The final value of sequence is basestop

	
- num - The number of values between the range. Default is 50

	
- endpoint - If true, stop is the last value in the range

	
- base - Base of log space, default is 10

	
- dtype - Data type of output array. If not given, it depends upon other input arguments


================================================================================


## 13. NumPy array manipulation



NumPy package provides several routines for manipulation of elements in ndarray object. These routines can be classified into the following types:−



### Changing shape


- **reshape** - gives a new shape to an array without changing its data


- **flat** - A 1-D iterator over the array


- **flatten** - returns a copy of the array collapsed into one dimension


- **ravel** - returns a contiguous flattened array




### Transpose operations



- **transpose** - permutes the dimensions of an array


- **ndarray.T** - same as self.transpose()


- **rollaxis** - rolls the specified axis backwards


- **swapaxes** - interchanges the two axes of an array




### Changing dimensions


- **broadcast** - produces an object that mimics broadcasting


- **broadcast_to** - broadcasts an array to a new shape


- **expand_dims** - expands the shape of an array


- **squeeze** - removes single-dimensional entries from the shape of an array




### Joining arrays


- **concatenate** - joins a sequence of arrays along an existing axis


- **stack** - joins a sequence of arrays along a new axis


- **hstack** - stacks arrays in sequence horizontally (column wise)


- **vstack** - stacks arrays in sequence vertically (row wise)




### Splitting arrays


- **split** - splits an array into multiple sub-arrays


- **hsplit** - splits an array into multiple sub-arrays horizontally (column-wise)


- **vsplit** - splits an array into multiple sub-arrays vertically (row-wise)




### Adding or removing elements



- **resize** - returns a new array with the specified shape


- **append** - appends the values to the end of an array


- **insert** - inserts the values along the given axis before the given indices


- **delete** - returns a new array with sub-arrays along an axis deleted


- **unique** - finds the unique elements of an array


================================================================================


## 14. NumPy indexing and slicing


In NumPy, the elements of ndarray object can be accessed and modified by indexing or slicing, just like in Python. The items in ndarray object follows zero-based index. 

Three types of indexing methods are available − 


- 1. **field access** 


- 2. **basic slicing**  


- 3. **advanced indexing**


### Basic slicing


Basic slicing is an extension of Python's basic concept of slicing to n dimensions. A Python slice object is constructed by giving start, stop, and step parameters to the built-in slice function. This slice object is passed to the array to extract a part of an array.


The following examples illustrate the idea:-

`x18 = np.arange(10)`

`s = slice(2,7,2)` 

`print(x18[s])`


In the above example, an ndarray object is created by **arange()** function. Then a slice object is defined with start, stop and step values 2, 7 and 2 respectively. This slice object is then passed to the ndarray. A part of the ndarray starting with index 2 up to 7 with a step of 2 is sliced.


The same result can also be obtained by giving the slicing parameters separated by a colon : (start:stop:step) directly to the ndarray object as follows:-

`x19 = x18[2:7:2]`


If only one parameter is put, a single item corresponding to the index will be returned.

`x18 = np.arange(10)`

`x20 = x18[5]`


If a : is inserted in front of it, all items from that index onwards will be extracted.

slice items starting from index 

`x18 = np.arange(10)`

`print(x18[2:])`


If two parameters (with : between them) is used, items between the two indexes (not including the stop index) with default step one are sliced.

`x18 = np.arange(10)`

`print(x18[2:5])`


The above description applies to multi-dimensional ndarray too.

`x20 = np.array([[1,2,3],[3,4,5],[4,5,6]])`


slice items starting from index

`print(x20[1:])`


slice array of items in the second column 
 
`print(x20[...,1])`


slice all items from the second row 

`print(x20[1,...])`


slice all items from column 1 onwards 
 
`print(x20[...,1:])`


================================================================================


## 15. NumPy broadcasting


In NumPy, **broadcasting** refers to the ability of NumPy to treat arrays of different shapes during arithmetic operations. Arithmetic operations on arrays are usually done on corresponding elements. If two arrays are of exactly the same shape, then these operations are smoothly performed.


However, if the dimensions of two arrays are dissimilar, element-to-element operations are not possible. Operations on arrays 
of different shapes is still possible in NumPy, because of the broadcasting capability. The smaller array is broadcast to the size of the larger array so that they have compatible shapes.


### Rules of broadcasting


Rules of broadcasting are as follows:- 



- 1. Array with smaller ndim than the other is prepended with '1' in its shape.



- 2. Size in each dimension of the output shape is maximum of the input sizes in that dimension.


- 3. An input can be used in calculation, if its size in a particular dimension matches the output size or its value is exactly 1.


- 4. If an input has a dimension size of 1, the first data entry in that dimension is used for all calculations along that dimension.




### Broadcast arrays



A set of arrays is said to be broadcastable if the above rules produce a valid result and one of the following is true:−


- 1. Arrays have exactly the same shape.


- 2. Arrays have the same number of dimensions and the length of each dimension is either a common length or 1.


- 3. Array having too few dimensions can have its shape prepended with a dimension of length 1, so that the above stated property is true.


================================================================================


## 16. NumPy - Binary Operators


There are several functions available for bitwise operations in NumPy package. These are as follows:-



- **bitwise_and** - Computes bitwise AND operation of array elements


- **bitwise_or** - Computes bitwise OR operation of array elements


- **invert** - Computes bitwise NOT


- **left_shift** - Shifts bits of a binary representation to the left


- **right_shift** - Shifts bits of binary representation to the right


================================================================================


## 17.	NumPy string functions


The following functions are used to perform vectorized string operations for arrays of dtype numpy.string_ or numpy.unicode_. They are based on the standard string functions in Python's built-in library.


- **add()** - Returns element-wise string concatenation for two arrays of str or Unicode


- **multiply()** - Returns the string with multiple concatenation, element-wise


- **center()** - Returns a copy of the given string with elements centered in a string of specified length


- **capitalize()** - Returns a copy of the string with only the first character capitalized


- **title()** - Returns the element-wise title cased version of the string or unicode


- **lower()** - Returns an array with the elements converted to lowercase


- **upper()** - Returns an array with the elements converted to uppercase


- **split()** - Returns a list of the words in the string, using separatordelimiter


- **splitlines()** - Returns a list of the lines in the element, breaking at the line boundaries


- **strip()** - Returns a copy with the leading and trailing characters removed


- **join()** - Returns a string which is the concatenation of the strings in the sequence


- **replace()** - Returns a copy of the string with all occurrences of substring replaced by the new string


- **decode()** - Calls str.decode element-wise


- **encode()** - Calls str.encode element-wise


================================================================================


## 18. NumPy arithmetic operations

Arithmetic operators on arrays apply elementwise. A new array is created and filled with the result.

Input arrays for performing arithmetic operations such as add(), subtract(), multiply(), and divide() must be either of the same shape or should conform to array broadcasting rules.


create two arrays

`z1 = np.array([10,20,30,40,50])`

`z2 = np.arange(5)`

addition

`z_add = z1 + z2`

subtraction

`z_sub = z1 - z2`

multiplication - elementwise product

`z_mult = z1 * z2`

division

`z_div = z1/2`

comparision operator

`z1 < 35`


Some of the other important arithmetic functions available in NumPy are as follows:-


- **numpy.reciprocal()**


This function returns the reciprocal of argument, element-wise. For elements with absolute values larger than 1, the result is always 0 because of the way in which Python handles integer division. For integer 0, an overflow warning is issued.


- **numpy.power()**


This function treats elements in the first input array as base and returns it raised to the power of the corresponding element in the second input array.


- **numpy.mod()**


This function returns the remainder of division of the corresponding elements in the input array. The function numpy.remainder() also produces the same result.



The following functions are used to perform operations on array with complex numbers.


- **numpy.real()** − returns the real part of the complex data type argument.


- **numpy.imag()** − returns the imaginary part of the complex data type argument.


- **numpy.conj()** − returns the complex conjugate, which is obtained by changing the sign of the imaginary part.


- **numpy.angle()** − returns the angle of the complex argument. The function has degree parameter. If true, the angle in the degree is returned, otherwise the angle is in radians.


================================================================================


## 19. NumPy - Statistical Functions


NumPy has various useful statistical functions for finding minimum, maximum, percentile, standard deviation and variance, from the given elements in the array. 

These functions are explained as follows:−

**numpy.amin()** and **numpy.amax()**

These functions return the minimum and the maximum from the elements in the given array along the specified axis.


For rows, axis = 1

For columns, axis = 0


Create an array

`i1 = np.array([[1,2,3],[4,5,6],[7,8,9]])`


Applying amin() function across rows

`print(np.amin(i1,1))`


Applying amin() function across columns

`print(np.amin(i1,0))`




Applying amax() function across rows

`print(np.amax(i1,1))`


Applying amax() function across columns

`print(np.amax(i1,0))`


### numpy.ptp()

The **numpy.ptp()** function returns the range (maximum-minimum) of values along an axis.

Applying ptp() function

`print(np.ptp(i1))`

Applying ptp() function along rows

`print(np.ptp(i1, axis = 1))`

Applying ptp() function along columns

`print(np.ptp(i1, axis = 0))`



### numpy.percentile()

Percentile is a measure used in statistics indicating the value below which a given percentage of observations in a group of observations fall.

Create an array

`i2 = np.array([[20,50,80],[30,60,90],[40,70,100]])`


Applying percentile() function

`print(np.percentile(i2,50))`



Applying percentile() function along rows

`print(np.percentile(i2,50,axis = 1))`


Applying percentile() function along columns

`print(np.percentile(i2,50,axis = 0))`



### numpy.median()

Median is defined as the value separating the higher half of a data sample from the lower half. The **numpy.median()** function is used as shown in the following program.

Applying median() function

`print(np.median(i2))`


Applying median() function across rows

`print(np.median(i2, axis=1))`


Applying median() function across columns

`print(np.median(i2, axis=0))`




### numpy.mean()

Arithmetic mean is the sum of elements along an axis divided by the number of elements. The **numpy.mean()** function returns the arithmetic mean of elements in the array.

Create an array

`i3 = np.array([[1,2,3],[3,4,5],[4,5,6]])`

Applying mean() function

`print(np.mean(i3))`


Applying mean() function along rows

`print(np.mean(i3, axis = 1))`


Applying mean() function along columns

`print(np.mean(i3, axis = 0))`






### numpy.average()

Weighted average is an average resulting from the multiplication of each component by a factor reflecting its importance. 

The **numpy.average()** function computes the weighted average of elements in an array according to their respective weight given in another array. The function can have an axis parameter. If the axis is not specified, the array is flattened.

Considering an array [1,2,3,4] and corresponding weights [4,3,2,1], the weighted average is calculated by adding the product of the corresponding elements and dividing the sum by the sum of weights.

Weighted average = (1*4+2*3+3*2+4*1)/(4+3+2+1)

Declare an array
`i4 = np.array([1,2,3,4])`

Print the array 
`print(i4)`


`print('Applying average() function:')`

`print(np.average(i4))`


specify weights

`wts = np.array([4,3,2,1])`

`print('Applying average() function with weights:')`

`print(np.average(i4,weights = wts))`


Returns the sum of weights, if the returned parameter is set to True.

`print('Sum of weights')`

`print(np.average([1,2,3,4],weights = [4,3,2,1], returned = True))`


### Variance

Variance is the average of squared deviations. It is given by **mean(abs(x - x.mean())**2)**.

calculation of variance

`i5 = np.array([1,2,3,4])`

`print(np.var(i5))`





### Standard Deviation

Standard deviation is the square root of the variance.

`print(np.std(i5))`


================================================================================


## 20. NumPy Sorting

NumPy provides various sorting related functions. These sorting functions implement different sorting algorithms and enable us to sort the array as we want. These sorting functions are as follows:-


### numpy.sort()



The **sort()** function returns a sorted copy of the input array. It has the following parameters:−



`numpy.sort(a, axis, kind, order)`



Description of the parameters is as follows:-



- a - Array to be sorted

	
- axis - The axis along which the array is to be sorted. If none, the array is flattened, sorting on the last axis

	
- kind - Default is quicksort

	
- order - If the array contains fields, the order of fields to be sorted


### numpy.argsort()


The **argsort()** function performs an indirect sort on input array, along the given axis and using a specified kind of sort to return the array of indices of data. This indices array is used to construct the sorted array.



### numpy.lexsort()


The **lexsort()** function performs an indirect sort using a sequence of keys. The keys can be seen as a column in a spreadsheet. The function returns an array of indices, using which the sorted data can be obtained. The last key happens to be the primary key of sort.


================================================================================


## 21. NumPy Searching

NumPy package has a number of functions for searching inside an array. These functions enable us to find the maximum, the minimum as well as the elements satisfying a given condition.

### numpy.argmax() and numpy.argmin()

These two functions return the indices of maximum and minimum elements respectively along the given axis.


### numpy.nonzero()

The **numpy.nonzero()** function returns the indices of non-zero elements in the input array.


### numpy.where()

The **where()** function returns the indices of elements in an input array where the given condition is satisfied.


### numpy.extract()

The **extract()** function returns the elements satisfying any condition.	


================================================================================


## 22. NumPy Copies and Views



While executing the functions, some of them return a copy of the input array, while some return the view. When the contents are physically stored in another location, it is called **Copy**. If on the other hand, a different view of the same memory content is provided, we call it as **View**.


### No Copy


Simple assignments do not make the copy of array object. Instead, it uses the same id() of the original array to access it. The **id()** returns a universal identifier of Python object, similar to the pointer in C.


Any changes in either gets reflected in the other too. For example, changing the shape of one will change the shape of the other too.



### View or Shallow Copy

NumPy has a **ndarray.view()** method which is a new array object that looks at the same data of the original array. In this case, change in dimensions of the new array doesn't change dimensions of the original.


### Deep Copy

The **copy()** function creates a deep copy. It is a complete copy of the array and its data, and doesn't share with the original array.


================================================================================


## 23. Input Output with NumPy



The ndarray objects can be saved to and loaded from the disk files. The input output functions available are as follows:−


- **load()** and **save()** functions handle /numPy binary files (with npy extension).


- **loadtxt()** and **savetxt()** functions handle normal text files.



NumPy introduces a simple file format for ndarray objects. It is called **.npy file**. This .npy file stores data, shape, dtype and other information required to reconstruct the ndarray in a disk file. The array is correctly retrieved even if the file is on another machine with different architecture.


### numpy.save()


The **numpy.save()** file stores the input array in a disk file with npy extension.






### savetxt()

The storage and retrieval of array data in simple text file format is done with **savetxt()** and **loadtxt()** functions.


The **savetxt()** and **loadtxt()** functions accept additional optional parameters such as header, footer, and delimiter.


================================================================================


## 24. Random sampling with NumPy


NumPy provides `random` module for doing random sampling. This `random` module contains many useful functions for generation of random numbers. 

There are several functions to generate simple random data. These functions are described below:-

### rand() function


This function creates an array of the given shape and populate it with random samples from a uniform distribution over [0, 1).


### randn() 

It returns a sample (or samples) from the "standard normal" distribution.


### randint()

It returns random integers from low (inclusive) to high (exclusive).


### random()

It returns random floats in the half-open interval [0.0, 1.0)


### choice()

It generates a random sample from a given 1-D array.



