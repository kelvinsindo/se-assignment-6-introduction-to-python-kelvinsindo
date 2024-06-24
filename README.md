[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/WfNmjXUk)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15319333&assignment_repo_type=AssignmentRepo)
# SE-Assignment-6
 Assignment: Introduction to Python
Instructions:
Answer the following questions based on your understanding of Python programming. Provide detailed explanations and examples where appropriate.

 Questions:

1. Python Basics:
   - What is Python, and what are some of its key features that make it popular among developers? Provide examples of use cases where Python is particularly effective.

   Python is a high-level, interpreted programming language known for its simplicity and readability.

Key features of python:
1) simple and easy to learn: Python's syntax is clear and concise, making it easy for beginners to grasp and write code quickly.
2) Expressive and readable: Python's readability allows developers to write logical and clear code, enhancing collaboration and maintainability.
3) Interpreted and interactive: Python's interpreter allows for immediate code execution and experimentation.
4) Rich standard library:  Python comes with a large standard library that provides modules and functions for various tasks, minimizing the need for external libraries.
5) Dynamically typed: Python uses dynamic typing, allowing variables to be declared without specifying their type, which simplifies development and speeds up coding.
6) Cross-platform: Python is available on various platforms making it versatile for developing applications across different environments. 

Python is used in: web development, data science and machine learning, automation and scripting, game development, and embedded systems.

2. Installing Python:
   - Describe the steps to install Python on your operating system (Windows, macOS, or Linux). Include how to verify the installation and set up a virtual environment.

Step to install python:
1) Download python from the official website "python.org".
2) Follow the installation process and ensure to have set the path for your software.
3) Confirm if python is installed in you machine by opening the powershell and type the command `python --version` the press enter to check on the installation.
4) Setup a virtual environment to edit your python script on a code editor such as vs code. Ensure it is installed in your machine. Open the extensions menu and install python. This will help you run python scripts.


3. Python Syntax and Semantics:
   - Write a simple Python program that prints "Hello, World!" to the console. Explain the basic syntax elements used in the program.

print("Hello, World!")

print() is a built-in function in Python used to output text or other data to the console.
"Hello, World!" is a string literal. 

4. Data Types and Variables:
   - List and describe the basic data types in Python. Write a short script that demonstrates how to create and use variables of different data types.

   Integer: Represents whole numbers without a fractional component.
   Floating point: Represents numbers with a fractional component.
   String: Represents sequences of characters.
   Boolean: Represents truth values 'True' or 'False'.
   List: Represents ordered collections of items.
   Tuple: Represents ordered, immutable collections of items.
   Dictionary: Represents collections of key-value pairs.
   Set: Represents unordered collections of unique items.

   Examples:
   my_bool = True
   print("Boolean:", my_bool)

   my_list = [1, 2, 3, 4, 5]
   print("List:", my_list)

   my_tuple = (1, 2, 3, 4, 5)
   print("Tuple:", my_tuple)

   my_dict = {'name': 'Alice', 'age': 25}
   print("Dictionary:", my_dict)

5. Control Structures:
   - Explain the use of conditional statements and loops in Python. Provide examples of an `if-else` statement and a `for` loop.

Conditional statements in Python allow you to execute different blocks of code based on certain conditions.

Example:
age = 18

if age >= 18:
   print("You are an adult.")
else:
   print("You are a minor.")

Loops allow you to execute a block of code repeatedly.

Example:
fruits = ["apple", "banana", "mango"]

for fruit in fruits:
    print(fruit)

6. Functions in Python:
   - What are functions in Python, and why are they useful? Write a Python function that takes two arguments and returns their sum. Include an example of how to call this function.

Functions in Python are blocks of reusable code that perform a specific task. 
Importance of functions in python:
1) Code Reusability: Functions allow you to write code once and use it multiple times.
2) Modularity: Functions help in breaking down complex problems into smaller, manageable pieces.
3) Improved Readability: Functions make the code more organized and easier to read.
4) Ease of Maintenance: Functions make it easier to update and maintain the code.

Example:
def add_numbers(a, b):
    return a + b

result = add_numbers(9, 6)
print("The sum is:", result)

7. Lists and Dictionaries:
   - Describe the differences between lists and dictionaries in Python. Write a script that creates a list of numbers and a dictionary with some key-value pairs, then demonstrates basic operations on both.

   Elements in a list have a defined order, and each element can be accessed by its index, whereas dictionaries do not maintain the order of elements.
   List elements are accessed using zero-based indices, whereas each element is a key-value pair, where keys are unique in dictionaries.
   Lists can contain duplicate elements, whereas each key in a dictionary must be unique; values can be duplicated.
   Lists are defined using square brackets, whereas dictionaries are defined using curly braces.

Example:
numbers = [1, 2, 3, 4, 5]
print("Original list:", numbers)

person = {
    'name': 'Alice',
    'age': 25,
    'city': 'New York'
}

print("Original dictionary:", person)


8. Exception Handling:
   - What is exception handling in Python? Provide an example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script.

Exception handling in python allows you to handle errors gracefully without crashing your program.

Example:

def divide(a, b):
    try:
        result = a / b
        return result
    except ZeroDivisionError:
        print("Error: Cannot divide by zero!")
        return None
    finally:
        print("Division operation completed.")
print("Test Case 1:")
divide(10, 2)

9. Modules and Packages:
   - Explain the concepts of modules and packages in Python. How can you import and use a module in your script? Provide an example using the `math` module.

   Modules
   A module in Python is a single file that contains definitions of functions, classes, and variables.

   Packages
   A package in Python is a way of organizing related modules into a directory hierarchy. 

   How to use import module?
   import math
   number = 25
   square_root = math.sqrt(number)

   print(f"The square root of {number} is {square_root:.2f}")

10. File I/O:
    - How do you read from and write to files in Python? Write a script that reads the content of a file and prints it to the console, and another script that writes a list of strings to a file.

The program below executes the read and write to files in python.

def write_file(file_path, lines):
    with open(file_path, 'w') as file:
        for line in lines:
            file.write(line + '\n')

def read_file(file_path):
    try:
        with open(file_path, 'r') as file:
            content = file.read()
            print(content)
    except FileNotFoundError:
        print(f"The file {file_path} does not exist.")

file_path = 'output.txt'
lines = ["Hello, world!", "This is a test.", "Writing to a file in Python."]
write_file(file_path, lines)
read_file(file_path)


# Submission Guidelines:
- Your answers should be well-structured, concise, and to the point.
- Provide code snippets or complete scripts where applicable.
- Cite any references or sources you use in your answers.
- Submit your completed assignment by [due date].


