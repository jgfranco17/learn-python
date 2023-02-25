## Basics of Object Design

Object-Oriented Programming (OOP) is a programming paradigm that emphasizes the use of objects, which are instances of classes that contain data and methods. Python is an object-oriented programming language and supports OOP concepts such as encapsulation, inheritance, and polymorphism. In this chapter, we will explore the basics of OOP in Python.

### Classes and Objects

A class is a blueprint or template for creating objects that define the properties and methods of the object. To create a class, you use the class keyword followed by the name of the class. 

Here's an example:

```python
class Car(object):
    def __init__(self, make:str, model:str, color:str):
        """
        A class representing a car object.

        Args:
            brand (str): The brand of the car.
            model (str): The model of the car.
            kmpl (int): The car's fuel efficiency in kilometers per liter.
        """
        self.make = make
        self.model = model
        self.color = color

    def honk(self):
        print("HONK!")
```

In the above example, we have created a class named `Car` that has 3 properties: make, model, and color. We have also defined a special kind of function (called a "method") inside: `honk`. Note that the `self` parameter is used to refer to the object that is created from the class.

To create an object of the Car class, you simply call the class name followed by parentheses. 

```python
my_car = Car(make="Toyota", model="Supra", color="red")
```

In the above example, we have created an object named my_car of the Car class. Now we can access the properties and methods of the object using the dot notation. 

```python
print(my_car.color) 
my_car.honk()
```

Output: 

```
red
HONK!
```

In the above example, we have accessed the properties of the `my_car` object and called its methods. What makes methods special is that unlike regular functions, they can only be used by the class they are defined in. We cannot use the `honk` method alone; it must be used with a `Car` instance. 

Moving forward, we will be learning the 4 pillars of object-oriented programming, and how we can use these concepts to maximize the use of objects in our code.