# Py.Class.Examples
Python Class Examples

'''class Jets:

    def __init__(self, name, country):
        self.name = name
        self.origin = country

    def show(self):
        print(self.name,self.origin)


first_item = Jets("F16", "USA")

a = first_item
print(a.show())'''

'''This time print the origin of the first_item.'''

'''class Jets:
    model = None
    country = 0

    def __init__(self, name, country):
        self.name = name
        self.origin = country


first_item = Jets("F16", "USA")

a = first_item.origin


print(a)'''

'''Define a Point3D class that inherits from object Inside the Point3D class, define an __init__() function that accepts self, x, y, and z, and
assigns these numbers to the member variables self.x,self.y,self.z. Define a __repr__() method that returns "(%d, %d, %d)" % (self.x, self.y, self.z).
This tells Python to represent this object in the following format: (x, y, z).
Outside the class definition, create a variable named my_point containing a new instance of Point3D with x=1, y=2, and z=3. Finally, print my_point.'''

******'''Where do we use F in Python?
Python f strings embed expressions into a string literal. 
You can use f strings to embed variables, strings, or the results of functions into a string. 
An f string are prefixed with “f” at the start, before the string iitself begins. 
Introduced in Python 3.6, make it easier to format strings.'''****

****'''The %d operator is used as a placeholder to specify integer values, decimals or numbers. 
It allows us to print numbers within strings or other values. 
The %d operator is put where the integer is to be specified. 
Floating-point numbers are converted automatically to decimal values'''***







class point3d:
    def __init__(self,x,y,z):
        self.x = x
        self.y = y
        self.z = z

    def __repr__(self):
        return "(%d,%d,%d)" % (self.x,self.y,self.z) #%d is the place value holder we have to use in the format "%d" % VN(Varibale name from whihc value will be holded here

my_point=point3d(1,2,3)
print(my_point)




'''Create new instances until the sixth item following this order:
F14, SU33, AJS37, Mirage2000, Mig29, A10.
You can check Hint 1 for the origins.
'''


'''class Jets:
    model = None
    country = 0

    def __init__(self, name, country):
        self.name = name
        self.origin = country'''



'''F14, SU33, AJS37, Mirage2000, Mig29, A10.'''

'''first_item=Jets('f14','USA')
second_item=Jets('SU33','RUSSIA')
third_item=Jets('AJS37','Sweden')
fourth_item=Jets('Mirage2000','France')
fifth_item=Jets('Mig29', 'USSR')
sixth_item=Jets('A10', 'USA')


first_army=[first_item.name,second_item.name,third_item.name,fourth_item.name,fifth_item.name,sixth_item.name]


print(first_army)'''

'''Add another attribute called "quantity" to the initialization method (usually referred to as constructor or __init__). 
Then define assign this attribute to self.quantity attribute inside the constructor.
Then create 2 instances for: F14 and Mirage2000 with quantities 87 and 35.'''

'''class Jets:
    model = None
    country = 0

    def __init__(self, name, country,quantity):
        self.name = name
        self.origin = country
        self.quantity = quantity



first_item=Jets('F14','USA',87)
second_item=Jets('Mirage2000','France',35)

total=first_item.quantity+second_item.quantity
print(total)'''


'''Let's try something else.

Try building a simple class from the ground up. An instance is already created for you and instance
attributes are included inside the print.
Take those clues and try to reverse engineer the class.'''

#Type your code here.

'''class Nobel:
    def __init__(self,category,year,winner):
        self.category= category
        self.year = year
        self.winner = winner


np2005=Nobel("Peace", 2005, "Muhammad Yunus")
print(np2005.category, np2005.year, np2005.winner)'''

'''Let's practice using string representation method to represent the data in previous exercise in a much "classier" way, no pun intended!.
__str__ function can be used to return a string representation for the class when needed.'''

