# Part 3: Manipulating Objects

## 1.3.1: Dynamic Typing

Video here: [\[LINK\]](media/1.3.1-dynamic-typing.mp4)

Check the notebook example [1.3.1-dynamic-typing.ipynb](scripts/1.3.1-dynamic-typing.ipynb)

Types tell the computer what the sequence of numbers it reads are.

Some languages like C and C++ are statically typed, and others like Python are **dynamically typed**:

-   Static typing means that type checking is performed during compile time
-   Dynamic typing means that type checking is performed at run time

Three important concepts here:

-   Variable
-   Object
-   Reference

When you assign a value to objects in Python, the following three things happen. For example, if we type `x = 3`:

-   Python creates an object, the number `3`
-   Python creates a variable name, in this case `x`
-   Finally, Python inserts a reference from the name of the variable to the actual object

Variable names and objects are stored in different parts of computer's memory.

**Key points:**

-   Variable names always link to objects, never to other variables
-   A variable is, therefore, a reference to the given object
    -   In other words, a name is possibly one out of many names that are attached to that object

It's important to keep in mind distinction between mutable and immutable objects.

### Examples

-   `x = 3`: Python creates the object `3`, the name `x` and then inserts the reference between them

    ```         
    x ──────► 3
    ```

-   `y = x`: Python doesn't create the object linked to the `x` name as it already exists, it creates the variable name `y` and after that the reference between the name `y` and the object that `x` is referring to

    ```         
    x ──────► 3
              ▲
    y ────────┘
    ```

-   `y = y - 1`: Python gets the object referenced by `y` but as numbers are immutable, it creates a new one after resolving the `y - 1` operation (in this case `2`). Then, it replaces the previous reference from `y` to the object `3` with the new reference to the object `2`

    ```         
    x ──────► 3

    y ──────► 2
    ```

The dynamic typing for mutable objects work like this:

-   `L1 = [2, 3, 4]`: Python creates the object for the list, the variable name `L1` and the reference between them

    ```         
    L1 ──────► [2, 3, 4]
    ```

-   `L2 = L1`: Again, Python doesn't create again the value object and reference the newly created variable name `L2` to the same as what `L1` is referencing

    ```         
    L1 ──────► [2, 3, 4]
               ▲
    L2 ────────┘
    ```

-   `L1[0] = 24`: Here, we're replacing the reference of the first position of the link to a new object `24`, but the previous references are still valid

    ```         
    L1 ──────► [24, 3, 4]
               ▲
    L2 ────────┘
    ```

Each object in Python has a **type, value and an identity**, meaning that mutable objects in Python can be identical in content and yet be actually different objects.

-   Each different object is stored in a different position in memory, referenced by its identity (`id()`)
-   `L is M` is the same as `id(L) == id(M)`

### Comprehension Check

#### Question 1

Consider the following code:

`x = 3`

`x` did not exist in memory prior to this code. Which of the following does NOT occur?

-   The object `3` refers to the variable name `x`

#### Question 2

Consider the following code:

``` python
x = 3
y = x
y = y - 1
```

What does `x` equal?

-   `3`

#### Question 4

Consider the following code:

``` python
L1 = [2,3,4]
L2 = L1
L2[0] = 24
```

What does `L1` equal?

-   `[24, 3, 4]`

#### Question 4

Consider the following code:

``` python
L = [2,3,4]
M1 = L
M2 = L[:]
M1 is M2
```

What will this return?

-   `False`

## 1.3.2: Copies

Video here: [\[LINK\]](media/1.3.2-copies.mp4)

Check the notebook example [1.3.2-copies.ipynb](scripts/1.3.2-copies.ipynb)

Python provides the `copy` module for creating identical copies of objects.

There are two types of copies available:

-   Shallow copy: it constructs a new compound object and then inserts its references into it to the original object
-   Deep copy: constructs a new compound object and then recursively inserts copies into it of the original objects

Diagram:

```         
┌─────────────┐                     
│             │                     
│      x      │                     
│             │                     
└──┬────────┬─┘                     
   │        │                       
 ┌─▼─┐    ┌─▼─┐      ┌───┐    ┌───┐ 
 │ a │    │ b │      │ a'│    │ b'│ 
 └─▲─┘    └─▲─┘      └─▲─┘    └─▲─┘ 
   │        │          │        │   
┌──┴────────┴──┐    ┌──┴────────┴──┐
│              │    │              │
│      x'      │    │      x''     │
│              │    │              │
└──────────────┘    └──────────────┘
  Shallow copy          Deep copy   
```

### Comprehension checks

#### Question 1

Consider the following code:

``` python
import copy
x = [1,[2]]
y = copy.copy(x)
z = copy.deepcopy(x)
y is z
```

What will this return?

- `False`

## 1.3.3: Statements

Video here: [\[LINK\]](media/1.3.3-statements.mp4)

Check the notebook example [1.3.3-statements.ipynb](scripts/1.3.3-statements.ipynb)

Statements are used to compute values, assign values, and modify attributes, among many other things.

- `return`: returns values from a function
- `import`: used to import modules
- `pass`: it is used to do nothing and we need a placeholder for syntactical reasons

**Compound statements** contain groups of other statements and they affect or control the execution of those other statements in som way.

- Compound statements typically span multiple lines and consist of one or more clauses
  - A clause consists of a header and a block or a suit of code
