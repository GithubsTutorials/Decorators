## Introduction to Decorators
Definition: A decorator in Python is a function that takes another function as an argument, extends its behavior, and returns a new function with the extended behavior.

Purpose: Decorators are commonly used to add functionality to an existing function in a clean, readable, and reusable ways.

### Syntax - @decorator_name

### Introducing a Decorator

def create_deco(func):

    def wrappers():
        print("Enhance the Message : ")
        func()
        print("Enhanced well! : ")
    return wrappers

    
### Here, you’re creating a decorator called my_decorator that adds some functionality before and after the execution of func.

### Applying the Decorator
@create_deco

def ribbon():

    print("Perfecto!!!!")

ribbon()

### How It Works
When @create_deco is placed above ribbon, it transforms ribbon by passing it to create_deco.

create_deco returns the wrapper function, which wraps around ribbon, adding the extra behavior.




## Types of Decorators
1.Function Decorators - A function decorator in Python is a design pattern that allows you to modify or extend the behavior of a function or method without changing its actual code.

2.Class Decorators - Classs decorators are a way to modify nd enhances the behavior of classes. 

3.Custom Decorators - User define decorators to add custom behavior to functions or methods 

4.Built in Decorators(Static and Class)


### @staticmethod - 
### Purpose:  Static methods do not require access to the instance (self) or the class (cls). They are just regular functions that happen to reside in a class body.

class MyClass:

    @staticmethod
    def my_static_method():
        print("This is a static method.")

MyClass.my_static_method()


### @classmethod -
### Purpose: Used to define a class method. Class methods receive the class (cls) as their first argument instead of the instance (self).
class MyClass:

    @classmethod
    def my_class_method(cls):
        print(f"This is a class method of {cls}")

MyClass.my_class_method()






