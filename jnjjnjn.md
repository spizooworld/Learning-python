## Lesson 05: Branching Structure

Up to now, the Python code we have written has been executed line by line in sequence, which is called a sequential structure. However, a sequential structure alone cannot solve all problems. For example, if we design a game where the condition to pass the first level is that the player must earn 1000 points, then after the first level is completed, we need to decide whether to enter the second level or tell the player “Game Over” based on the score. In such a scenario, our code will produce two branches, and only one of these branches will be executed. There are many similar situations, and we call this structure a “branching structure” or “selection structure.” Give yourself one minute — you should be able to think of at least five similar examples. Try it now!

### Using if and else to construct branching structures

In Python, to construct branching structures, you can use the keywords `if`, `elif`, and `else`. A **keyword** refers to a word that has a special meaning in a programming language. For example, `if` and `else` are keywords specifically used to build branching structures, and obviously, you cannot use them as variable names. Of course, we don’t necessarily use all three keywords every time we construct a branching structure. We will explain this through examples below.
Let's write a Body Mass Index (BMI) calculator. BMI, also known as body mass index, is an international standard commonly used to measure whether a person's weight is appropriate and whether they are healthy. The formula is shown below. Generally, it is considered that $\small{18.5 \le BMI < 24}$ is the normal range, $\small{BMI < 18.5}$ indicates underweight, $\small{BMI \ge 24}$ indicates overweight, and $\small{BMI \ge 27}$ falls into the obesity category.

$$
BMI = \frac{weight}{height^{2}}
$$

> **Explanation**: In the above formula, weight is measured in kilograms (kg), and height is measured in meters (m).
```python
"""
BMI Calculator

Version: 1.0
Author: ashewbytes
"""
height = float(input('Height (cm): '))
weight = float(input('Weight (kg): '))
bmi = weight / (height / 100) ** 2
print(f'{bmi = :.1f}')
if 18.5 <= bmi < 24:
    print('You are in great shape!')
```
> **Tip**: There is a `:` at the end of the `if` statement, and it is a colon entered using the English input method; the special characters such as `'`, `"`, `=`, `(`, `)` typed in the program are all entered while using the English input method — this has been mentioned before. Many beginners often overlook this point, and when they run the code, they will see a bunch of error messages. Of course, by carefully reading the error messages, it's easy to find where the problem is, but it is **strongly recommended** that when writing code, you **switch to the English input method**, as this can avoid a lot of unnecessary trouble.

In the above code, after calculating and printing the BMI, we added a branching structure. If the condition $\small{18.5 \le BMI < 24}$ is met, the program will output “You are in great shape!”, but if the condition is not met, this output will not appear. This is what we meant earlier by having different execution paths in the code — some code statements may not be executed. After the `if` keyword, we provided an expression `18.5 <= bmi < 24`. As stated earlier, relational operations produce a Boolean value. If the Boolean value after `if` is `True`, then the indented `print('You are in great shape!')` under the `if` statement (indented by four spaces) will be executed. Let’s input a few sets of data and run the code above, as shown below.

First input:
```
Height (cm): 175
Weight (kg): 68
bmi = 22.2
You are in great shape!
```

Second input:

```
Height (cm): 175
Weight (kg): 95
bmi = 31.0
```


Third input:

```
Height (cm): 175
Weight (kg): 50
bmi = 16.3
```
Only the first set of height and weight inputs resulted in a BMI within the range of 18.5 to 24, so the `if` condition was triggered, and “You are in great shape” was printed. It should be noted that unlike programming languages such as C, C++, and Java, Python does not use curly braces to form code blocks but **uses indentation to represent the hierarchical structure of the code**. If multiple statements need to be executed when the `if` condition is satisfied, they only need to maintain the same indentation. In other words, if several consecutive lines of statements have the same indentation, then they belong to the same **code block**, meaning they are executed together as a whole. Indentation can be done with any number of spaces, but **typically 4 spaces are used**. It is strongly recommended **not to use the Tab key for indentation**. If you are already used to doing that, you can set your code editor to automatically convert one Tab into four spaces — many editors support this feature, and PyCharm has this setting enabled by default.

Another point: in languages such as C, C++, and Java, `18.5 <= bmi < 24` must be written as two separate conditions, `bmi >= 18.5` and `bmi < 24`, and then the two conditions are connected with a logical AND operator. Python can also do this — for example, the previous `if` statement could also be written as `if bmi >= 18.5 and bmi < 24:`, but there is no need. Isn’t `if 18.5 <= bmi < 24:` much more elegant? Below is the same thing written in Java code. It’s fine if you don’t understand Java — just notice how different it looks compared to Python syntax.

