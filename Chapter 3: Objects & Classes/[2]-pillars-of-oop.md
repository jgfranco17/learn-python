## Pillars of OOP

This section covers the four pillars of object-oriented programming: Abstraction, Encapsulation, Inheritance, and Polymorphism. These four concepts form the foundation of object-oriented programming and are essential to creating modular, extensible, and maintainable software. We will explore each concept in detail, and provide examples to help you understand how to leverage them in your Python programs. 

### Encapsulation

Encapsulation is the concept of hiding the implementation details of an object and only exposing a public interface. In Python, encapsulation is achieved by using private and protected attributes.

Private attributes are denoted by a double underscore (`__`) prefix. These attributes can only be accessed within the class itself. Here's an example:

```python
class BankAccount:
    def __init__(self, account_number, balance):
        self.__account_number = account_number
        self.__balance = balance
    
    def deposit(self, amount):
        self.__balance += amount
    
    def withdraw(self, amount):
        if amount > self.__balance:
            print("Insufficient funds")
        else:
            self.__balance -= amount
    
    def get_balance(self):
        return self.__balance
```

In the above example, we have defined a `BankAccount` class that has two private attributes: `__account_number` and `__balance`. These attributes can only be accessed within the class methods.

Protected attributes are denoted by a single underscore (`_`) prefix. These attributes can be accessed within the class and its subclasses. H

```python
class Animal:
    def __init__(self, name):
        self._name = name
    
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

```

In the above example, we have defined an `Animal` class that has a protected attribute `_name`. We have also defined a `Dog` class that inherits from the `Animal` class and overrides its speak method.

### Inheritance

Inheritance is the concept of creating a new class from an existing class. The new class inherits the properties and methods of the existing class and can also add its own properties and methods. In Python, inheritance is achieved by defining a new class that inherits from an existing class using the `super()` method.

```python
class Animal:
    def __init__(self, name):
        self.name = name
    
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"
```

In the above example, we have defined a `Dog` class and a `Cat` class that inherit from the `Animal` class. Both `Dog` and `Cat` classes have their own implementation of the `speak()` method.

### Polymorphism

Polymorphism is the concept of having multiple forms of the same object or method. In Python, polymorphism is achieved by defining methods with the same name in different classes.

```python
class Rectangle:
    def __init__(self, length, width):
        self.length = length
        self.width = width
    
    def area(self):
        return self.length * self.width

class Circle:
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14 * self.radius ** 2
```

In the above example, we have defined a `Rectangle` class and a `Circle` class that both have an area method. Even though the implementation of the `area` method is different in both classes, we can call the `area` method on objects of both classes.

```python
rectangle = Rectangle(4, 5)
circle = Circle(3)

print(rectangle.area())
print(circle.area())
```

The resulting output is:

```
20
28.26
```

In this chapter, we have explored the basics of object-oriented programming in Python. We learned how to define classes and objects, how to use encapsulation to hide implementation details, how to use inheritance to create new classes from existing classes, and how to use polymorphism to have multiple forms of the same object or method. These concepts are essential for building complex applications in Python.