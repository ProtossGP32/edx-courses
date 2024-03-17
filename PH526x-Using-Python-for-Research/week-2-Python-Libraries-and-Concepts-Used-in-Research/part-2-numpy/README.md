# Part 2: NumPy

## 2.2.1: Introduction to NumPy Arrays

Video here: [\[LINK\]](media/2.2.1-introduction-to-numpy-arrays.mp4)

Check the notebook example [2.2.1-introduction-to-numpy-arrays](scripts/2.2.1-introduction-to-numpy-arrays.ipynb)

### GOALS:

- Learn how to import NumPy
- Learn how to create simple NumPy arrays, including vectors and matrices of zeros and ones

### What is NumPy?

NumPy is a Python module designed for scientific computation with several very useful features:

- NumPy arrays are n-dimensional array objects, a core component of cientific and numerical computation in Python
- NumPy also provides tools for integrating your code with existing C, C++ and Fortran code
- NumPy also provides useful tools to help you perform linear algebra, generate random numbers, etc.

### What are NumPy arrays?

NumPy arrays are an additional data type provided by NumPy, and they are used for **representing vectors and matrices**.

- Unlike dynamically growing Python lists, NumPy arrays have a size that is fixed when they are constructed
- Elements of NumPy arrays are also all of the same data type, leading to more efficient and simpler code than using Python's standard data types
- The default data type of NumPy arrays are floating point numbers

### Initializing NumPy arrays

- `numpy.zeros(shape)`: initializes a numpy array filled with zeros with the provided shape
- `numpy.ones(shape)`: initializes a numpy array filled with ones with the provided shape
- `numpy.empty(shape)`: initializes a numpy array filled with empty values with the provided shape. This is useful if you are dealing with a very large array and you know for sure that you will be updating each element of the array before accessing them, saving Python some computation time.
  
  > :warning: Be careful here as NumPy allocates the requested space in memory but it doesn't initialize it, meaning that the content could be anything, whatever happens to be the computer's memory at the location where the array is set up

- `numpy.array(values)`: initializes a numpy array filled with the provided values in the input argument (typically a list of numbers)

### Transposing a matrix

We can transpose a NumPy array by using its `transpose()` method.

### Comprehension check

Please check the lesson's notebook for any question not explained here.

#### Question 1

True or False: a `numpy` array's length may be modified after being created.

- False: NumPy pre-allocates the memory space of the array. For this it needs to know its shape and it can't be changed afterwards

## 2.2.2: Slicing NumPy Arrays

Video here: [\[LINK\]](media/2.2.2-slicing-numpy-arrays.mp4)

Check the notebook example [2.2.2-slicing-numpy-arrays](scripts/2.2.2-slicing-numpy-arrays.ipynb)

### GOALS:

- Learn how to slice NumPy arrays

### Accessing array values

- With one-dimensional arrays, we specify the index of the element we want to access just like accessing lists
- With two-dimensional arrays, we specify the index of the row and the column we want to access

### Slicing arrays

- With one-dimensional arrays, we specify the range of the elements we want to slice just like slicing lists
- With two-dimensional arrays, we specify the range of elements for rows and columns to slice

### Algebraic operations

Careful with aditions! Remember that `list` built-in class concatenates lists when using the `+` operator, but NumPy arrays do an element-wise addition between the two arrays, returning an array of the same length as them.

### Comprehension check

Please check the lesson's notebook for any question not explained here.

## 2.2.3: Indexing NumPy Arrays

Video here: [\[LINK\]](media/2.2.3-indexing-numpy-arrays.mp4)

Check the notebook example [2.2.3-indexing-numpy-arrays](scripts/2.2.3-indexing-numpy-arrays.ipynb)

### GOALS

- Learn how to index NumPy arrays with other arrays or sequence-like objects
- Learn an important distinction between slicing an array and indexing an array

### Indexing arrays

We can use `list` or `np.array` filled with index values to then be passed as arguments of another `np.array` and then retrieve their indexed values

We can also create **boolean arrays**:

- Boolean arrays, also called Logical arrays, are arrays whose value (`True` or `False`) is the result of a clause applied to each NumPy array value:
  ```python
  z1 = np.array([1, 3, 5, 7, 9])
  # Return the boolean array of z1 depending on whether its values are > 6
  z1 > 6
  # It returns: array([False, False, False,  True,  True])
  ```
- Logical arrays can be used to index another vector. As the operation returns a NumPy array, it can be directly used as the input range of an existing array:
  ```python
  z1[z1 > 6]
  # It returns: array([7, 9])
  ```

> [!NOTE]
> Remember that when you **slice an array** using the colon operator, **you get a view of the object**. This means that **if you modify it, the original array will also be modified**.
>
> This is contrast with what happens when you **index an array**, in which case **what is returned to you is a copy of the original data**.


### Comprehension check

Please check the lesson's notebook for questions not explained here.

## 2.2.4: Building and Examining NumPy Arrays

Video here: [\[LINK\]](media/2.2.4-building-and-examining-numpy-arrays.mp4)

Check the notebook example [2.2.4-building-and-examining-numpy-arrays](scripts/2.2.4-building-and-examining-numpy-arrays.ipynb)

### GOALS

- Learn how to construct NumPy arrays using `np.linspace()` and `np.logspace`
- Learn how to check the **shape** and **size** of an array
- Learn how to determine whether the elements of an array fulfill a logical condition using `np.any()` and `np.all()`


### Useful array building methods

- `np.linspace()`: it returns an array of linearly spaced elements
  - First argument: the starting point
  - Second argument: the ending point, included
  - Third argument: the number of points we want
- `np.logspace()`: it returns an array of logarithmically spaced elements
  - First argument: log of the starting point --> i.e: log(10) = 1
  - Segond argument: log of the ending point --> i.e: log(100) = 2
  - Third argument: number of elements in our array


### Shape and size

- `np.array.shape`: returns the length of each dimension of the array
- `np.array.size`: returns the total number of elements in that array

> [!NOTE]
> Notice how `np.shape` and `np.size` don't have parenthesis. That's because they are NumPy array data attributes, not methods.


### Logical conditioning on an array's values

- `np.any()`: returns `True` or `False` depending on the logical condition passed as a parameter
  - If any logical condition applied to a member of the array is `True`, then `np.any()` returns `True`
  - Else, it returns `False`
- `np.all()`: returns `True` or `False` depending on the logical condition passed as a parameter
  - If thelogical condition applied to all members of the array is `True`, then `np.any()` returns `True`
  - Else, it returns `False`

### Comprehension check

Please check the lesson's notebook for questions not explained here.