```java
import java.util.Scanner;

class Test {

    public static void main(String[] args) {
        try (Scanner sc = new Scanner(System.in)) {
            System.out.print("Height (cm): ");
            double height = sc.nextDouble();
            System.out.print("Weight (kg): ");
            double weight = sc.nextDouble();
            double bmi = weight / Math.pow(height / 100, 2);
            System.out.printf("bmi = %.1f\n", bmi);
            if (bmi >= 18.5 && bmi < 24) {
                System.out.println("You are in great shape!");
            }
        }
    }
}
```

> **Explanation**: The above is the Java code corresponding to version 1.0 of the BMI calculator — feel free to roast it in the comments.

Next, we will slightly modify the code above. When BMI does not satisfy the condition $\small{18.5 \le BMI < 24}$, we will also display a prompt message. We can add an `else` code block after the `if` code block, which will execute when the condition given by the `if` statement is not met, as shown below. Obviously, between the `print('You are in great shape!')` under `if` and the `print('Your body is not quite standard!')` under `else`, only one of them will be executed.

```python
"""
BMI Calculator

Version: 1.1
Author: ashewbytes
"""
height = float(input('Height (cm): '))
weight = float(input('Weight (kg): '))
bmi = weight / (height / 100) ** 2
print(f'{bmi = :.1f}')
if 18.5 <= bmi < 24:
    print('You are in great shape!')
else:
    print('Your body is not quite standard!')
```
If we want to provide more accurate prompt messages, we can modify the above code again by adding more branches to the structure using the `elif` keyword, as shown below.

```python
"""
BMI Calculator

Version: 1.2
Author: ashewbytes
"""
height = float(input('Height (cm): '))
weight = float(input('Weight (kg): '))
bmi = weight / (height / 100) ** 2
print(f'{bmi = :.1f}')
if bmi < 18.5:
    print('You are underweight!')
elif bmi < 24:
    print('You are in great shape!')
elif bmi < 27:
    print('You are overweight!')
elif bmi < 30:
    print('You are mildly obese!')
elif bmi < 35:
    print('You are moderately obese!')
else:
    print('You are severely obese!')
```

We will test the above code again with the same three sets of data to see the results.

First input:

```
Height (cm): 175
Weight (kg): 68
bmi = 22.2
You are in great shape!
```

Second input:

```
Height (cm): 175
Weight (kg): 95
bmi = 31.0
You are moderately obese!
```

Third input:

```
Height (cm): 175
Weight (kg): 50
bmi = 16.3
You are underweight!
```
### Using match and case to construct branching structures

Python 3.10 introduces a new way to construct branching structures. By using the `match` and `case` keywords, we can easily build multi-branch structures. In the official Python documentation, when introducing this new syntax, they use an example of identifying HTTP response status codes — quite interesting. If you don't know what HTTP response status codes are, you can check the [MDN documentation](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Status). Below, we slightly modify the example from the official documentation to explain this syntax. First, take a look at the version implemented using the `if-else` structure.

```python
status_code = int(input('Response status code: '))
if status_code == 400:
    description = 'Bad Request'
elif status_code == 401:
    description = 'Unauthorized'
elif status_code == 403:
    description = 'Forbidden'
elif status_code == 404:
    description = 'Not Found'
elif status_code == 405:
    description = 'Method Not Allowed'
else:
    description = 'Unknown status Code'
print('Status Code Description:', description)
```
Run result:

```
Response status code: 403
Status Code Description: Forbidden
```
Below is the code implemented using the `match-case` syntax. Although it serves exactly the same purpose, the code appears simpler and more elegant.

```python
status_code = int(input('Response status code: '))
match status_code:
    case 400: description = 'Bad Request'
    case 401: description = 'Unauthorized'
    case 403: description = 'Forbidden'
    case 404: description = 'Not Found'
    case 405: description = 'Method Not Allowed'
    case _: description = 'Unknown Status Code'
print('Status Code Description:', description)
```
> **Explanation**: The `case` statement with `_` in the code acts as a wildcard. If none of the previous branches match, execution will go to `case _`. Using `case _` is optional — not every branching structure requires a wildcard option. If `case _` appears in the branch structure, it must be placed at the end; if additional branches are placed after it, those branches will be unreachable.

Of course, the `match-case` syntax has many advanced usages, which we will explain later when needed. One pattern-combining feature can be shared here. For example, if we want to group status codes `401`, `403`, and `404` into one branch, group `400` and `405` into another branch, and leave others unchanged, the code can be written like this:

