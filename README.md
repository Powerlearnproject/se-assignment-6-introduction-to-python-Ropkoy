[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/WfNmjXUk)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15344598&assignment_repo_type=AssignmentRepo)
# SE-Assignment-6
 Assignment: Introduction to Python
Instructions:
Answer the following questions based on your understanding of Python programming. Provide detailed explanations and examples where appropriate.

 Questions:

1. Python Basics:
   - What is Python, and what are some of its key features that make it popular among developers? Provide examples of use cases where Python is particularly effective.
     Answers:
   - Python is a computer programming language often used to build websites and software, automate tasks, and conduct data analysis.
   - Key Features
     .Readability -Easy to Read
     .Free and Open Source
     .Object-Oriented Programming Language
     .Large Standard Library Support
   - Use cases
     .Data Science and Machine Learning
     .Business Applications
     .Web Development


2. Installing Python:
   - Describe the steps to install Python on your operating system (Windows, macOS, or Linux). Include how to verify the installation and set up a virtual environment.
     Answers:
   - Head over to the official Python download page (https://www.python.org/downloads/) and download the latest stable version of the Windows installer
   - Double-click the downloaded installer (.exe file).
   - Verify Installation: Open a command prompt or terminal window and type python --version
   - If successful, you'll see the installed Python version.

3. Python Syntax and Semantics:
   - Write a simple Python program that prints "Hello, World!" to the console. Explain the basic syntax elements used in the program.
     Answers:
   - print("Hello, World!")
     .print function is a built-in function in Python that outputs data to the console.
     .() Parentheses are used to enclose arguments passed to a function. In this case, the argument is the string "Hello, World!".
     ."" double quotes: Double quotes are used to define string literals, which are sequences of characters.
     .Semicolon ; (optional): In Python, semicolons are optional at the end of statements.

4. Data Types and Variables:
   - List and describe the basic data types in Python. Write a short script that demonstrates how to create and use variables of different data types.
     Answers:
     .Integers (int): Represent whole numbers, positive, negative, or zero (e.g., 42, -100, 0).
     .Floats (float): Represent decimal numbers (e.g., 3.14, -9.25, 1.0).
     .Strings (str): Represent sequences of characters enclosed in single (') or double (") quotes (e.g., "Hello, World!",).
     .Booleans (bool): Represent logical values, True or False.
     .Lists (list): Represent ordered collections of items enclosed in square brackets [] and separated by commas.

5. Control Structures:
   - Explain the use of conditional statements and loops in Python. Provide examples of an `if-else` statement and a `for` loop.
     Answers:
     .Control structures allows one to control the flow of execution in your Python programs.
     .Code
     age = 18
if age >= 18:
  print("You are eligible to vote.")
else:
  print("You are not eligible to vote.")

6. Functions in Python:
   - What are functions in Python, and why are they useful? Write a Python function that takes two arguments and returns their sum. Include an example of how to call this function.
     Answers:
   - Functions are reusable blocks of code that perform specific tasks in Python. They promote code modularity, reusability, and readability.
   - They're useful because they improve code readability by encapsulating functionality with meaningful names, You can define a function once and then call it multiple times from different parts of your program, avoiding code duplication, they break down complex programs into smaller, manageable parts. This makes code easier to understand, maintain, and test.

7. Lists and Dictionaries:
   - Describe the differences between lists and dictionaries in Python. Write a script that creates a list of numbers and a dictionary with some key-value pairs, then demonstrates basic operations on both.
     Answers:
   - Lists:
Ordered collections of items enclosed in square brackets [].
Elements can be accessed using zero-based indexing (starting from 0).
Lists can contain duplicate elements.
Elements can be of different data types (heterogeneous).

Dictionaries:
Unordered collections of key-value pairs enclosed in curly braces {}.
Keys must be unique and immutable (often strings or numbers).
Values can be of any data type.
Accessing elements is done using keys, not indexes.

Code;
# List of numbers
numbers = [5, 2, 8, 1]

# Access first element
first_number = numbers[0]
print("First number:", first_number)

# Modify third element
numbers[2] = 10
print("Modified list:", numbers)

# Check for element (less efficient for large lists)
if 7 in numbers:
  print("7 is present")
else:
  print("7 is not present")

# Loop through elements
for number in numbers:
  print(number)

# Dictionary with key-value pairs
person = {"name": "Bob", "age": 35}

# Access value by key
name = person["name"]
print("Name:", name)

# Update age
person["age"] = 36
print("Updated dictionary:", person)

# Check for key existence
if "city" in person:
  print("city key exists")
else:
  print("city key does not exist")

# Loop through key-value pairs
for key, value in person.items():
  print(key, ":", value)


8. Exception Handling:
   - What is exception handling in Python? Provide an example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script.
     Answers:
   - It's mechanism in Python to manage errors or unexpected situations that may arise during program execution.
   - Script;    
def divide(numerator, denominator):
  """
  This function divides two numbers and handles potential division by zero.
  """
  try:
    result = numerator / denominator
  except ZeroDivisionError:
    print("Error: Cannot divide by zero.")
  finally:
    print("Division operation completed.")

# Example usage
divide(10, 2)  # Successful division
divide(10, 0)  # Triggers ZeroDivisionError
print("Executes (after finally).")

9. Modules and Packages:
   - Explain the concepts of modules and packages in Python. How can you import and use a module in your script? Provide an example using the `math` module.
    Answers:
     .Modules: Modules are essentially Python files (.py) containing reusable code like functions, classes, and variables. They promote code organization and reusability.
     .Packages: Packages are directories containing multiple modules and potentially sub-packages. They provide a hierarchical structure for organizing related modules. A special file named __init__.py (can be empty) is required within a package directory to mark it as a Python package.
     Script;
     import module_name


10. File I/O:
    - How do you read from and write to files in Python? Write a script that reads the content of a file and prints it to the console, and another script that writes a list of strings to a file.
     Answers;
    - Steps
      .Open the file: Use the open() function with the filename and access mode ('r' for reading). This returns a file object.
      .Read the content: Use methods like read() (reads entire file), readline() (reads a single line), or readlines() (reads all lines as a list) on the file object.
      .Close the file: Ensure you close the file object using close() to release resources.
    - Script
      def read_file(filename):
  """
  This function reads the contents of a text file and prints them to the console.
  """
  try:
    with open(filename, 'r') as file:
      content = file.read()
      print(content)
  except FileNotFoundError:
    print(f"Error: File '{filename}' not found.")
# Example usage
read_file("financebill.txt")  # file name

References
- gpt
- Google (several sources)
# Submission Guidelines:
- Your answers should be well-structured, concise, and to the point.
- Provide code snippets or complete scripts where applicable.
- Cite any references or sources you use in your answers.
- Submit your completed assignment by [due date].


