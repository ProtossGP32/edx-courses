# Part 2: Sequence objects

## 1.2.1: Sequences

Video here: [[LINK]](media/1.2.1-sequences.mp4)

Check the notebook example [1.2.1-sequences.ipynb](scripts/1.2.1-sequences.ipynb)

### Comprehension check
#### Question 1

Consider the folliwong tuple and index `(1, 2, 3)[0]`. What will it return?

- `1`

#### Question 2

Consider the following tuple and index `(1, 2, 3)[-0: 0]`. What will this return?

- `()` (Empty, no index inbetween)


## 1.2.2: Lists

Video here: [[LINK]](media/1.2.2-lists.mp4)

Check the notebook example [1.2.2-lists.ipynb](scripts/1.2.2-lists.ipynb)

- Lists are mutable sequences of objects of any type, typically used to store homogeneous items (although not strictly a requirement).
- In-place list methods modify the original list (`reverse`, `sort`, etc.).
- Using Python's `sort` method will let Python create a new object

### Comprehension check
#### Question 1

Consider a list `x=[1,2,3]`. Which index corresponds to `2` in `x`?

- `1`

#### Question 2

Consider a list `x=[1,2,3]`. Enter the code below for how you would use the append method to add the number `4` to the end of list `x`.

- `x.append(4)`

#### Question 3

What do list methods such as `reverse` and `sort` return?

- They return nothing because they are in-place methods, meaning they alter the content of the original list.

## 1.2.3: Tuples

Video here: [[LINK]](media/1.2.3-tuples.mp4)

Check the notebook example [1.2.3-tuples.ipynb](scripts/1.2.3-tuples.ipynb)

Tuples are immutable sequences typically used to store heterogeneous data.

### Comprehensive checks
#### Question 1

Consider the tuple `x=(1,2,3)`.
How could you add the integer 4 to the end of the tuple?

- This is impossible. Tuples are immutable, so they can't be edited after they've been created

#### Question 2

Consider `x=(1,2,3)`. Use the count method to count the number of 3s in x.

- `x.count(3)`

#### Question 3

Consider again `x=(1,2,3)`. If you wanted the sum of the numbers in x using a single function, which command would you use?

- `sum(x)`

#### Question 4

Which of the following prints type `tuple`?

- `type((2,))`

## 1.2.4: Ranges

Video here: [[LINK]](media/1.2.4-ranges.mp4)

Check the notebook example [1.2.4-ranges.ipynb](scripts/1.2.4-ranges.ipynb)

Ranges are immutable sequences of integers, and they are commonly used in `for` loops.

Don't turn ranges into lists just to access indexes of a database, it's a waste of space. Use the range directly.

### Point of difference: Range in Python 2 vs Python 3

Here is another point of difference between Python 2 and Python 3! Note that the Python 3 range object is a generator, similar to the Python 2 xrange object.  In contrast, the Python 2 range object is a list, which instantiates its elements.

### Comprehension check
#### Question 1

Why might you prefer to use a range over a list?

- Ranges take up less memory than lists because they do not hold all the numbers simultaneously.

## 1.2.5: Strings

Video here: [[LINK]](media/1.2.5-strings.mp4)

Check the notebook example [1.2.5-strings.ipynb](scripts/1.2.5-strings.ipynb)

Strings are immutable sequences of characters.

Common operations:

- `len()` function
- Common generic sequence operations:
  - Retrieve by index (`string_test[2]`)
  - Slice (`string_test[:3]`)
  - Membership in string (`'P' in string_test`)

Polymorphism: the result of an operator depends on the type of objects it is being applied to.

Manipulation operations: They generate new objects

- `replace`
- `split`

### Comprehension Check
#### Question 1

Which of the following expressions are valid?

- `2 + 2`
- `"2" + "2"`
- `2 * 2`
- `2 * "2"`

#### Question 2

Which of the following lines of code will fail to return the integers `0` through `9` in a single string?

- `str(range(10))`

#### Question 3

Assume you have assigned `x` the string value of "125,000" (i.e., `x = "125,000"`). Can you find a string method that tests if `x` only contains digits?

- `x.isdigit()`


## 1.2.6: Sets

Video here: [[LINK]](media/1.2.6-sets.mp4)

Check the notebook example [1.2.6-sets.ipynb](scripts/1.2.6-sets.ipynb)

Sets are unordered collections of distinct **hashable objects**:

- **Hashable objects** are immutable objects
- Sets cannot be indexed
- Sets of an element can never be duplicated (all objects will always be unique)

Two types of sets:

- Set: mutable set
- Frozen set: immutable set

Set operations:

- Union: `|`
- Intersection: `&`


### Comprehension Checks
#### Question 1

Let sets `x={1,2,3}` and `y={2,3,4}`. How could you get `{4}` from x and y using basic set operations?

- `y - x`

#### Question 2

Consider again sets `x={1,2,3}`` and `y={2,3,4}`. How could you get `{2, 3}` from `x` and `y` using basic set operations?

- `y & x`

#### Question 3

Consider again sets `x={1,2,3}` and `y={2,3,4}`. How could you get `{1, 4}` from `x` and `y` using the provided set methods?

- `set.symmetric_difference()`: This is called *symmetric difference*, also achievable by the operation `x ^ y`

#### Question 4

Consider again sets `x={1,2,3}` and `y={2,3,4}`. Which of the following lines of code will determine if all elements of `x` are in `y`?

- `x.issubset(y)`

## 1.2.7: Dictionaries

Video here: [[LINK]](media/1.2.7-dictionaries.mp4)

Check the notebook example [1.2.7-dictionaries.ipynb](scripts/1.2.7-dictionaries.ipynb)
Dictionaries are mappings from key objects to value objects.

- Dictionaries consist of Key:Value pairs, where the keys must be immutable and the values can be anything
- Dictionaries themselves are mutable so this means once you create your dictionary, you can modify its contents on the fly
- Dictionaries can be used for performing very fast look-ups on unordered data
- **Dictionaries are not sequences**. Looping over a dictionary will be done in an arbitrary order of the keys

Dictionary methods return View objects

- As you update your dictionaries, so will the View objects


## A Note on Dictionaries and Order
As of Python 3.6, dictionary elements maintain an order. Specifically, each element is kept in the order it was added to the dictionary. The Python developer mailing list suggests this feature will remain in all future versions of Python.

### Comprehension Checks
#### Question 1

Consider the dictionary:
```python
age={'Tim':29, 'Jim':31, 'Pam':27, 'Sam':35}
```

`age[0]` returns an error. Why?

- There is no key `0` in the dictionary

##### Question 2

Why may you not edit the key `"Tim"` to `"Tom"`?

- Dictionary keys are not mutable

#### Question 3

Which of the following data structures may be used as keys in a `dict`?

- Strings (immutable)
- Tuples (immutable)