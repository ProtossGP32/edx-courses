# Part 1 - Objects and methods
## Python Basics
Video here: [[LINK]](media/1.1.1-python-basics.mp4)

### Python modes
Python has two different operating modes:

- Interactive mode: useful for testing code before importing to standard mode
- Standard mode: code stored in files and executed from start to end

### Python distributions
In this course we'll be using the [Anaconda Python distribution](https://www.continuum.io/downloads), supporting +300 packages. Anaconda also supports Jupyter and Spyder, used in this course.

### Comprehension check
#### Question 1
Python has two operating modes. Which are they:
- Interactive mode
- Standard mode

#### Question 2
Which of the following statements is NOT correct?
- Python 2 code will always work with Python 3.

## Objects
Video here: [[LINK]](media/1.1.2-objects.mp4)

### Meaning
All data in a Python program is represented by objects and by relationships between objects (thus it is an Object Oriented Programming Language).

- Object: it is a data representation

### Types of objects

- Mutable objects: objects whose value can change during the course of program execution
- Immutable objects: objects whose value is unchangeable after they've been created

### Object characteristics
Each object in Python has three characteristics:

- Object type: the kind of object we're dealing with (number, string, list, etc.)
  - Object types always determines the kind of operations that it supports
  - In other words, depending on the type of the object, different methods may be available
- Object value: data value contained by the object (it could be a specific number, for example)
- Object identity: the unique ID of the object

### Object attributes
Most Python objects have either data or functions or both associated with them; these are known as attributes. Attributes are accessed by using the dot-notation:

- Example: Given the object `dog`, its name attribute may be accessed by calling `dog.name`

There are two types of attributes:

- Data attribute: value attached to a specific object
- Method: function attached to an object. Typically **a method performs some function or some operation on that object**

#### Difference between data attribute and method
Check the notebook example [1.1.2-objects.ipynb](scripts/1.1.2-objects.ipynb)

### Object instance
An instance is one occurrence of an object. Think of objects as templates for creating instances.

### Python libraries
The Python library consists of all core elements:
- Data types;
- Built-in functions: functions that can be used by all Python programs
- Modules: these must be imported in the code using the `import` statement

### Comprehension check
#### Question 1
Python has immutable objects (e.g., strings and tuples) and mutable objects(e.g., dictionaries and lists). What does it mean for an object to be immutable?
- Its contents cannot be modified by the programmer after the object has been created.

#### Question 2
Consider the following line of code:

```python
x = 4
```
In this assignment, what does the number `4` represent?
- The object value

#### Question 3

What is the difference between methods and data attributes of objects?
- Methods are functions associated with objects, whereas data attributes are data associated with objects

## Modules and Methods
Video here: [[LINK]](media/1.1.3-modules-and-methods.mp4)
Check the notebook example [1.1.3-modules-and-methods.ipynb](scripts/1.1.3-modules-and-methods.ipynb) for this section's examples.

### Meaning
Python modules are libraries of code that can be imported and reused in your own code.

### Importing methods
We can either import a whole module or just the methods and attributes we need from them.

### Namespaces
A Namespace is a container of names shared by objects that typically go together and its intention is to prevent naming conflicts.

### Importing sequence
This is what happens when using the `import` statement:

1. Python creates a new namespace for all the objects which are defined in the new module. In an abstract sense, this is our new namespace
1. Then, Python executes the code of the module and runs it within this newly created namespace
1. After that, Python creates a name (like `np` for `numpy` in our examples), and this name references the new namespace object

So when we call `np.sqrt` function, Python is using the `sqrt` function within the `numpy` namespace. 

### Inspecting module objects

- Use `type` built-in method to retrieve the Object type
- Use `dir` built-in method to retrieve the Object attributes and methods
- Use `help` build-in method to retrieve information of Object methods and attributes

### Comprehension check
#### Question 1
Suppose that `math.sqrt` and `numpy.sqrt` had identical behavior. Are they the same function?
- No. Because they belong to different namespaces, Python treats them separately, regardless of their behavior.

#### Question 2
After running `import numpy as np`, if you want to access the square root function (`sqrt()`) from the library `numpy`, which method would you use?
- `np.sqrt()`

## Numbers and Basic Calculations
Video here: [[LINK]](media/1.1.4-numbers-and-basic-calculations.mp4)

Check the notebook example [1.1.5-random-choice.ipynb](scripts1.1.5-random-choice.ipynb)

### Types of numbers
Python provides 3 different type of numbers:
- Integer numbers:
- Floating point numbers:
- Complex numbers:

Some features in Python numbers:
- Python types have unlimited precision. This means that you can fit any long number to Python's integer type in contrast with other programming languages
- Python numeric types can be freely mixed. This means you aren't constrained by its type when doing calculations (i.e. you don't have to cast them to anotyer type for the calculation to work)
- All Python numbers support all the usual arithmetic operations

### Point of Difference: Python 2 vs Python 3
Floating point division in Python 2 and Python 3 behaves the same, but integer division works differently in Python 2 and in Python 3.
- In the example in the video, where JP divides 6 by 7, Python 2 would give you 0 - but Python 3 does not give 0!

### Comprehension check
#### Question 1
What is the value of 4 factorial (4!)?
- 24:
```python
>>> import math
>>> math.factorial(4)
24
```

## Random choice
Video here: [[LINK]](media/1.1.5-random-choice.mp4)

Check the notebook example [1.1.5-random-choice.ipynb](scripts/1.1.5-random-choice.ipynb)

Python module for random operations is `random`

- `random.choice()` returns a random value from a given iterable object

### Comprehension check
#### Question 1
True or false: `random.choice` will not work on immutable types

- FALSE: `random.choice` only requires that the object has several values regardless of mutability.

## Expressions and Booleans
Video here: [[LINK]](media/1.1.6-expressions-and-booleans.mp4)

Check the notebook example [1.1.6-expressions-and-booleans.ipynb](scripts/1.1.6-expressions-and-booleans.ipynb)

### Comprehension check
#### Question 1

Consider the expression `True and not False is True`. What will return?

- `True`

#### Question 2

What is the difference between `==` and `is`?

- `==` tests whether objects have the same value, whereas `is` tests whether objects have the same identity.
