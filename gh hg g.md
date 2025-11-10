**Lesson 04: Operators in Python**

Python supports many types of operators.
The following table lists Python operators **from highest to lowest priority (precedence).**

With variables and operators, we can construct expressions to solve real-world problems.

In computer science, an **expression** is a syntactic unit composed of one or more constants, variables, functions, and operators.
A programming language evaluates the expression to produce a result.

Regardless of the programming language, **constructing expressions is a fundamental skill.**
| Operator(s)                                     | Description                      |
|--------------------------------------------------|----------------------------------|
| `[]` , `[:]`                                     | Indexing, slicing               |
| `**`                                             | Exponent (power)                |
| `~` , `+` , `-`                                   | Bitwise NOT, unary plus, unary minus |
| `*` , `/` , `%` , `//`                            | Multiply, divide, modulus, floor division |
| `+` , `-`                                         | Addition, subtraction           |
| `>>` , `<<`                                       | Bitwise right shift, bitwise left shift |
| `&`                                              | Bitwise AND                     |
| `^` , `|`                                         | Bitwise XOR, bitwise OR         |
| `<=` , `<` , `>` , `>=`                           | Comparison operators            |
| `==` , `!=`                                       | Equality and inequality         |
| `is` , `is not`                                   | Identity operators              |
| `in` , `not in`                                   | Membership operators            |
| `not` , `or` , `and`                              | Logical operators               |
| `=` , `+=` , `-=` , `*=` , `/=` , `%=` , `//=` , `**=` , `&=` , `|=` , `^=` , `>>=` , `<<=` | Assignment operators |
> **Note:**  
> Operator precedence means the order in which operations are performed when an expression contains multiple operators.  
> If you're unsure about the precedence in a complicated expression, you can always use parentheses `()` to explicitly control the order of execution.

**Arithmetic Operators**

Python provides a rich variety of arithmetic operators. Besides the most common addition, subtraction, multiplication, and division, it also includes floor division, modulus (remainder), and exponentiation operators. The example below demonstrates how to use arithmetic operators.

```python
"""
Arithmetic Operators

Version: 1.0
Author: ashewbytes
"""

print(321 + 12)     # Addition → Output: 333
print(321 - 12)     # Subtraction → Output: 309
print(321 * 12)     # Multiplication → Output: 3852
print(321 / 12)     # Division → Output: 26.75
print(321 // 12)    # Floor division (integer result) → Output: 26
print(321 % 12)     # Modulus (remainder) → Output: 9
print(321 ** 12)    # Exponentiation (power) → Output: 1196906950228928915420617322241
```
Arithmetic operations follow the rule of performing multiplication and division before addition and subtraction, which is the same as what you learned in mathematics.
In other words, multiplication and division have higher precedence than addition and subtraction.
If exponentiation is involved, exponentiation has even higher precedence than multiplication and division.

If you want to change the order of execution in an arithmetic expression, you can use parentheses () (typed in English input mode).
The expression inside the parentheses will be executed first, as shown in the example below.

```python
"""
Arithmetic Operation Precedence

Version: 1.0
Author: ashewbytes
"""

print(2 + 3 * 5)           # 17
print((2 + 3) * 5)         # 25
print((2 + 3) * 5 ** 2)    # 125
print(((2 + 3) * 5) ** 2)  # 625
```

**Assignment Operators**

The assignment operator is one of the most commonly used operators. Its purpose is to assign the value on the right side to the variable on the left side.
Assignment operators can also be combined with arithmetic operators to form compound assignment operators. For example:
a += b is equivalent to a = a + b,
and a *= a + 2 is equivalent to a = a * (a + 2).
The example below demonstrates the use of assignment operators and compound assignment operators.
```python
"""
Assignment Operators and Compound Assignment Operators

Version: 1.0
Author: ashewbytes
"""

a = 10
b = 3
a += b        # Equivalent to: a = a + b
a *= a + 2    # Equivalent to: a = a * (a + 2)
print(a)      # Try calculating what the output will be
```
> **Note:**  
> An assignment operation itself does not produce a value.  
> To solve this, Python 3.8 introduced a new assignment operator `:=`,  
> commonly known as the *walrus operator*.  
> (You can guess why it’s called that — we’ll explain when we use it later.)

