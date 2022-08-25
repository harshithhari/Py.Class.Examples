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