- The close headers of a particular compound statement start with a keyword, end with a colon and are all at the same indentation level.
- Etc.

**In Python, indentation is not cosmetic!**

### Comprehension Checks
#### Question 1

Consider the following code:

```python
if False:
    print("False!")
elif True:
    print("Now True!")
else:
    print("Finally True!")
```
What does this print?

- `Now True!`

#### Question 2

Consider the following code:

```python
if n%2 == 0:
    #blank#
else:
    print("odd")
```

Assume that `n` is a previously defined integer. Can you replace the `#blank#` line so that the code prints `"even"` if `n` is even, and `"odd"` if `n` is odd?

- `print("even")`

## 1.3.4: For and While Loops

Video here: [\[LINK\]](media/1.3.4-for-and-while-loops.mp4)

Check the notebook example [1.3.4-for-and-while-loops.ipynb](scripts/1.3.4-for-and-while-loops.ipynb)

For loops have a finite number of iterations defined by the statement clause

While loops can run infinitely as long as a given expression is true.

### Comprehension Check
#### Question 1

Consider:

```python
bears = {"Grizzly":"angry", "Brown":"friendly", "Polar":"friendly"}
```

Can you replace `#blank#` so the code will print a greeting only to friendly bears? Your code should work even if more bears are added to the dictionary

```python
for bear in bears:
    if #blank#:
        print("Hello, "+bear+" bear!")
    else:
        print("odd")
```

- `bears[bear] == "friendly":`

#### Question 2

Consider the following code:

```python
is_prime = True
for i in range(2,n):
    if n%i == 0:
        #blank#

print(is_prime)
```

Can you fill in the `#blank#` line so the code will only print `True` if `n` is prime?

- ```python
  is_prime = False
  break
  ```

#### Question 3

Consider the following code:

```python
n=100
number_of_times = 0
while n >= 1:
    n //= 2
    number_of_times += 1
print(number_of_times)
```

What will this print?

- `7`

## 1.3.5: List Comprehension

Video here: [\[LINK\]](media/1.3.5-list-comprehension.mp4)

Check the notebook example [1.3.5-list-comprehension.ipynb](scripts/1.3.5-list-comprehension.ipynb)

### Comprehension Check
#### Question 1

Consider the following code:

```python
sum([i**2 for i in range(3)])
```

What will this output?

- `5`

#### Question 2

How can you use a list comprehension, including `if` and `for`, to sum the odd numbers from `0` through `9`?

- ```python
  sum([number if number%2 != 0 else 0 for number in range(10)])
  ```

## 1.3.6: Reading and Writing Files

Video here: [\[LINK\]](media/1.3.6-reading-and-writing-files.mp4)

Check the notebook example [1.3.6-reading-and-writing-files.ipynb](scripts/1.3.6-reading-and-writing-files.ipynb)

### Comprehension Check
#### Question 1

Consider the following code:

```python
F = open("input.txt", "w")
F.write("Hello\nWorld")
F.close()
lines = []
for line in open("input.txt"):
    lines.append(line.strip())
print(lines)
```

What does this print?

- `['Hello', 'World']`

## 1.3.7: Introduction to Functions

Video here: [\[LINK\]](media/1.3.7-introduction-to-functions.mp4)

Check the notebook example [1.3.7-introduction-to-functions.ipynb](scripts/1.3.7-introduction-to-functions.ipynb)

- Arguments in Python functions are matched by position.
- Functions can return tuples of values
- Functions do not exist until Python reaches and runs the `def` statement
  - This means that the order of their declaration is important
- The `def` statement creates an object and assigns it t a name
  - This means that we can later in the code reassign the function object ot another name
- Arguments are passed by assigning objects to local names

### Comprehension Check
#### Question 1

Consider the following function:

```python
def modify(mylist):
  mylist[0] *= 10
  return(mylist)

L = [1, 3, 5, 7, 9]
M = modify(L)
M is L
```

What is the value of the final line?

- `True`: That's because regardless of the operations done to the mutable object, the `modify` function returns the reference to the object, not a copy of it


## 1.3.8: Writing Simple Functions


Video here: [\[LINK\]](media/1.3.8-writing-simple-functions.mp4)

Check the notebook example [1.3.8-writing-simple-functions.ipynb](scripts/1.3.8-writing-simple-functions.ipynb)


### Comprehension Check

Please refer to the Comprehension Check section in the notebook for non-explained questions.

#### Question 3

Why `is_vowel(4)` would not work?

- `4` is not a string, and Python cannot test if an `int` is in a string

#### Question 4

The new code accomodates the objects of type `int` by casting them as a `string`

#### Question 5

- `N *= i`


## 1.3.9: Common Mistakes and Errors

Video here: [\[LINK\]](media/1.3.9-common-mistakes-and-errors.mp4)

Check the notebook example [1.3.9-common-mistakes-and-errors.ipynb](scripts/1.3.9-common-mistakes-and-errors.ipynb)

Common mistakes:

- Not properly reading the error messages
- Forgetting that dictionaries are not ordered
- Trying to do an operation not supported by the object
- Trying to access a value the wrong way
- Trying to modify an immutable object
- Trying to operate on objects of different type

### Comprehension Check
#### Question 1

When you encounter an error in Python, what should you do?

- All of the above, meaning:
  - Read the error message
  - Try `help()` or `dir()`
  - Use Google or StackOverflow to find an answer
  - Search the course discussion forum and post a question if yours hasn't been asked.