### Comparison Operators and Logical Operators

Comparison operators are also called relational operators.  
They include: `==`, `!=`, `<`, `>`, `<=`, `>=`.  
These are easy to understand at first glance.

> **Note:**  
> To compare equality, Python uses `==` (double equals).  
> `=` is the assignment operator, as explained earlier.  
> To compare inequality, Python uses `!=`, which is different from the mathematical symbol `≠`.  
> In Python 2, `<>` was used to represent "not equal",  
> but in Python 3, using `<>` will cause a **SyntaxError (syntax error)**.

Comparison operators return a Boolean value: **True** or **False**.


---

Logical operators in Python are: `and`, `or`, and `not`.

- `and` literally means *"and"*.  
  It connects two Boolean values or expressions that produce Boolean values.  
  If both are `True`, the result is `True`;  
  if either one is `False`, the result is `False`.  
  If the left side of `and` is `False`, the right side will be skipped  
  (this is called **short-circuit evaluation** — if the right side is an expression, it will not run).

- `or` literally means *"or"*.  
  It also connects two Boolean values or expressions.  
  If **at least one** is `True`, the result is `True`.  
  `or` also supports short-circuiting —  
  if the left side is `True`, the right side will be skipped.

- `not` is placed before a Boolean value or expression.  
  If the value after `not` is `True`, the result becomes `False`;  
  if it is `False`, the result becomes `True`.

```python
"""
Using Comparison Operators and Logical Operators

Version: 1.0
Author: ashewbytes
"""

flag0 = 1 == 1
flag1 = 3 > 2
flag2 = 2 < 1
flag3 = flag1 and flag2
flag4 = flag1 or flag2
flag5 = not flag0

print('flag0 =', flag0)     # flag0 = True
print('flag1 =', flag1)     # flag1 = True
print('flag2 =', flag2)     # flag2 = False
print('flag3 =', flag3)     # flag3 = False
print('flag4 =', flag4)     # flag4 = True
print('flag5 =', flag5)     # flag5 = False
print(flag1 and not flag2)  # True
print(1 > 2 or 2 == 3)      # False
```

> **Note:**  
> Comparison operators have higher precedence than assignment operators.  
> So `flag0 = 1 == 1` is evaluated as `(1 == 1)` first → `True`, then assigned to `flag0`.  
>  
> The `print()` function can output multiple values separated by commas, and it automatically inserts spaces between them.

**Examples of Operators and Expressions**

**Example 1: Converting Fahrenheit to Celsius**
Requirement: Input a Fahrenheit temperature and convert it to Celsius.
The conversion formula from Fahrenheit to Celsius is: C = (F − 32) / 1.8.

> **Note:**  
> The `input` function in the code above is used to receive user input from the keyboard.  
> Since the input is taken as a string, if you want to use it as a floating-point number for further calculations,  
> you can use type conversion (as explained in the previous lesson) and convert the string (`str`) to a floating-point number (`float`) using the `float()` function.

In the code above, we formatted the output of the `print` function.  
The output string contains two `%.1f` placeholders, and these placeholders will be replaced by the two `float` variables `(f, c)` after the `%`.  
The floating-point numbers keep **1 digit after the decimal point**.  
If the string contains a `%d` placeholder, it will be replaced with an `int` value.  
If the string contains a `%s` placeholder, it will be replaced with a `str` value.

Besides the formatting method shown above, Python also supports another formatting approach:

We create a **string with placeholders**, and the letter `f` in front of the string indicates that it is a formatted string (f-string).  
The placeholders `{f:.1f}` and `{c:.1f}` can be understood as `{f}` and `{c}` first — meaning when printing, Python will replace them with the values of variables `f` and `c`.  
The part `:.1f` indicates that the value is formatted as a floating-point number, keeping **1 digit after the decimal point**.

