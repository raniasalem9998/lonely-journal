| [Introduction to Python and cmputer programming](python_1.md)  | [Data Types](python_2.md)   | [Variables/input](python_3.md) |

# Day 4
# Variables
## How to store the result?
## Names of **variables** should:
- The name of the variable must be composed of upper-case or lower-case letters, digits, and the character `_`.
- The name of the variable must begin with a letter.
- Upper- and lower-case letters are treated as different (a little differently than in the real world - Alice and ALICE are the same first names, but in Python they are two different variable names.
- the name of the variable must not be any of Python's reserved words.
## Notes:
- A variable comes into existence as a result of assigning a value to it. Unlike in other languages, you don't need to declare it in any special way.
- If you assign any value to a nonexistent variable, the variable will be automatically created. You don't need to do anything else.
```python
var = 1
account_balance = 1000.0
client_name = 'John Doe'
```
## Assigning a new value to an already existing variable.
```python
var = 1
print(var)
var = var + 1
print(var)
```
->
```c
1
2
```
# LAB
## Estimated time
10 minutes

## Level of difficulty
Easy

## Objectives
becoming familiar with the concept of storing and working with different data types in Python;
experimenting with Python code.
## Scenario
Here is a short story:

Once upon a time in Appleland, John had three apples, Mary had five apples, and Adam had six apples. They were all very happy and lived for a long time. End of story.

## Your task is to:

- create the variables: john, mary, and adam;
- assign values to the variables. The values must be equal to the numbers of fruit possessed by John, Mary, and Adam respectively;
- having stored the numbers in the variables, print the variables on one line, and separate each of them with a comma;
- now create a new variable named totalApples equal to addition of the three former variables.
- print the value stored in totalApples to the console;
- experiment with your code: create new variables, assign different values to them, and perform various arithmetic operations on them (e.g., +, -, *, /, //, etc.). Try to print a string and an integer together on one line, e.g., "Total number of apples:" and totalApples.
```python
John = 5
mary = 4
adam = 3
print (John , mary , adam)
totalApples = John + mary + adam
print (totalApples)
```
## Shortcut operators 
- `x = x * 2` to `x *= 2`
- `sheep = sheep + 1` to `sheep += 1`
- `i = i + 2 * j` to `i += 2 * j`
- `rem = rem % 10` to `rem %= 10` 
you get it ..
# LAB
## Estimated time
10 minutes

## Level of difficulty
Easy

## Objectives
becoming familiar with the concept of, and working with, variables;
performing basic computations and conversions;
experimenting with Python code.
## Scenario
Miles and kilometers are units of length or distance.

Bearing in mind that 1 mile is equal to approximately 1.61 kilometers, complete the program in the editor so that it converts:

miles to kilometers;
kilometers to miles.
Do not change anything in the existing code. Write your code in the places indicated by ###. Test your program with the data we've provided in the source code.


Pay particular attention to what is going on inside the print() function. Analyze how we provide multiple arguments to the function, and how we output the expected data.

Note that some of the arguments inside the print() function are strings (e.g., "miles is", whereas some other are variables (e.g., miles).

## TIP

There's one more interesting thing happening there. Can you see another function inside the print() function? It's the round() function. Its job is to round the outputted result to the number of decimal places specified in the parentheses, and return a float (inside the round() function you can find the variable name, a comma, and the number of decimal places we're aiming for). We're going to talk about functions very soon, so don't worry that everything may not be fully clear yet. We just want to spark your curiosity.


After completing the lab, open Sandbox, and experiment more. Try to write different converters, e.g., a USD to EUR converter, a temperature converter, etc. - let your imagination fly! Try to output the results by combining strings and variables. Try to use and experiment with the round() function to round your results to one, two, or three decimal places. Check out what happens if you don't provide any number of digits. Remember to test your programs.

Experiment, draw conclusions, and learn. Be curious.
```python
kilometers = 12.25
miles = 7.38

miles_to_kilometers = ###
kilometers_to_miles = ###

print(miles, "miles is", round(miles_to_kilometers, 2), "kilometers")
print(kilometers, "kilometers is", round(kilometers_to_miles, 2), "miles")
```
```python
miles_to_kilometers = miles * 1.61
kilometers_to_miles = kilometers / 1.61
```
# LAB 
## Estimated time
10-15 minutes

## Level of difficulty
Easy

## Objectives
becoming familiar with the concept of numbers, operators, and arithmetic operations in Python;
performing basic calculations.
## Scenario
Take a look at the code in the editor: it reads a float value, puts it into a variable named x, and prints the value of a variable named y. Your task is to complete the code in order to evaluate the following expression:

`3x3 - 2x2 + 3x - 1`

The result should be assigned to y.

Remember that classical algebraic notation likes to omit the multiplication operator - you need to use it explicitly. Note how we change data type to make sure that x is of type float.

Keep your code clean and readable, and test it using the data we've provided, each time assigning it to the x variable (by hardcoding it). Don't be discouraged by any initial failures. Be persistent and inquisitive.

```python
x =  # hardcode your test data here
x = float(x)
# write your code here
print("y =", y)
```
```python
x =  -1
x = float(x)
y = 3*(x**3) - 2*(x**2) + 3*x -1
print("y =", y)
```
> the ( ) are just in case :) ..

## Leaving A comment 
```python
# This program evaluates the hypotenuse c.
# a and b are the lengths of the legs.
a = 3.0
b = 4.0
c = (a ** 2 + b ** 2) ** 0.5  # We use ** instead of square root.
print("c =", c)
# This is
a multiline
comment. #

print("Hello!")
```
> Good, responsible developers describe each important piece of code.

# Day 6

# The input() function
The input() function is able to read data entered by the user and to return the same data to the running program.
```python
print("Tell me anything...")
anything = input()
print("Hmm...", anything, "... Really?")
```
- The program prompts the user to input some data from the console (most likely using a keyboard, although it is also possible to input data using voice or image);
- note: you need to assign the result to a variable; this is crucial - missing out this step will cause the entered data to be lost;
- the argument can be a message 
```python
anything = input("Tell me anything...")
print("Hmm...", anything, "...Really?")
```
- **the result of the input() function is a string.**
```python
TypeError: unsupported operand type(s) for ** or pow(): 'str' and 'float'
```
- To specify te type of input :
 - int(): takes one argument and convert it to int.
 - float(): convert the arg to float.

## Concatenation
`string + string` : It simply concatenates (glues) two strings into one.
## Replication
The * (asterisk) sign, when applied to a string and number (or a number and string, as it remains commutative in this position) becomes a replication operator
`string * number`
`number * string`
`"James" * 3` gives `"JamesJamesJames"`
## Type conversion str()
convert a number into a string.

# LAB
## Estimated time
5-10 minutes

## Level of difficulty
Easy

## Objectives
becoming familiar with the inputting and outputting of data in Python;
evaluating simple expressions.
## Scenario
Your task is to complete the code in order to evaluate the results of four basic arithmetic operations.

The results have to be printed to the console.

You may not be able to protect the code from a user who wants to divide by zero. That's okay, don't worry about it for now.

Test your code - does it produce the results you expect?

We won't show you any test data - that would be too simple.
```python
# input a float value for variable a here
# input a float value for variable b here

# output the result of addition here
# output the result of subtraction here
# output the result of multiplication here
# output the result of division here

print("\nThat's all, folks!")
```
```python
# input a float value for variable a here
a = int(input('inter a = '))
# input a float value for variable b here
b = int(input('inter b = '))
# output the result of addition here
print ('add = ' + str(a + b))
# output the result of subtraction here
print('sub = ' + str(a - b))
# output the result of multiplication here
print('multi = ' + str(a*b))
# output the result of division here
print('div = ' + str(a/b))
print("\nThat's all, folks!")
```
# LAB
## Estimated time
20 minutes

## Level of difficulty
Intermediate

## Objectives
becoming familiar with the concept of numbers, operators and arithmetic operations in Python;
understanding the precedence and associativity of Python operators, as well as the proper use of parentheses.
## Scenario
Your task is to complete the code in order to evaluate the following expression:


```python
x = float(input("Enter value for x: "))

# put your code here
y = 1/(x +( 1 /( x + 1 /( x + 1 / x) ) ) )
print("y =", y)
```
# LAB 
## Estimated time
15-20 minutes

## Level of difficulty
Easy

## Objectives
improving the ability to use numbers, operators, and arithmetic operations in Python;
using the print() function's formatting capabilities;
learning to express everyday-life phenomena in terms of programming language.
## Scenario
Your task is to prepare a simple code able to evaluate the end time of a period of time, given as a number of minutes (it could be arbitrarily large). The start time is given as a pair of hours (0..23) and minutes (0..59). The result has to be printed to the console.

For example, if an event starts at 12:17 and lasts 59 minutes, it will end at 13:16.
```python
hour = int(input("Starting time (hours): "))
mins = int(input("Starting time (minutes): "))
dura = int(input("Event duration (minutes): "))

# put your code here
```
```python
hour = int(input("Starting time (hours): "))
mins = int(input("Starting time (minutes): "))
dura = int(input("Event duration (minutes): "))

# put your code here
add_mins = ( (mins+dura) % 60 )
add_hours = (int((mins+dura) / 60))
print ('time = ' + str(hour+add_hours)+ ':' + str(mins + add_mins))
```

Don't worry about any imperfections in your code - it's okay if it accepts an invalid time - the most important thing is that the code produce valid results for valid input data.