'''class Nobel:
    def __init__(self,category,year,winner):
        self.category= category
        self.year = year
        self.winner = winner

    def __str__(self):
        return "{} was the winner of noble prize in{} in the year{}".format(self.winner,self.category,self.year)
#{}  is the output holders
"""def format(self, *args, **kwargs):  # known special case of str.format     
        S.format(*args, **kwargs) -> str
        Return a formatted version of S, using substitutions from args and kwargs.
        The substitutions are identified by braces ('{' and '}').
        pass"""


np2005 = Nobel("Peace", 2005, "Muhammad Yunus")
print(np2005)'''


'''We have seen multiple examples of class usage in Python. Let's build something from ground up.
In this exercise create a class named myfunc and inside it place a very simple function named "fifth" which takes x and
returns fifth power of x. No __init__ or class attributes needed.
Finally call your function with number 5 and assign it to variable ans.'''

'''class myfunc:
    def fifth(x):
        return x**5

ans =myfunc.fifth(5)
print(ans)'''
#**************************************************************
*****'''Now let's make some changes to the class we created in the previous Python exercise.
First make your function so that it takes to parameters: x and y. x will be the number being raised and y will be the power. 
So, users can raise numbers to any power! Also let's change the function's name to power.
Also let's add a string representation quickly, so that when a user prints the class they get a meaningful description.
It can be something like: This class will consist of mathematical operations. We only have one function named power currently.'''******

class myfunc:
    def power(x,y):
        return x**y
    def __str__(self):
        return "mMyfunc is a class which is capable of mathematical operations like raising a number \nto a power with power function"

ans1 = myfunc.power(8,5)
ans2 =myfunc()

print(ans1)
print(ans2)


**********************************************************************************************************************************

''' Write a Program to create a class by name Students,
and initialize attributes like name, age, and grade while creating an object.'''

'''class students:
    def __init__(self,nam,age,grade):
        self.name = nam
        self.age = age
        self.grade = grade

s1 = students("harry",25,'A+')
print(s1.grade,s1.age,s1.name)'''

'''Write a program, to create a child class Teacher that will inherit the properties of Parent class Staff'''

'''class staff:
    def __init__(self,sub,_class):
        self.subject = sub
        self._class = _class

class teacher(staff):
    def __init__(self,name,gender,age, experience):
        super().__init__()
        self.name = name
        self.gender = gender
        self.age = age
        self.exp = experience
    def show(self):
        print(self.name,self.gender,self.age,self.exp)
    def __str__(self):
        print("this teacher belongs to class {} and her subject is {}".format(self._class,self.subject))
s1 = staff('chemistry', "10th")
t1 = teacher('harry','male',25,4)
print(t1.__str__())'''

'''Exercise 1
Follow the steps:

Create a class, Triangle. Its __init__() method should take self, angle1, angle2, and angle3 as arguments. 
Make sure to set these appropriately in the body of the __init__()method.
Create a variable named number_of_sides and set it equal to 3.
Create a method named check_angles. 
The sum of a triangle's three angles is It should return True if the sum of self.angle1, self.angle2, and self.angle3 is equal 180, 
and False otherwise.
Create a variable named my_triangle and set it equal to a new instance of your Triangle class. 
Pass it three angles that sum to 180 (e.g. 90, 30, 60).
Print out my_triangle.number_of_sides and print out my_triangle.check_angles().'''

'''class triangle:
    def __init__(self, angle1, angle2, angle3):
        self.angle1 = angle1
        self.angle2 = angle2
        self.angle3 = angle3
    number_of_sides = 3
    def check_angles(self):
        total = self.angle1+self.angle2+self.angle3
        if total==180:
            return "true"
        else:
            return "False"

my_triangle = triangle(90,30,60)

print(my_triangle.number_of_sides)
print(my_triangle.check_angles())'''