```python
"""
Convert Fahrenheit temperature to Celsius

Version: 1.1
Author: ashewbytes
"""
f = float(input("Enter temperature in Fahrenheit: "))
c = (f - 32) / 1.8
print(f"{f:.1f}°F = {c:.1f}°C")
```

**Example 2: Calculate the circumference and area of a circle**
Requirement: Enter the radius of a circle, then calculate its circumference ( 2πr ) and area ( πr² ).

```python

"""
Calculate the circumference and area of a circle based on the radius entered.

Version: 1.0
Author: ashewbytes
"""

radius = float(input("Enter the radius of the circle: "))
perimeter = 2 * 3.1416 * radius
area = 3.1416 * radius * radius

print("Circumference: %.2f" % perimeter)
print("Area: %.2f" % area)
```

In Python, there is a built-in module called `math`, and this module defines a variable named `pi`, whose value is the mathematical constant π (pi).
If we want to use Python’s built-in `pi`, we can slightly modify the code above.

```python
"""
Calculate the circumference and area of a circle based on the input radius

Version: 1.1
Author: ashewbytes
"""
import math

radius = float(input("Enter the radius of the circle: "))
perimeter = 2 * math.pi * radius
area = math.pi * radius ** 2

print(f"Circumference: {perimeter:.2f}")
print(f"Area: {area:.2f}")
```

> **Note:**  
> The statement `import math` is used to import the `math` module.  
> Only after importing this module can we use `math.pi` to access the value of π (pi).

There is actually another way to format output. This is a new feature introduced in Python 3.8.
Just look at the code below and you will understand it.

```python
"""
Calculate the circumference and area of a circle based on the input radius

Version: 1.2
Author: ashewbytes
"""
import math

radius = float(input("Enter the radius of the circle: "))  # Input: 5.5
perimeter = 2 * math.pi * radius
area = math.pi * radius ** 2

print(f"{perimeter = :.2f}")  # Output: perimeter = 34.56
print(f"{area = :.2f}")       # Output: area = 95.03
```

> **Note:**  
> If the value of the variable `a` is `9.87`, then the formatted string `f'{a = }'` will output:  
> `a = 9.87`  
> And the formatted string `f'{a = :.1f}'` will output:  
> `a = 9.9`  
> This formatting method prints both the variable name and its value at the same time.

**Example 3: Determine whether a year is a leap year**
Requirement: Enter a year (greater than the year 1582) and determine whether it is a leap year.

```python
"""
Input a year; output True if it's a leap year, otherwise False.

Version: 1.0
Author: ashewbytes
"""

year = int(input("Enter a year: "))
is_leap = year % 4 == 0 and year % 100 != 0 or year % 400 == 0
print(f"{is_leap = }")
```

> **Note:**  
> For the **Gregorian calendar** (the calendar used today), the rules for determining a leap year are:  
> 1. A year that is **not divisible by 4** is a common year.  
> 2. A year that **is divisible by 4 but not divisible by 100** is a leap year.  
> 3. A year that **is divisible by 400** is a leap year.  
>
> The Gregorian calendar was introduced by **Pope Gregory XIII** in **October 1582** as a modification and replacement of the **Julian calendar**. We need to keep this in mind when entering a year.
>
> In the above code, we use `%` to check whether `year` is divisible by 4, 100, or 400, and then combine the three conditions using `and` and `or`.  
> The first two conditions must both be satisfied, and the third condition only needs to satisfy one of them together with the first two.

**Summary**

Through the explanations and examples above, I believe you’ve already felt the power of operators and expressions.
Many problems in actual programming are solved by constructing expressions, so variables, operators, and expressions are extremely important fundamentals for any programming language.

If there is anything in this lesson that you do not understand, don’t rush into the next lesson — first leave a comment in the discussion section, and I will reply and help you as soon as possible.

