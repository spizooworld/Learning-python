**Lesson 03: Variables in Python**

For beginners who want to learn programming, there are usually two common questions:

**1. What is a (computer) program?**
 
**2. What can we do by writing a (computer) program?**

Here’s how I understand it: A program is an ordered collection of data and instructions. Writing a program means using data + instructions to control the computer to do what we want it to do.

Nowadays, why do so many people choose Python for programming?
Because Python is simple and powerful. Compared to languages like C, C++, or Java, Python is much more friendly for beginners and non-professionals. Many things that require a lot of code in other languages can be done in Python using simple and elegant solutions.

From here onward, we will start with the most basic building blocks of Python and gradually learn how to use the language.

**Some Basic Computer Knowledge**

Before we start learning programming, let's understand some basic concepts about computers.

A computer’s hardware system is generally made up of five major components:
**- Arithmetic Unit
- Control Unit
- Memory
- Input Devices
- Output Devices
**
The arithmetic unit and the control unit together form the CPU (Central Processing Unit).  
The CPU executes calculations and controls all instructions.

A program is a collection of instructions. Writing a program means organizing instructions and using them to control the computer to do what we want.

Memory is divided into two categories:

| Type             | Description |
|------------------|-------------|
| Internal Memory  | Also known as RAM. The CPU can directly access it. Data and instructions are loaded here while programs run. |
| External Memory  | Storage devices like HDD or SSD. Used to permanently store files and programs. |

Input and output devices are collectively called I/O devices.

| Input Devices                       | Output Devices          |
|-------------------------------------|--------------------------|
| Keyboard, Mouse, Microphone, Camera | Monitor, Printer, Speaker |

Modern computers follow the Von Neumann architecture, which has two key ideas:
1. Memory and CPU are separate.
2. All data is represented in binary (0s and 1s).

Binary is a counting system based on “carry when reaching two”, and its essence is the same as the decimal system that humans use, which is based on “carry when reaching ten”. Humans use decimal because we have ten fingers — when all ten fingers are used up while counting, we move to the next digit through carrying. Of course, there are exceptions. The Maya civilization may have used their toes as well since they often walked barefoot, so they used a vigesimal (base-20) counting system. Because of this system, the Mayan calendar differed from the one we normally use. According to the Mayan calendar, the year 2012 was the final year of a “solar cycle”, and 2013 marked the beginning of a new one. Later, this was mistakenly and wildly spread as “the Mayans predicted the end of the world in 2012”, which is completely absurd. Today, many people speculate that the slow development of the Mayan civilization might be related to their use of the base-20 system.

For computers, binary is the easiest to implement at the hardware level because high voltage can represent 1, and low voltage can represent 0. Not every programmer needs to be familiar with binary or conversions between decimal, binary, octal, and hexadecimal. Most of the time, we can write programs without knowing these details. However, it is essential to understand that computers use binary internally — no matter what kind of data we store, it is always represented in binary form inside computer memory.

> **Note:**  
> For binary counting and how it converts to other number systems (decimal, octal, hexadecimal), you can refer to introductory computer science books such as *“Introduction to Computers”* or *“Computer Fundamentals”*.  
> We will not go into details here — readers who are interested may explore further on their own.

**Variables and Data Types**

To store data in a computer’s memory, we first need to understand the concept of a variable.
In programming languages, a variable is a carrier of data — simply put, it is a block of memory used to store data.
The value stored in a variable can be read and modified, which is the foundation of all computing and control operations.

A computer can process many types of data.
The most common type is numbers, but besides numbers, there are also text, images, audio, video, and many other data types.

Although data is stored in binary form inside the computer, we use different data types in our programs to represent these different kinds of data.

Python provides multiple built-in data types, and it also allows us to define our own custom data types (we will learn about this later).
Let’s first get familiar with the most commonly used data types in Python.

**1. Integer (int):**
Python can handle integers of any size, and it supports multiple number representations:

- Binary (e.g., 0b100, which equals 4 in decimal)

- Octal (e.g., 0o100, which equals 64 in decimal)

- Decimal (e.g., 100)

- Hexadecimal (e.g., 0x100, which equals 256 in decimal)

Run the code below and observe the output.
```python
print(0b100)   # binary integer
print(0o100)   # octal integer
print(100)     # decimal integer
print(0x100)   # hexadecimal integer
```

**2. Floating-point number (float):**

A floating-point number represents a number with decimals. It is called floating-point
because, in scientific notation, the decimal point can *float* to different positions.

In Python, floating-point numbers can be written in:

- Standard notation (e.g., `123.456`)
- Scientific notation (e.g., `1.23456e2`, which represents \( 1.23456 \times 10^2 \) )

Run the following code and observe the output:

```python
print(123.456)    # standard notation
print(1.23456e2)  # scientific notation
```

**3. String (str):**  
A string is any text enclosed in single quotes or double quotes, such as `'hello'` and `"hello"`.