```python
status_code = int(input('Response status code: '))
match status_code:
    case 400 | 405: description = 'Invalid Request'
    case 401 | 403 | 404: description = 'Not Allowed'
    case _: description = 'Unknown Status Code'
print('Status Code Description:', description)
```
Run result:

```
Response status code: 403
Status Code Description: Not Allowed
```

### Example Application of Branching Structures

#### Example 1: Piecewise function evaluation

Given the piecewise function below, input `x` and calculate `y`.

$$
y = \begin{cases} 3x - 5, & (x \gt 1) \\ x + 2, & (-1 \le x \le 1) \\ 5x + 3, & (x \lt -1) \end{cases}
$$
```python
"""
Piecewise function evaluation

Version: 1.0
Author: ashewbytes
"""
x = float(input('x = '))
if x > 1:
    y = 3 * x - 5
elif x >= -1:
    y = x + 2
else:
    y = 5 * x + 3
print(f'{y = }')
```
According to practical development needs, branching structures can be nested — meaning that within an `if`, `elif`, or `else` block, you can introduce another branching structure. For example, if the `if` condition is satisfied and indicates that a player has passed a level, you may still need to evaluate their performance based on the number of treasures or items collected (such as lighting up one, two, or three stars). In such a scenario, you would construct a new branching structure inside the existing `if`. Likewise, we can build new branching structures inside `elif` and `else` blocks — this is called a nested branching structure. Following this logic, the piecewise function evaluation above can also be written as follows.

```python
"""
Piecewise function evaluation

Version: 1.1
Author: ashewbytes
"""
x = float(input('x = '))
if x > 1:
    y = 3 * x - 5
else:
    if x >= -1:
        y = x + 2
    else:
        y = 5 * x + 3
print(f'{y = }')
```
> **Explanation**: You can evaluate for yourself which of the two approaches above is better. In the [**Zen of Python**](https://zhuanlan.zhihu.com/p/111843067), there is a saying: “**Flat is better than nested**.” The reason “flat” code is preferred is because excessive nesting makes code harder to read. Therefore, I believe the first version of the code above is the better choice.

#### Example 2: Converting percentage grades to letter grades

Requirement: If the input grade is 90 or above (including 90), output `A`; if the grade is between 80 and 90 (excluding 90), output `B`; if the grade is between 70 and 80 (excluding 80), output `C`; if the grade is between 60 and 70 (excluding 70), output `D`; if the grade is below 60, output `E`.

```python
"""
Convert percentage grade to letter grade

Version: 1.0
Author: ashewbytes
"""
score = float(input('Please enter the score: '))
if score >= 90:
    grade = 'A'
elif score >= 80:
    grade = 'B'
elif score >= 70:
    grade = 'C'
elif score >= 60:
    grade = 'D'
else:
    grade = 'E'
print(f'{grade = }')
```
#### Example 3: Calculate the perimeter and area of a triangle.

Requirement: Enter the lengths of three sides. If they can form a triangle, calculate the perimeter and area; otherwise, display “Cannot form a triangle.”

```python
"""
Calculate the perimeter and area of a triangle

Version: 1.0
Author: ashewbytes
"""
a = float(input('a = '))
b = float(input('b = '))
c = float(input('c = '))
if a + b > c and a + c > b and b + c > a:
    perimeter = a + b + c
    print(f'Perimeter: {perimeter}')
    s = perimeter / 2
    area = (s * (s - a) * (s - b) * (s - c)) ** 0.5
    print(f'Area: {area}')
else:
    print('Cannot form a triangle')
```
> **Explanation:** The `if` condition above means that the sum of any two sides must be greater than the third side — this is the necessary condition for forming a triangle. When this condition is satisfied, we need to calculate and print the perimeter and area, so the five statements under `if` all have the same indentation and form one unit. As long as the `if` condition is true, all of them will be executed — this is what we previously referred to as a code block. In addition, the formula used above to calculate the area of a triangle is called Heron's formula. Suppose a triangle has side lengths $\small{a}$, $\small{b}$, and $\small{c}$; then the area $\small{A}$ can be obtained using the formula below, where $\small{s=\frac{a+b+c}{2}}$.
>
>$$
> A = \sqrt{s(s-a)(s-b)(s-c)}
> $$

### Summary

After learning branching structures and looping structures in Python, we can solve many real-world problems. This lesson should have helped you master how to construct branching structures. In the next lesson, we will introduce looping structures. After learning both lessons, you will definitely find that you can write a lot of interesting code. Keep going!
