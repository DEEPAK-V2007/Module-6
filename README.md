## NAME: DEEPAK.V
## REGISTER NO: 212225230044

## EX 26:🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

## 💻 Program
```
from abc import ABC, abstractmethod

class Shape(ABC):

    @abstractmethod
    def calculate_area(self):
        pass

class Rectangle(Shape):

    def __init__(self):
        self.length = 10
        self.breadth = 5

    def calculate_area(self):
        area = self.length * self.breadth
        print(f"The area of the rectangle is: {area}")

class Circle(Shape):

    def __init__(self):
        self.radius = 7

    def calculate_area(self):
        area = 3.14 * self.radius * self.radius
        print(f"The area of the circle is: {area}")

r = Rectangle()
c = Circle()

r.calculate_area()
c.calculate_area()
```
## Output

<img width="449" height="196" alt="image" src="https://github.com/user-attachments/assets/dd3de06d-efa7-406b-9981-23e4f735a9f9" />

## Result
Thus, the Python program to implement an abstract class with abstract methods using inheritance was successfully implemented and executed, and the output was verified.

## EX 27:🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

## 💻 Program
```
class Rectangle:

    def __init__(self):
        self.__length = 10
        self.__breadth = 5

        print(f"The length of the rectangle is: {self.__length}")
        print(f"The breadth of the rectangle is: {self.__breadth}")

obj = Rectangle()
```
## Output

<img width="460" height="206" alt="image" src="https://github.com/user-attachments/assets/0f8ec820-90cd-4edf-a983-edd2834f853f" />

## Result
Thus, the Python program to implement encapsulation using private member variables in a class was successfully implemented and executed, and the output was verified.

## EX 28:🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```
class Fish:

    def type(self):
        print(f"This is a fish")

class Shark(Fish):

    def type(self):
        print(f"This is a shark")

obj_goldfish = Fish()
obj_hammerhead = Shark()

for i in (obj_goldfish, obj_hammerhead):
    i.type()
```
## OUTPUT

<img width="497" height="203" alt="{D3203A07-8D82-43F2-80B4-43CF176DDA52}" src="https://github.com/user-attachments/assets/9987e986-eb53-4572-8ed8-fb22ff0845bb" />

## RESULT
Thus, the Python program to demonstrate inheritance and method overriding using parent and child classes was successfully implemented and executed, and the output was verified.

## EX 29:🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

## 💻 Program
```
class A:

    def __init__(self, a):
        self.a = a

    def __lt__(self, o):
        if self.a < o.a:
            return "ob1 is less than ob2"
        else:
            return "ob2 is less than ob1"

ob1 = A(10)
ob2 = A(20)

print(f"{ob1 < ob2}")
```
## Output

<img width="513" height="211" alt="{0E856FF2-92FB-4D2D-BEE2-807010056B9C}" src="https://github.com/user-attachments/assets/36fbeda1-9faa-43f3-804f-3a70c9242a31" />

## Result
Thus, the Python program to demonstrate operator overloading using the less than (<) operator was successfully implemented and executed, and the output was verified.

## EX 30:🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

## 💻 Program
```
class Beans:

    def type(self):
        print(f"Type: Vegetable")

    def color(self):
        print(f"Color: Green")

class Mango:

    def type(self):
        print(f"Type: Fruit")

    def color(self):
        print(f"Color: Yellow")

def func(obj):
    obj.type()
    obj.color()

b = Beans()
m = Mango()

func(b)
func(m)
```
## Output

<img width="493" height="251" alt="image" src="https://github.com/user-attachments/assets/1c4f2680-7c10-49c0-824d-e4bee353026e" />

## Result
Thus, the Python program to demonstrate polymorphism using different classes and a generic function was successfully implemented and executed, and the output was verified.
