## Control Structures & Loops

Loops and control structures are essential tools in programming that allow you to control the flow of execution in your programs. They allow you to repeat a block of code multiple times, or execute a block of code only under certain conditions.

### Looping

There are two types of loops in Python: for loops and while loops.

A `for` loop is used to iterate over a sequence of items, such as a list or a string. The syntax for a for loop in Python is:

```python
for item in sequence:
    # code to be executed for each item
```

Here is an example of a for loop that iterates over a list of integers and prints out their squares:

```python
numbers = [1, 2, 3, 4, 5]

for x in numbers:
    print(x ** 2)
```

This code would output the following:

```python
1
4
9
16
25
```
A while loop, on the other hand, is used to repeat a block of code as long as a certain condition is true. The syntax for a while loop in Python is:

```python
while condition:
    # code to be executed while the condition is true
    ...
```
Here is an example of a while loop that counts down from 10 and prints out the numbers:

```python
count = 10

while count > 0:
    print(count)
    count -= 1
```

This code would output the following:

```python
10
9
8
7
6
5
4
3
2
1
```

### Control Structures

In addition to loops, Python also provides several control structures that allow you to make decisions and alter the flow of execution in your programs. These include:

`if` statements: These are used to execute a block of code only if a certain condition is true. The syntax for an if statement in Python is:
```python
if condition:
    # code to be executed if the condition is true
    ...
```
Here is an example of an if statement that checks if a number is positive or negative:

```python
x = 10

if x > 0:
    print("x is positive")
else:
    print("x is negative")
```

This code would output the following:

```python
x is positive
```

`break` and `continue` statements: These are used to alter the flow of a loop. The break statement is used to exit a loop early, while the continue statement is used to skip the rest of the current iteration and move on to the next one.
Here is an example of a for loop that uses the break statement to exit when it reaches a certain value:

```python
for x in range(1, 10):
    if x == 5:
        break
    print(x)
```

This code would output the following:

```python
1
2
3
4
```

And here is an example of a for loop that uses the continue statement to skip certain values:

```python
for x in range(1, 10):
    if x % 2 == 0:  # skip even numbers
        continue
    print(x)
```

This code would output the following:

```python
1
3
5
7
9
```
I hope this helps to clarify the basics of loops