**4. Boolean (bool):**  
A Boolean type has only two possible values: `True` and `False`.  
It can be used to represent real-world conditions such as **yes/no**, **true/false**, **good/bad**, **high/low**, etc.  
If a variable only has two possible states, we can use a Boolean type to store it.

## Variable Naming

For every variable, we need to give it a name — just like every person has their own name.  
In Python, variable names must follow the **rules** and **conventions** below.

---

### **Rules:**

- **Rule 1:**
A variable name is composed of letters, digits, and underscores, but cannot start with a digit.
Here, letters refers to Unicode characters, meaning technically Chinese, Japanese, Greek, and even Indian languages (like Hindi) can also be used as characters in a variable name.
However, some special characters (such as ! , @ , #, etc.) cannot appear in variable names.

We strongly recommend using only English letters for variable naming.

- **Rule 2:**  
  Python is **case-sensitive**.  
  This means `A` and `a` are two **different variables**.

- **Rule 3:**  
  Do **not** use Python **keywords** as variable names and try to **avoid reserved names**.  
  Keywords are words with special meaning in Python (such as `is`, `if`, `else`, `for`, `while`, `True`, `False`, etc.).  
  Reserved names refer to built-in functions, built-in modules, etc. (such as `int`, `print`, `input`, `str`, `math`, `os`, etc.).

---

### **Conventions (Best Practices):**

- **Convention 1:**  
  Variable names are usually written in **lowercase English letters**, and multiple words are connected with an underscore.  
  Example: `user_name`, `total_amount`

- **Convention 2:**  
  A **protected** variable starts with **one underscore**.  
  Example: `_config`

- **Convention 3:**  
  A **private** variable starts with **two underscores**.  
  Example: `__password`

Convention 2 and Convention 3 will become clear later when we learn OOP (Object-Oriented Programming).  
As a professional programmer, naming variables clearly and meaningfully is extremely important.

---

**Using Variables**

The following example demonstrates variable types and how to use variables.

```python
"""
Using variables to store data and perform addition, subtraction, multiplication, and division.

Version: 1.0
Author: ashewbytes
"""

a = 45        # define variable a and assign value 45
b = 12        # define variable b and assign value 12

print(a, b)   # 45 12
print(a + b)  # 57
print(a - b)  # 33
print(a * b)  # 540
print(a / b)  # 3.75
```
In Python, you can use the `type()` function to check the type of a variable.  
The concept of functions in programming is very similar to the concept of functions in mathematics —  
a function has a name, arguments (input), and a return value (output).  
If you don’t fully understand functions yet, don't worry — we will cover them in detail later.

```python
"""
Using the type() function to check variable types

Version: 1.0
Author: ashewbytes
"""

a = 100
b = 123.45
c = 'hello, world'
d = True

print(type(a))  # <class 'int'>
print(type(b))  # <class 'float'>
print(type(c))  # <class 'str'>
print(type(d))  # <class 'bool'>
```
You can change the type of a variable using Python's built-in functions.  
Below are some commonly used functions related to type conversion:

- `int()` : Converts a number or a string to an integer. Can specify the base (binary, octal, hex, etc.).
- `float()` : Converts a string (if possible) to a floating-point number.
- `str()` : Converts the specified object into a string. Can specify encoding when needed.
- `chr()` : Converts an integer (character code) into the corresponding character (string of length 1).
- `ord()` : Converts a character (string of length 1) into its corresponding integer (character code).

The example below demonstrates type conversion operations in Python.

```python
"""
Type Conversion of Variables

Version: 1.0
Author: ashewbytes
"""

a = 100
b = 123.45
c = "123"
d = "100"
e = "123.45"
f = "hello, world"
g = True

print(float(a))         # int 100 → float, output: 100.0
print(int(b))           # float 123.45 → int, output: 123
print(int(c))           # str "123" → int, output: 123
print(int(c, base=16))  # str "123" (hex) → int, output: 291
print(int(d, base=2))   # str "100" (binary) → int, output: 4
print(float(e))         # str "123.45" → float, output: 123.45
print(bool(f))          # non-empty string → bool, output: True
print(int(g))           # bool True → int, output: 1
print(chr(a))           # int 100 → char, output: 'd'
print(ord('d'))         # char 'd' → int, output: 100
```
> **Note:**  
> - When converting `str` to `int`, you can specify the number system using the `base` parameter.  
> - When converting `str` to `bool`, any non-empty string becomes `True`.  
> - When converting `bool` to `int`, `True → 1`, `False → 0`.  
> - In ASCII and Unicode, `'d'` corresponds to the code `100`.

**Summary**
In Python, we can use variables to store data. Variables have different data types, and the commonly used ones are int, float, str, and bool.
When needed, we can convert between these types using Python's built-in functions.
Variables can be used in operations (addition, subtraction, multiplication, division), and this is the foundation for solving many programming problems.
In the next lesson, we will learn more about variable operations.

