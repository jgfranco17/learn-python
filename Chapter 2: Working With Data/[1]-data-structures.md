## Python Data Structures

In this section, you will learn about the different types of data structures available in Python and how to use them to store and manipulate data in your programs. Data structures are an essential part of programming, as they allow you to organize and store data in a way that is efficient and easy to work with.

Python provides several built-in data structures that you can use in your programs, including lists, dictionaries, sets, and tuples. Each data structure has its own characteristics and is suited for different types of data and operations. It is important to choose the appropriate data structure for your needs, as this can affect the efficiency and complexity of your programs.

In this chapter, you will learn about the different data structures in Python and how to use them effectively. You will also learn about common operations and methods that you can use to work with data structures, and you will see some examples of how data structures can be used in real-world programs.

---

### Prior Note: Indexing

In Python, index notation is used to access elements of a sequence, such as a string, list, or tuple. Indexing allows you to retrieve a specific element or a range of elements from a sequence, based on their position.

In Python, indexing starts at 0, meaning that the first element of a sequence is at index 0, the second element is at index 1, and so on. You can use positive or negative indices to access elements, with negative indices counting from the end of the sequence; where -1 indicates the last item, -2 the second to the last, and so forth.

Here are some examples of index notation in Python:

```python
# Declare a string
text = "Hello, World!"

# Access a character by its index
print(text[0])  # prints "H"
print(text[-1])  # prints "!"

# Access a range of characters
print(text[7:12])  # prints "World"
print(text[7:-1])  # prints "World"
print(text[:5])  # prints "Hello"
print(text[-6:])  # prints "World!"

###########################################

# Declare a list
numbers = [1, 2, 3, 4, 5]

# Access an element by its index
print(numbers[0])  # prints 1
print(numbers[-1])  # prints 5

# Access a range of elements
print(numbers[2:4])  # prints [3, 4]
print(numbers[2:-1])  # prints [3, 4]
print(numbers[:3])  # prints [1, 2, 3]
print(numbers[-3:])  # prints [3, 4, 5]

###########################################

# Declare a tuple
coordinates = (10, 20, 30)

# Access an element by its index
print(coordinates[0])  # prints 10
print(coordinates[1])  # prints 20
print(coordinates[2])  # prints 30
```

---

### Lists

Python lists are ordered collections of items that can contain any type of data. They are declared using square brackets and are indexed by position, starting at 0. Lists are very flexible data structures, as they can store a variety of data types and can be modified in place. Here is an example of a list in Python:

```python
# Declare a list
numbers = [1, 2, 3, 4, 5]

# Access an element by its index
print(numbers[0])  # prints 1

# Modify an element by its index
numbers[0] = 10
print(numbers[0])  # prints 10

# Append an element to the end of the list
numbers.append(6)
print(numbers)  # prints [10, 2, 3, 4, 5, 6]

# Insert an element at a specific position
numbers.insert(1, 20)
print(numbers)  # prints [10, 20, 2, 3, 4, 5, 6]

# Remove an element by its index
numbers.pop(1)
print(numbers)  # prints [10, 2, 3, 4, 5, 6]

# Remove an element by its value
numbers.remove(5)
print(numbers)  # prints [10, 2, 3, 4, 6]

# Find the index of an element
print(numbers.index(4))  # prints 3

# Check if an element is in the list
print(5 in numbers)  # prints False
print(6 in numbers)  # prints True

# Get the length of the list
print(len(numbers))  # prints 5

# Sort the list
numbers.sort()
print(numbers)  # prints [2, 3, 4, 6, 10]

# Reverse the list
numbers.reverse()
print(numbers)  # prints [10, 6, 4, 3, 2]

# Copy the list
new_numbers = numbers.copy()
print(new_numbers)  # prints [10, 6, 4, 3, 2]
```

### Tuples

Python tuples are immutable sequences of values that can contain a variety of data types. They are similar to lists, but cannot be modified once created. Tuples are often used to store data that should not be modified, such as constants. Here is an example of a tuple in Python:

```python
# Declare a tuple
coordinates = (10, 20)

# Access an element by its index
print(coordinates[0])  # prints 10

# Try to modify an element by its index (this will cause an error)
# coordinates[0] = 30

# Concatenate tuples
new_coordinates = coordinates + (30, 40)
print(new_coordinates)  # prints (10, 20, 30, 40)

# Find the index of an element
print(new_coordinates.index(30))  # prints 2

# Check if an element is in the tuple
print(5 in coordinates)  # prints False
print(10 in coordinates)  # prints True

# Get the length of the tuple
print(len(coordinates))  # prints 2

# Unpack a tuple
x, y = coordinates
print(x)  # prints 10
print(y)  # prints 20
```

Python tuples provide some useful methods and operations that allow you to manipulate and work with data. You can use them to store and organize data, perform lookups and indexing, and much more.

