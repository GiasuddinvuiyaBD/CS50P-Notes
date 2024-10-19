## 📝 Notes

| **Lecture** | **Topics Covered**               |         **Language**      |
|-------------|----------------------------------|---------------------------|
| `0`         | Functions, Variables             | Python                    |

--- 
## Lecture 0 📚

- [Creating Code with Python](#creating-code-with-python)
- [Functions](#functions)
- [Bugs](#bugs)
- [Improving Your First Python Program](#improving-your-first-python-program)


--- 
## Creating Code with Python 
✨


To write and run Python programs, you’ll need a code editor, which is sometimes referred to as an IDE (Integrated Development Environment). In this course, we’ll be using **Visual Studio Code (VS Code)**, a popular and easy-to-use editor.

Before starting, make sure you have VS Code installed on your computer. Alternatively, you can use CS50's **Live VS Code Editor** for online coding.

In the editor:
- **Text editor** is where you write your code (at the top).
- **Terminal** is where you can execute commands (at the bottom).

---

### 📂 Creating a Python File

To create a new Python file, type the following command in the terminal:

```bash
code hello.py
```

Here's what the command does:

- `code`: is the command that opens a file in VS Code.

- `hello`: is the name of the file.

- `.py`: is the file extension used for Python files.

Running this command will open a new Python file named `hello.py`, where you can start writing code.

---

### ✏️ Writing Your First Python Program
Now, in the text editor, write the following code:

```py
    print("hello, world")
```

Explanation: 
- `print`:  A built-in Python function that displays text on the screen.

- `"hello, world"`: This is the message that will be displayed when the program runs.

---

### 🚀 Running Your Python Program
In the terminal, type the following command and hit Enter:

```bash
    python hello.py
```
This command runs your hello.py file. To run any Python program, use the format:

```bash
python file_name.py
```

---

### 🧠 How It Works


Computers understand only binary (zeros and ones). When you run `python hello.py`, Python interprets your code and converts it into binary so the computer can execute it.


The result of running this command is:
```py
hello, world
```

The results of running the `python.py` program is `hello, world`. 

🎉 **Congrats!** You’ve just written and run your first Python program!

--- 

## Functions 
🛠️

Functions are like actions (or verbs) that a computer or programming language already knows how to perform. 

They allow you to tell the computer what to do in a clear and efficient way.


For example, in your `hello.py` program, the `print()` function is designed to display text or output directly in the terminal window.

---

## Bugs
🐞
Bugs are a normal part of coding—mistakes you'll need to fix. Don’t get discouraged! 💪 Solving these issues is key to becoming a great programmer. 

For example, in our `hello.py` program, if I accidentally type `print("hello, world"` (missing the closing parenthesis), the compiler will show an error in the terminal. ⚠️

Error messages often indicate what went wrong and give hints for fixing it. However, sometimes the compiler may not provide helpful feedback. 🤔

--- 

## Improving Your First Python Program

Now, we're going to write our first Python program. We'll include another function called `input`, which allows us to prompt the user for input

```py
    input("What's your name ? ")
    print("hell, world")
```

This program currently does not display the user's input. To do that, we need to introduce variables. Variables will help us store and use the input provided by the user.

### Variables 🧮

In programming, a variable is like a container that stores values or data, allowing you to reuse or manipulate them later. 📦

For Example: 
```py
    name = input("What's your name ? ")
    print("hello, world")
```

Notice the `=` sign in `name = input("What's your name?")`. This is called the assignment operator.

➡️

- The assignment operator assigns the value on the right side to the variable on the left.

- Here, `name` is a variable that will store the user's input from the `input` function.

In simple terms, the `=` sign tells Python to store whatever is on the right into the variable on the left.


Here is Another Example: 
```py
    name = input("What's your name ?")
    print("My Name is : ", name)
```

The result in the terminal window would be
```bash
    What's your name ? Gias uddin vuiya
    My Name is : Gias uddin vuiya
```


🎉 We’re getting closer to the result we want!

For more details, you can check Python’s documentation on [data types](https://docs.python.org/3/library/datatypes.html). 📖


## Comments
Comments are a way for programmers to track what they are doing in their programs and even inform others about their intentions for a block of code

Code Example: 
```py
    # Ask user for their name
    name = input("What's your name? ")
    print(name)

    # or we can organize it
    print("My name is : ", name)
    print("My name is : {name}")
```

## Pseudocode

Pseudocode is a simple way to outline your program's logic using plain language. It helps you break down complex tasks into smaller, manageable steps, especially when you're unsure how to implement the code yet. Think of it as a to-do list for your code.

Example of Pseudocode:
```plaintext
    1. Start the program
    2. Ask the user for their name
    3. Store the user's name in a variable
    4. Print a welcome message with the user's name
    5. End the program
```

Once you understand the logic from the pseudocode, you can translate it into actual code. For instance, this pseudocode can be implemented in Python like this:

```py
# Step 1: Start the program
# Step 2: Ask the user for their name
name = input("What's your name? ")

# Step 3: Store the user's name in a variable (done above)
# Step 4: Print a welcome message with the user's name
print(f"Welcome, {name}!")

# Step 5: End the program
```

Pseudocode helps you organize your thoughts and makes coding easier!

## Strings and Paremeters

A string, known as a str in Python, is a sequence of text.

Let’s go back to our previous code. You might have noticed a visual side effect where the output appears on multiple lines.

```py
    # Ask the user for their name
    name = input("What's your name? ")
    print("hello,")
    print(name)
```
Functions accept arguments that control how they behave. By checking the documentation for [print](https://docs.python.org/3/library/functions.html#print), you can learn about the different arguments it can take and how they affect its output. 

From the documentation, you'll see that the print() function automatically includes the argument `end='\n'`. This`\n` signifies that the function will create a line break after each call by default. Essentially, the end argument's default value is set to insert a new line

Example: 
```py
    # Ask the user for their name
    name = input("What's your name? ")
    print("hello,", end="")
    print(name)
```
By setting `end=""`, we override the default value of `end`, preventing a new line from being created after the first print statement. For example, if we provide the name `'David'`, the output in the terminal will be `hello, David`.


You can learn more in Python’s documentation on [print](https://docs.python.org/3/library/functions.html#print).


--- 

## A small problem with quotation marks
Notice how adding quotation marks as part of your string is challenging.

`print("hello,"friend"")` will not work, and the compiler will throw an error.

Generally, there are two approaches to fixing this.

1. First, you could simply change the quotes to single quotation marks.
2. Another, more commonly used approach would be code as `print("hello, \"friend\"")`.

The backslashes tell the compiler that the following character should be considered a quotation mark in the string and avoid a compiler error.

--- 

## Formatting Strings

The most elegant way to work with strings is as follows:

```py
    # Ask the user for their name
    name = input("What's your name? ")
    print(f"hello, {name}")
```

Notice the `f` in `print(f"hello, {name}")`.

 This `f` is a special indicator for Python to treat this string a special way, different than previous approaches we have illustrated in this lecture. 

--- 

## More on Strings
Here we are going to discuss some string methods.

**strip()**
By utilizing the method strip on name as name = name.strip(), will strip all the whitespaces on the left and right of the users input.

Example: 
```py
    # Ask the user for their name
    name = input("What's your name? ")

    # Remove whitespace from the str
    name = name.strip()

    # Print the output
    print(f"hello, {name}")
```
Running this program will remove all leading and trailing spaces from the name.

**title**

Using the title method, it would title case the user’s name. 

```py
    # Ask the user for their name
    name = input("What's your name? ")

    # Remove whitespace from the str
    name = name.strip()

    # Capitalize the first letter of each word
    name = name.title()

    # Print the output
    print(f"hello, {name}")
``` 

**Notice that you can modify your code to be more efficient:**

```py
    # Ask the user for their name
    name = input("What's your name? ")

    # Remove whitespace from the str and capitalize the first letter of each word
    name = name.strip().title()

    # Print the output
    print(f"hello, {name}")
```

**We could even go further!**
```py
    # Ask the user for their name, remove whitespace from the str and capitalize the first letter of each word
    name = input("What's your name? ").strip().title()

    # Print the output
    print(f"hello, {name}")
```

You can learn more about strings in Python’s documentation on [str](https://docs.python.org/3/library/stdtypes.html#str)


## Integers or int

In Python, an integer is referred to as an `int`.

In mathematics, we commonly use the operators +, -, *, /, and %. The last operator, %, known as the modulo operator, might be less familiar to you.

**Tricks:**
You don’t have to use the text editor window in your compiler to run Python code. Down in your terminal, you can run `python` alone. 


You will be presented with >>> in the terminal window. You can then run live, interactive code. You could type 1+1, and it will run that calculation. 

**Now, we will create a calculator using Python.**

Opening up VS Code again, we can type code `calculator.py`

First, we can declare a few variables.
```py
x = 1
y = 2

z = x + y

print(z)
```
Naturally, when we run python `calculator.py` we get the result in the terminal window of `3`. 

We can make this more interactive using the input function.

```py
x = input("What's x? ")
y = input("What's y? ")

z = x + y

print(z)
```

Earlier, we saw that the `+` sign concatenates strings. Since input from the keyboard is treated as text, we need to convert it from a string to an integer for calculations. Here's how:

```py
x = input("What's x? ")
y = input("What's y? ")

z = int(x) + int(y)

print(z)
```

We can further improve our program as follows:
```py
x = int(input("What's x? "))
y = int(input("What's y? "))

print(x + y)
```

You can learn more in Python’s documtenation of [int](https://docs.python.org/3/library/functions.html#int).

--- 

## Readability Wins

When deciding on your approach to a coding task, keep in mind that there are often multiple valid ways to solve the same problem.

Regardless of what approach you take to a programming task, remember that your code must be readable.

You should use comments to give yourself and others clues about what your code is doing. Further, you should create code in a way that is readable.

--- 

## Float Basics

A floating-point value is a real number that includes a decimal point, such as 0.52

Example of a floating-point number:
```py
x = float(input("What's x? "))
y = float(input("What's y? "))

print(x + y)
```
It allows users to input values like 90.32, 3.0, and 9.0.


If you want to round the total to the nearest integer, you can use the `round` function from Python. The syntax is `round(number[, ndigits])`, where the square brackets indicate optional arguments. You can simply use `round(n)`to round to the nearest integer, or you can specify additional parameters as needed.

**Could code as follows:**
```py
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Create a rounded result
z = round(x + y)

# Print the result
print(z)
```
The output will be rounded to the nearest integer.


What if we wanted to format the output of long numbers? For example, rather than seeing 1000, you may wish to see 1,000. You could modify your code as follows:

```py
# Get the users input
x = float(input("What's x?"))
y = float(input("What's y?"))

z = round(x + y)
print(f"{z:,}")
```

## More on Floats
How can we round floating point values? First, modify your code as follows:

```py
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Calculate the result
z = x / y

# Print the result
print(z)
```
When inputting 2 as x and 3 as y, the result z is 0.6666666666, seemingly going on to infinite as we might expect.


Let’s imagine that we want to round this down. We could modify our code as follows:
```py
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Calculate the result and round
z = round(x / y, 2)

# Print the result
print(z)
```
As we might expect, this will round the result to the nearest two decimal points.



We could also use `fstring` to format the output as follows:

```py
# Get the user's input
x = float(input("What's x? "))
y = float(input("What's y? "))

# Calculate the result
z = x / y

# Print the result
print(f"{z:.2f}")
```
This cryptic fstring code displays the same as our prior rounding strategy.


You can learn more in Python’s documentation of [float](https://docs.python.org/3/library/functions.html#float).

## Def

In Python, the `def` keyword is used to declare a function. It defines a reusable block of code that performs a specific task. The general syntax for defining a function is:

```py
def function_name(parameters):
    # code block
    return value  # optional
```

Now we can create our own function called hello as follows:
```py
def hello():
    print("hello")


name = input("What's your name? ")
hello()
print(name)
```

Explanation of the code:
```py
def hello():
    print("hello")
```
- This defines a function named `hello` that, when called, prints "hello" to the console.

```py
name = input("What's your name? ")
```

- This line prompts the user to enter their name and stores the `input` in the variable `name`.

```py
hello()
```
- This calls the `hello` function, which prints "hello".

```py
print(name)
```
- Finally, this line prints the user's name to the console.


**We can further improve our code:**
```py
# Create our own function
def hello(to):
    print("hello,", to)


# Output using our own function
name = input("What's your name? ")
hello(name)
```
Here, in the first lines, you are creating your `hello` function. This time, however, you are telling the compiler that this function takes a single parameter: a variable called `to`. Therefore, when you call `hello(name)` the computer passes name into the hello function as `to`. This is how we pass values into functions.  


**We can change our code to add a default value to hello:**
```py
# Create our own function
def hello(to="world"):
    print("hello,", to)


# Output using our own function
name = input("What's your name? ")
hello(name)

# Output without passing the expected arguments
hello()
```

## main function
In Python, the main function serves as the entry point for a program. It’s a common convention to define a main function to encapsulate the primary logic of the script. By organizing code in a main function, you make your program more structured and easier to understand.

Example: 
```py
def main():

    # Output using our own function
    name = input("What's your name? ")
    hello(name)

    # Output without passing the expected arguments
    hello()


# Create our own function
def hello(to="world"):
    print("hello,", to)


main()
```

## Returning Values
You can imagine many scenarios where you don’t just want a function to perform an action but also to `return` a value back to the main function. For example, rather than simply printing the calculation of `x + y`, you may want a function to `return` the value of this `calculation` back to another part of your program. This `“passing back”` of a value we call a `return` value.

Example of return value
```py
def main():
    x = int(input("What's x? "))
    print("x squared is", square(x))


def square(n):
    return n * n


main()
```
Effectively, x is passed to square. Then, the calculation of x * x is returned back to the main function.
