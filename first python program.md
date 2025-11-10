**Lesson 02: First Python Program**

In the previous lesson, we learned about the past and present of Python and prepared the interpreter environment needed to run Python programs. Now everyone must be eager to start writing code.

But a new question appears:
Where do we write Python programs, and how do we run them?

We can write our Python code in the code editor window. After writing the code, right-click inside the window and select “Run” to execute it. The output of the program will appear in the Run panel below, as shown in the image.

<img width="1488" height="972" alt="image" src="https://github.com/user-attachments/assets/d182af20-2e75-4ec9-b8c7-28652ccf79d3" />


**Hello, World**

According to industry tradition, the first program we write when learning any programming language is to output "hello, world". This originates from the classic book “The C Programming Language”, written by the legendary Dennis Ritchie (father of the C language, co-creator of the Unix operating system along with Ken Thompson) and Brian Kernighan (inventor of the awk language). The first example code in that book prints "hello, world".
Below is the Python version of that program.
```python
print('hello, world')
```
> **Note:**  
> The parentheses `()` and single quotes `' '` in the code above must be typed using **English input mode**.

The code above contains only one statement. In this statement, we use a function called print, which allows us to output the specified content. The 'hello, world' inside the parentheses of the print function is a string, which represents a piece of text. In Python, we can use either single quotes or double quotes to represent a string.

Unlike programming languages such as C, C++, or Java, Python statements do not require a semicolon to indicate the end of the statement. This means that if we want to write another statement, we simply press Enter to move to a new line, as shown in the code below.

Additionally, Python code does not require a main function as an entry point in order to run. In C, C++, or Java, providing an entry function is required in order to make the program executable — most programmers are familiar with this — but in Python, it is not necessary.
```python
print('hello, world')
print('goodbye, world')
```
If you do not use an integrated development environment like PyCharm, you can also run Python programs by directly calling the Python interpreter.

We can save the code above into a file named `example01.py`.

For Windows systems, let's assume the file is located in:

`C:\code\`

Open **Command Prompt** or **PowerShell**, and enter the following command to run it:

```bash
python C:\code\example01.py
```
You can try modifying the code above — for example, replace 'hello, world' with any other text or write multiple print statements to see different outputs.
> **Note:**  
> When writing Python code, it is best to write only **one statement per line**.  
> Although we *can* use `;` to place multiple statements on a single line, it makes the code messy and harder to read.

**Commenting Your Code**

Comments are an important part of any programming language.
They are used to explain what the code does, which improves readability.
We can also temporarily disable a piece of code by turning it into a comment, and when needed, we can remove the comment marks to make the code run again.

In short:
**Comments make your code easier to understand, and they do not affect the execution of your program.**

**There are two types of comments in Python:**

**1. Single-line comment**
Starts with # followed by a space.
Everything after # on that line will be treated as a comment.

**2. Multi-line comment**
Written using three quotation marks (""") at the beginning and at the end.
Usually used for longer explanations over multiple lines.
```python
"""
First Python Program - hello, world

Version: 1.0
Author: ashewbytes
"""
# print('hello, world')
print("Hello, World!")
```

**Summary**

At this point, we have successfully run our first Python program — feels great, right?
If you continue learning and keep practicing, after some time you will be able to use Python to build many more powerful and exciting things.

Today, programming is just like learning English — for many people, it has become a skill that must be mastered.