'''Exercise 2
Define a class called Songs, it will show the lyrics of a song. 
Its __init__() method should have two arguments:selfanf lyrics.lyricsis a list. 
Inside your class create a method called sing_me_a_songthat prints each element of lyricson his own line. 
Define a varible:

happy_bday = Song(["May god bless you, ",
                   "Have a sunshine on you,",
                   "Happy Birthday to you !"])
                   
Call the sing_me_songmehod on this variable.'''

'''class songs:
    def __init__(self,lyrics):
        self.lyrics = lyrics
    def sing_me_a_song(self):
        for i in self.lyrics:
            print(i)

_song = songs(["May god bless you, ","Have a sunshine on you,","Happy Birthday to you !"])
print(_song.sing_me_a_song())'''

'''Exercise 3
Define a class called Lunch.Its __init__() method should have two arguments:selfanf menu.Where menu is a string. 
Add a method called menu_price.It will involve a ifstatement:

if "menu 1" print "Your choice:", menu, "Price 12.00", if "menu 2" print "Your choice:", menu, "Price 13.40", else print "Error in menu".
To check if it works define: Paul=Lunch("menu 1") and call Paul.menu_price().'''

'''class lunch:
    def __init__(self,menu1):
        self.menu1= menu1
    def menu_price(self):
        if self.menu1=="menu1":
            print("your choice :",self.menu1,"price 12.00")
        elif self.menu1=="menu2":
            print("your choice :",self.menu1,"price 13.40")
        else:
           return "error in menu"

paul= lunch("menu3")
print(paul.menu_price())'''

****'''Python super() function****
When a class inherits all properties and behavior from the parent class is called inheritance.
In such a case, the inherited class is a subclass and the latter class is the parent class.

In child class, we can refer to parent class by using the super() function.
The super function returns a temporary object of the parent class that allows us to call a parent class method inside a child class method.

Benefits of using the super() function.

We are not required to remember or specify the parent class name to access its methods.
We can use the super() function in both single and multiple inheritances.
The super() function support code reusability as there is no need to write the entire function'''

class Company:
    def company_name(self):
        return 'Google'

class Employee(Company):
    def info(self):
        # Calling the superclass method using super()function
        c_name = super().company_name()
        print("Jessa works at", c_name)

# Creating object of child class
emp = Employee()
emp.info()

'''A new class named F14 is initated for you which inherits from the parent class Jets.

Instead of taking parameters other than self such as name and country,
initiate the new class so that name is always fixed to "F14" and origin is always fixed to "USA"

Make sure the new class has its own initation method (constructor or __init__) ehich takes only one parameter:self and
overrides name and origin attributes as those don't change for an F14 fighter jet.'''


'''class Jets:

    def __init__(self, name, country):
        self.type = "Jet"
        self.area = "Air"
        self.name = name
        self.origin = country


# Type your code below inside the new class

class F14(Jets):

    def __init__(self):
        self.name = 'F14'
        self.origin = 'USA'


a = F14()
print(a.origin)
print(a.name)'''

'''Write a Python program to create a Vehicle class with max_speed and mileage instance attributes.'''

'''class vehicle:
    def __init__(self,max_speed,mileage):
        self.max_speed = max_speed
        self.mileage = mileage

x = vehicle(200,20)
print(x.max_speed,x.mileage)'''


'''Create a Vehicle class without any variables and methods'''

'''class vehicle:
    def show(self):
        pass
x = vehicle()
print(x.show())'''

#without any variables

'''class vehicle:
    pass'''


'''OOP Exercise 3: Create a child class Bus that will inherit all of the variables and methods of the Vehicle class'''

class Vehicle:

    def __init__(self, name, max_speed, mileage):
        self.n = name
        self.max_speed = max_speed
        self.mileage = mileage

class bus(Vehicle):
    pass

x = bus('volvo',150,20)

