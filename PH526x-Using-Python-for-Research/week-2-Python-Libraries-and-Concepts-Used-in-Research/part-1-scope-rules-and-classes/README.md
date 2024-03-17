# Part 1: Scope Rules and Classes

## 2.1.1: Scope Rules

Video here: [\[LINK\]](media/2.1.1-scope-rules.mp4)

Check the notebook example [2.1.1-scope-rules](scripts/2.1.1-scope-rules.ipynb)

### GOALS

- Learn the **LEGB** rule for scope
- Review some examples that demonstrate **scope rules** in Python

### LEGB

LEGB stands for:

- L: local
- E: enclosing function
- G: global
- B: built-in

It defines the order that Python uses to look for a variable or function context.

### Side-efects functions
Consider the function `update()` that modifies a global variable `x`. Functions that modify either their inputs or objects defined in other parts of the program, such as global variables, in this type of behind-the-scenes manner are saide to have **side effects**:

- This is a programming style to be generally avoided as it can lead to programming errors that are very difficult to find.

### Scope rules, mutability and immutability of Python objects

Remember that what is passed to a function is the variable name (reference) of an object, thus if it is immutable (i.e. an integer) its value won't be modified outside the scope of the function (it will be treated as a local variable); if it is a mutable object, then the function can modify it and the result will persist outside the scope of the function.

### Comprehension check

Please refer to the lesson's notebook if a question is not explained here.

## 2.1.2: Classes and Object-Oriented Programming

Video here: [\[LINK\]](media/2.1.2-classes-and-object-oriented-programming.mp4)

Check the notebook example [2.1.2-classes-and-object-oriented-programming](scripts/2.1.2-classes-and-object-oriented-programming.ipynb)

### Class

A class is a blueprint of the methods and attributes that an object of that class should have.

An object created from a class is commonly referred as an **instance**.

- The `class` statement doesn't create any instances of the class
- The functions defined inside a class are known as **instance methods** because they operate on an instance of the class
- By convention, the name of the class instance is called `self`, and it must always be passed as the first argument to the functions defined as part of a class

### Inheritance

Inheritance takes place when a class inherits its methods and attributes from another class:

In this example, `MyList` class inherits all the attributes of the built-in `list` class:

```python
class MyList(list):
  # ...
```

### Comprehension check

Please refer to the lesson's notebook if a question is not explained here.