It is important to note that tuples are immutable, meaning that you cannot modify their contents once they are created. This can be a useful feature if you need to store data that should not be changed, but it can also be a limitation if you need to modify the data stored in a tuple.

In general, tuples are less flexible than lists, but they can be more efficient in certain cases, such as when you need to store a large number of elements and do not need to modify them. 

### Dictionaries

Dictionaries are unordered collections of items that are stored as key-value pairs. They are declared using curly braces and are indexed by keys. Dictionaries are very efficient for storing and retrieving data, as they allow you to access a value directly using its key. Here is an example of a dictionary in Python:

```python
# Declare a dictionary
student = {
    "name": "John Smith",
    "age": 20,
    "courses": ["Math", "Physics", "Computer Science"],
}

# Access a value by its key
print(student["name"])  # prints "John Smith"

# Modify a value by its key
student["age"] = 21
print(student["age"])  # prints 21

# Add a new key-value pair
student["phone"] = "555-555-5555"
print(student)  # prints {'name': 'John Smith', 'age': 21, 'courses': ['Math', 'Physics', 'Computer Science'], 'phone': '555-555-5555'}

# Remove a key-value pair
del student["phone"]
print(student)  # prints {'name': 'John Smith', 'age': 21, 'courses': ['Math', 'Physics', 'Computer Science']}

# Check if a key is in the dictionary
print("phone" in student)  # prints False
print("age" in student)  # prints True

# Get the keys of the dictionary
print(student.keys())  # prints ['name', 'age', 'courses']

# Get the values of the dictionary
print(student.values())  # prints ['John Smith', 21, ['Math', 'Physics', 'Computer Science']]

# Get the key-value pairs of the dictionary
print(student.items())  # prints [('name', 'John Smith'), ('age', 21), ('courses', ['Math', 'Physics', 'Computer Science'])]

# Make a copy of the dictionary
new_student = student.copy()
print(new_student)  # prints {'name': 'John Smith', 'age': 21, 'courses': ['Math', 'Physics', 'Computer Science']}
```

As you can see, Python dictionaries provide many useful methods and operations that allow you to manipulate and work with data. You can use them to store and organize data, perform lookups and updates, and much more.

It is important to note that dictionaries are unordered, meaning that the elements in a dictionary are not stored in a specific order. This means that you cannot access elements in a dictionary by their position, only by their keys. It also means that the order of elements in a dictionary may change over time, as dictionaries do not maintain a fixed order.

### Sets

Sets are unordered collections of unique items. They are declared using curly braces or the `set()` function, and do not allow duplicate elements. Sets are useful for storing and manipulating data when you need to ensure that all elements are unique, or when you need to perform set operations such as union, intersection, and difference. Here is an example of a set in Python:

```python
# Declare a set
numbers = {1, 2, 3, 4, 5}

# Try to add a duplicate element (this will have no effect)
numbers.add(5)
print(numbers)  # prints {1, 2, 3, 4, 5}

# Add a new element
numbers.add(6)
print(numbers)  # prints {1, 2, 3, 4, 5, 6}

# Remove an element
numbers.remove(6)
print(numbers)  # prints {1, 2, 3, 4, 5}

# Check if an element is in the set
print(5 in numbers)  # prints True
print(6 in numbers)  # prints False

# Get the length of the set
print(len(numbers))  # prints 5

# Create a set from a list (duplicate elements will be removed)
new_numbers = set([1, 2, 2, 3, 3, 3, 4, 4, 4, 4, 5, 5, 5, 5, 5])
print(new_numbers)  # prints {1, 2, 3, 4, 5}

# Perform set operations
even_numbers = {2, 4, 6, 8, 10}
odd_numbers = {1, 3, 5, 7, 9}

# Union
print(even_numbers | odd_numbers) # prints {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}

# Intersection
print(even_numbers & odd_numbers) # prints set()

# Difference
print(even_numbers - odd_numbers) # prints {2, 4, 6, 8, 10}
print(odd_numbers - even_numbers) # prints {1, 3, 5, 7, 9}

# Symmetric difference
print(even_numbers ^ odd_numbers) # prints {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}

# Check if a set is a subset or superset of another set
print(even_numbers <= odd_numbers) # prints False
print(even_numbers >= odd_numbers) # prints False
print(even_numbers <= even_numbers) # prints True
print(even_numbers >= even_numbers) # prints True
```

As you can see, Python sets provide many useful methods and operations that allow you to manipulate and work with data. You can use them to store and organize data, perform set operations, and much more.

Sets are unordered and do not allow duplicate elements. This can be a useful feature if you need to store a collection of unique items, or if you need to perform set operations. However, sets do not support indexing or slicing, so you cannot access or modify individual elements directly.