print(x.n,x.max_speed,x.mileage)
***********************************************************************************************************************************************************************
*******'''Create a Bus class that inherits from the Vehicle class. Give the capacity argument of Bus.**********
seating_capacity() a default value of 50.
Use the following code for your parent Vehicle class.'''
'''class Vehicle:
    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

    def seating_capacity(self, capacity):
        return f"The seating capacity of a {self.name} is {capacity} passengers"

class bus(Vehicle):
    def seating_capacity(self, capacity=50):
        return super().seating_capacity(capacity=50)

y = bus('Volvo',200,20)

print(y.seating_capacity())'''


'''OOP Exercise 5: Define a property that must have the same value for every class instance (object)
Define a class attribute”color” with a default value white. I.e., Every Vehicle should be white.

Use the following code for this exercise.'''

'''class Vehicle:

    Color = 'white'

    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

class Bus(Vehicle):
    pass

class Car(Vehicle):
    pass

x = Bus('Volvo',200,20)
y= Car ('Audi',220,20)

print(f'color :{x.Color},name :{x.name},max speed: {x.max_speed},mileage:{x.mileage}')'''

'''Home » Python Exercises » Python Object-Oriented Programming (OOP) Exercise: Classes and Objects Exercises
Python Object-Oriented Programming (OOP) Exercise: Classes and Objects Exercises
Updated on: December 8, 2021 | 36 Comments

This Object-Oriented Programming (OOP) exercise aims to help you to learn and practice OOP concepts. All questions are tested on Python 3.

Python Object-oriented programming (OOP) is based on the concept of “objects,” which can contain data and code: data in the form of instance variables (often known as attributes or properties), and code, in the form method. I.e., Using OOP, we encapsulate related properties and behaviors into individual objects.

What is included in this Python OOP exercise?

This OOP classes and objects exercise includes 8 different programs, questions, and challenges. All solutions are tested on Python 3.


This OOP exercise covers questions on the following topics:

Class and Object creation
Instance variables and Methods, and Class level attributes
Model systems with class inheritance i.e., inherit From Other Classes
Parent Classes and Child Classes
Extend the functionality of Parent Classes using Child class
Object checking

When you complete each question, you get more familiar with the Python OOP. Let us know if you have any alternative solutions. It will help other developers.

Use Online Code Editor to solve exercise questions.

Refer:

Guide on Python OOP
Inheritance in Python
Table of contents
OOP Exercise 1: Create a Class with instance attributes
OOP Exercise 2: Create a Vehicle class without any variables and methods
OOP Exercise 3: Create a child class Bus that will inherit all of the variables and methods of the Vehicle class
OOP Exercise 4: Class Inheritance
OOP Exercise 5: Define a property that must have the same value for every class instance (object)
OOP Exercise 6: Class Inheritance
OOP Exercise 7: Check type of an object
OOP Exercise 8: Determine if School_bus is also an instance of the Vehicle class

OOP Exercise 1: Create a Class with instance attributes
Write a Python program to create a Vehicle class with max_speed and mileage instance attributes.

Refer:

Classes and Objects in Python
Instance variables in Python
Show Solution
OOP Exercise 2: Create a Vehicle class without any variables and methods
Show Solution
OOP Exercise 3: Create a child class Bus that will inherit all of the variables and methods of the Vehicle class
Given:

class Vehicle:

    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

Create a Bus object that will inherit all of the variables and methods of the parent Vehicle class and display it.

Expected Output:

Vehicle Name: School Volvo Speed: 180 Mileage: 12
Refer: Inheritance in Python

Show Solution
OOP Exercise 4: Class Inheritance
Given:

Create a Bus class that inherits from the Vehicle class. Give the capacity argument of Bus.seating_capacity() a default value of 50.

Use the following code for your parent Vehicle class.

class Vehicle:
    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

    def seating_capacity(self, capacity):
        return f"The seating capacity of a {self.name} is {capacity} passengers"

Expected Output:

The seating capacity of a bus is 50 passengers
Refer:

Inheritance in Python
Polymorphism in Python
Show Hint
First, use method overriding.
Next, use default method argument in the seating_capacity() method definition of a bus class.
Show Solution
class Vehicle:
    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

    def seating_capacity(self, capacity):
        return f"The seating capacity of a {self.name} is {capacity} passengers"

class Bus(Vehicle):
    # assign default value to capacity
    def seating_capacity(self, capacity=50):
        return super().seating_capacity(capacity=50)

School_bus = Bus("School Volvo", 180, 12)
print(School_bus.seating_capacity())
 Run
OOP Exercise 5: Define a property that must have the same value for every class instance (object)
Define a class attribute”color” with a default value white. I.e., Every Vehicle should be white.

Use the following code for this exercise.

class Vehicle:

    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

class Bus(Vehicle):
    pass

class Car(Vehicle):
    pass

Expected Output:

Color: White, Vehicle name: School Volvo, Speed: 180, Mileage: 12
Color: White, Vehicle name: Audi Q5, Speed: 240, Mileage: 18
Refer: Class Variable in Python

Show Hint
Show Solution
Variables created in .__init__() are called instance variables. An instance variable’s value is specific to a particular instance of the class. For example, in the solution, All Vehicle objects have a name and a max_speed, but the name and max_speed variables’ values will vary depending on the Vehicle instance.

On the other hand, the class variable is shared between all class instances. You can define a class attribute by assigning a value to a variable name outside of .__init__().

class Vehicle:
    # Class attribute
    color = "White"

    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

class Bus(Vehicle):
    pass

class Car(Vehicle):
    pass

School_bus = Bus("School Volvo", 180, 12)
print(School_bus.color, School_bus.name, "Speed:", School_bus.max_speed, "Mileage:", School_bus.mileage)

car = Car("Audi Q5", 240, 18)
print(car.color, car.name, "Speed:", car.max_speed, "Mileage:", car.mileage)
Run'''

