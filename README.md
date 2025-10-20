# Python OOP: Abstract Class & Method Example
# AIM
To create an abstract class named Shape with an abstract method calculate_area, and implement this method in two subclasses: Rectangle and Circle.

# ALGORITHM
Import ABC module:

Use from abc import ABC, abstractmethod to define abstract classes and methods.
Create Abstract Class Shape:

Define an abstract method calculate_area() with @abstractmethod.
Create Subclass Rectangle:

Set default values for length and breadth.
Override calculate_area() to compute the rectangle area.
Create Subclass Circle:

Set default value for radius.
Override calculate_area() to compute the circle area.
Create Objects & Call Methods:

Instantiate Rectangle and Circle.
Call their calculate_area() methods.
# Program
```
from abc import ABC
class Shape(ABC):
    def calculate_area(self):
        pass
class Rectangle(Shape):
    length = 5
    breadth =3 
    def calculate_area(self):
        return self.length * self.breadth

class Circle(Shape):
  radius = 4
  def calculate_area(self):
      return 3.14 * self.radius * self.radius

rec=Rectangle()
cir=Circle()


print("Area of a rectangle:", rec.calculate_area()) 
print("Area of a circle:", cir.calculate_area()) 
```
# Output
![alt text](<Screenshot 2025-10-20 164124.png>)
# Result

# Python OOP: Encapsulation with Private Members
# AIM
To implement Encapsulation in Python by defining a class Rectangle with private member variables __length and __breadth.

# ALGORITHM
Define the Class:

Create a class Rectangle with two private attributes: __length and __breadth.
Initialize Variables:

Use the __init__() constructor to set initial values for __length and __breadth.
Print Values:

Display the private variables from within the class to demonstrate access.
Instantiate the Object:

Create an object of the Rectangle class to trigger the constructor.
# Program
```
class Rectangle:
  __length = 0 
  __breadth = 0
  def __init__(self):
    self.__length = 5
    self.__breadth = 3
    
    print(self.__length)
    print(self.__breadth)
 
rect = Rectangle()


```
# Output
![alt text](<Screenshot 2025-10-20 164016.png>)
# Result

# Method Overriding-Fish and Shark Class Inheritance in Python
# AIM:
To write a Python program that demonstrates class inheritance by creating a parent class Fish with a method type, and a child class Shark that overrides the type method.

# ALGORITHM:
Define the Fish class with a method named type() that prints "fish".
Define the Shark class as a subclass of Fish, and override the type() method to print "shark".
Create an instance of the Fish class named obj_goldfish.
Create an instance of the Shark class named obj_hammerhead.
Use a for loop to iterate over both objects.
Within the loop, call the type() method using the loop variable.
Output will demonstrate method overriding: printing "fish" and "shark" accordingly.
# PROGRAM
```
class Fish:
    def type(self):
        print("fish")

class Shark(Fish):
    def type(self):
        print("shark")

obj_goldfish=Fish()
obj_hammerhead=Shark()

for ani in (obj_goldfish,obj_hammerhead):
    ani.type()
```
# OUTPUT
![alt text](<Screenshot 2025-10-20 163744.png>)
# RESULT

# Python OOP: Operator Overloading (Less Than <)
# AIM
To write a Python program that demonstrates operator overloading by overloading the less than (<) operator using a custom class.

# ALGORITHM
Create Class A:

Define the __init__() method to initialize the object with a value a.
Overload the < Operator:

Define the __lt__() method with logic:
If self.a < o.a, return "ob1 is less than ob2"
Else, return "ob2 is less than ob1"
Create Objects:

Instantiate two objects ob1 and ob2 with values.
Use < Operator:

Use print(ob1 < ob2) to trigger the overloaded behavior.
# Program
```
class MyClass:
    def __init__(self, a):
        self.a = a

    def __lt__(self, o):
        if self.a < o.a:
            return "ob1 is less than ob2"
        else:
            return "ob2 is less than ob1"


ob1 = MyClass(10)
ob2 = MyClass(20)


print(ob1 < ob2)
```
# Output
![alt text](<Screenshot 2025-10-20 164519.png>)
# Result

# Python OOP: Polymorphism with Classes
# AIM
To create two specific classes — Beans and Mango. Then, create a generic function that can accept any object and determine its type (Fruit or Vegetable) and color, using polymorphism.

# ALGORITHM
Create Class Beans:

Define type() method that prints "Vegetable".
Define color() method that prints "Green".
Create Class Mango:

Define type() method that prints "Fruit".
Define color() method that prints "Yellow".
Define Generic Function func(obj):

Call obj.type() and obj.color() — this works with both Beans and Mango objects, showcasing polymorphism.
Create Objects:

Instantiate Beans and Mango.
Pass them to func() and execute the program.
# Program
```

class Beans:
    def type(self):
        print("Vegetable")

    def color(self):
        print("Green")


class Mango:
    def type(self):
        print("Fruit")

    def color(self):
        print("Yellow")


def func(obj):
    obj.type()
    obj.color()

b = Beans()
m = Mango()


func(b)
func(m)
```
# Output
![alt text](<Screenshot 2025-10-20 163643.png>)
# Result