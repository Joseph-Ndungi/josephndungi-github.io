# Advance Exception Handling

Writing dependable and sturdy code is essential to ensure that your applications can gracefully manage unexpected errors and prevent crashes. This is where error handling becomes important. In this guide we will delve into the realm of exceptions covering types of exceptions how to raise and handle them and the best practices for error management in Python.

Exceptions are interruptions, in a programs flow caused by issues like incorrect data, input mistakes in file handling or other unforeseen challenges during runtime. When these exceptions arise they disrupt the programs execution. Without mechanisms in place Python programs would abruptly stop when encountering an error. However by using tools such as the try except block we can effectively manage these exceptions and respond accordingly.

## Common Types of Exceptions in Python

Python has a wide range of built-in exception classes for different types of errors:

* ImportError – when a module or library fails to import
* IndexError – Occurs when trying to access an invalid index in a list, tuple, etc
* NameError – when referring to a variable that hasn't been defined
* TypeError – for mixing incompatible types in an operation
* ValueError – Occurs when built-in functions receive inappropriate arguments
* ZeroDivisionError – attempting to divide by zero
* FileNotFoundError – when a file cannot be found at a specified path
* KeyboardInterruption – hen the Ctrl+C keys are pressed
* SyntaxError - for errors in syntax

Catching exceptions is like using tools for different jobs. Rather than relying on a broad catch statement it’s crucial to target specific exception types. This approach enables you to distinguish between different errors and provide precise error messages, which in turn enhances the efficiency of identifying and resolving issues.

## Difference between syntax errors and runtime errors

A syntax error happens when Python can't understand what you are saying. A run-time error happens when Python understands what you are saying, but runs into trouble when following your instructions.

## The try, except, finally, and else Statements

The try block lets you test a block of code for errors.

The except block lets you handle the error.

The else block lets you execute code when there is no error.

The finally block lets you execute code, regardless of the result of the try- and except blocks.

## Syntax and usage of try-except blocks

Python typically stops and outputs an error message when an error—or exception, as we call it—occurs.

These exceptions can be handled using the try statement:

'''
try:
  print(x)
except:
  print("An exception occurred")
'''

Since the try block raises an error, the except block will be executed.

Without the try block, the program will crash and raise an error.

You can define as many exception blocks as you want.  

'''
try:
    # Code that may raise a specific exception
    ...
except SpecificException as e:
    # Handle the specific exception
    ...
except AnotherSpecificException as e:
    # Handle another specific exception
    ...
except Exception as e:
    # Handle other exceptions or provide a fallback behavior
'''

Example

'''
try:
    with open('data.csv', 'r') as file:
        csv_reader = csv.reader(file)
        for row in csv_reader:
            # Perform some calculations on the data
            result = int(row[0]) / int(row[1])
            print(f"Result: {result}")
except FileNotFoundError:
    print("The file 'data.csv' was not found.")
except IndexError:
    print("Invalid data format in the CSV file.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
except ValueError:
    print("Invalid value encountered during calculations.")
except Exception as e:
    print(f"An unexpected error occurred: {e}")
'''