'''Home » Python Exercises » Python Object-Oriented Programming (OOP) Exercise: Classes and Objects Exercises
Python Object-Oriented Programming (OOP) Exercise: Classes and Objects Exercises
Updated on: December 8, 2021 | 36 Comments

This Object-Oriented Programming (OOP) exercise aims to help you to learn and practice OOP concepts. All questions are tested on Python 3.

Python Object-oriented programming (OOP) is based on the concept of “objects,” which can contain data and code: data in the form of instance variables (often known as attributes or properties), and code, in the form method. I.e., Using OOP, we encapsulate related properties and behaviors into individual objects.

What is included in this Python OOP exercise?

This OOP classes and objects exercise includes 8 different programs, questions, and challenges. All solutions are tested on Python 3.


This OOP exercise covers questions on the following topics:

Class and Object creation
Instance variables and Methods, and Class level attributes
Model systems with class inheritance i.e., inherit From Other Classes
Parent Classes and Child Classes
Extend the functionality of Parent Classes using Child class
Object checking

When you complete each question, you get more familiar with the Python OOP. Let us know if you have any alternative solutions. It will help other developers.

Use Online Code Editor to solve exercise questions.

Refer:

Guide on Python OOP
Inheritance in Python
Table of contents
OOP Exercise 1: Create a Class with instance attributes
OOP Exercise 2: Create a Vehicle class without any variables and methods
OOP Exercise 3: Create a child class Bus that will inherit all of the variables and methods of the Vehicle class
OOP Exercise 4: Class Inheritance
OOP Exercise 5: Define a property that must have the same value for every class instance (object)
OOP Exercise 6: Class Inheritance
OOP Exercise 7: Check type of an object
OOP Exercise 8: Determine if School_bus is also an instance of the Vehicle class

OOP Exercise 1: Create a Class with instance attributes
Write a Python program to create a Vehicle class with max_speed and mileage instance attributes.

Refer:

Classes and Objects in Python
Instance variables in Python
Show Solution
OOP Exercise 2: Create a Vehicle class without any variables and methods
Show Solution
OOP Exercise 3: Create a child class Bus that will inherit all of the variables and methods of the Vehicle class
Given:

class Vehicle:

    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

Create a Bus object that will inherit all of the variables and methods of the parent Vehicle class and display it.

Expected Output:

Vehicle Name: School Volvo Speed: 180 Mileage: 12
Refer: Inheritance in Python

Show Solution
OOP Exercise 4: Class Inheritance
Given:

Create a Bus class that inherits from the Vehicle class. Give the capacity argument of Bus.seating_capacity() a default value of 50.

Use the following code for your parent Vehicle class.

class Vehicle:
    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

    def seating_capacity(self, capacity):
        return f"The seating capacity of a {self.name} is {capacity} passengers"

Expected Output:

The seating capacity of a bus is 50 passengers
Refer:

Inheritance in Python
Polymorphism in Python
Show Hint
First, use method overriding.
Next, use default method argument in the seating_capacity() method definition of a bus class.
Show Solution
class Vehicle:
    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

    def seating_capacity(self, capacity):
        return f"The seating capacity of a {self.name} is {capacity} passengers"

class Bus(Vehicle):
    # assign default value to capacity
    def seating_capacity(self, capacity=50):
        return super().seating_capacity(capacity=50)

School_bus = Bus("School Volvo", 180, 12)
print(School_bus.seating_capacity())
 Run
OOP Exercise 5: Define a property that must have the same value for every class instance (object)
Define a class attribute”color” with a default value white. I.e., Every Vehicle should be white.

Use the following code for this exercise.

class Vehicle:

    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

class Bus(Vehicle):
    pass

class Car(Vehicle):
    pass

Expected Output:

Color: White, Vehicle name: School Volvo, Speed: 180, Mileage: 12
Color: White, Vehicle name: Audi Q5, Speed: 240, Mileage: 18
Refer: Class Variable in Python

Variables created in .__init__() are called instance variables. An instance variable’s value is specific to a particular instance of the class. For example, in the solution, All Vehicle objects have a name and a max_speed, but the name and max_speed variables’ values will vary depending on the Vehicle instance.

On the other hand, the class variable is shared between all class instances. You can define a class attribute by assigning a value to a variable name outside of .__init__().

class Vehicle:
    # Class attribute
    color = "White"

    def __init__(self, name, max_speed, mileage):
        self.name = name
        self.max_speed = max_speed
        self.mileage = mileage

class Bus(Vehicle):
    pass

class Car(Vehicle):
    pass

School_bus = Bus("School Volvo", 180, 12)
print(School_bus.color, School_bus.name, "Speed:", School_bus.max_speed, "Mileage:", School_bus.mileage)

car = Car("Audi Q5", 240, 18)
print(car.color, car.name, "Speed:", car.max_speed, "Mileage:", car.mileage)
 Run'''

'''OOP Exercise 6: Class Inheritance
Given:

Create a Bus child class that inherits from the Vehicle class. 
The default fare charge of any vehicle is seating capacity * 100. 
If Vehicle is Bus instance, we need to add an extra 10% on full fare as a maintenance charge. 
So total fare for bus instance will become the final amount = total fare + 10% of the total fare.'''

'''class Vehicle:
    def __init__(self, name, mileage, capacity):
        self.name = name
        self.mileage = mileage
        self.capacity = capacity

    def fare(self):
        return self.capacity * 100

class Bus(Vehicle):
    def fare(self):
        total = super().fare()
        final_amount= total+(10/100*total)
        return final_amount

School_bus = Bus("School Volvo", 12, 50)
print("Total Bus fare is:", School_bus.fare())'''

'''OOP Exercise 7: Check type of an object
Write a program to determine which class a given Bus object belongs to.'''
class Vehicle:
    def __init__(self, name, mileage, capacity):
        self.name = name
        self.mileage = mileage
        self.capacity = capacity

class Bus(Vehicle):
    pass

School_bus = Bus("School Volvo", 12, 50)

print(issubclass(Bus,Vehicle))
print(type(School_bus))


