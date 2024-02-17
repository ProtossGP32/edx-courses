# Part 1 - Objects and methods
## Python Basics
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
Check the python example

### Object instance
An instance is one occurrence of an object. Think of objects as templates for creating instances.


## Python libraries
The Python library consists of all core elements:
- Data types;
- Built-in functions: functions that can be used by all Python programs
- Modules: these must be imported in the code using the `import` statement
