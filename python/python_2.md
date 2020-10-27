| [Introduction to Python and cmputer programming](python_1.md)  | [Data Types](python_2.md)   | [Variables/input](python_3.md) |

 
# Day 2
# Data Types 
## The print() function
launch IDLE, create a new Python source file, fill it with this code, name the file and save it. Now run it. If everything goes okay, you'll see the rhyme's line in the IDLE console window.
```python
print("Hello, World!")
```
shows -> `Hello, World!`

## A function is a separate part of the computer code able to:
- cause some effect (e.g., send text to the terminal, create a file, draw an image, play a sound, etc.); this is something completely unheard of in the world of mathematics.
- evaluate a value or some values (e.g., the square root of a value or the length of a given text); this is what makes Python's functions the relatives of mathematical concepts.

## Where do the functions come from?

- They may come from Python itself;(*it is built-in*); you don't have to do anything special.
- if you want to make use of it;
they may come from one or more of Python's add-ons named *modules*; some of the modules come with Python, others may require separate installation.
- you can write them yourself, placing as many functions as you want and need inside your program to make it simpler, clearer and more elegant.

## Function components
- an effect.
- a result.
- The argument(s).
- Python functions strongly demand the presence of a pair of parentheses - opening and closing ones, respectively.

## String
**string is delimited with quotes**
Almost anything you put inside the quotes will be taken literally, not as code, but as *data*.

## What happens when Python encounters an invocation ?
- First, Python checks if the name specified is legal (it browses its internal data in order to find an existing function of the name; if this search fails, Python aborts the code);
- second, Python checks if the function's requirements for the number of arguments allows you to invoke the function in this way (e.g., if a specific function demands exactly two arguments, any invocation delivering only one argument will be considered erroneous, and will abort the code's execution);
- third, Python leaves your code for a moment and jumps into the function you want to invoke; of course, it takes your argument(s) too and passes it/them to the function;
- fourth, the function executes its code, causes the desired effect (if any), evaluates the desired result(s) (if any) and finishes its task;
- finally, Python returns to your code (to the place just after the invocation) and resumes its execution.

# **LAB**
## Estimated time
5 minutes

## Level of difficulty
Very easy

## Objectives
becoming familiar with the print() function and its formatting capabilities;
experimenting with Python code.
Scenario
The print() command, which is one of the easiest directives in Python, simply prints out a line to the screen.

## In your first lab:

- use the print() function to print the line Hello, Python! to the screen. Use double quotes around the string;
having done that, use the print() function again, but this time print your first name;
- remove the double quotes and run your code. Watch Python's reaction. What kind of error is thrown?
```c
File "main.py", line 1
    print(HEllo,python!)
                      ^
SyntaxError: invalid syntax
```
- then, remove the parentheses, put back the double quotes, and run your code again. What kind of error is thrown this time?
```c
 File "main.py", line 1
    print"HEllo,python!"
                       ^
SyntaxError: invalid syntax
```
- experiment as much as you can. Change double quotes to single quotes, use multiple print() functions on the same line, and then on different lines. See what happens.
- single and double works.
- space after the function name is ok. 
- ( ; and , ) at the end are ok.

-------------------

## What arguments does print() expect?

Any. We'll show you soon that print() is able to operate with virtually all types of data offered by Python. Strings, numbers, characters, logical values, objects - any of these may be successfully passed to print().


## What value does the print() function evaluate?

None. Its effect is enough - print() does not evaluate anything.

## Python's syntax is quite specific in this area. Unlike most programming languages, Python requires that there cannot be more than one instruction in a line.
- Python's syntax is quite specific in this area. Unlike most programming languages, Python requires that there cannot be more than one instruction in a line.
- The empty print() invocation is not as empty as you may have expected - it does output an empty line, or (this interpretation is also correct) its output is just a newline.

## The escape and newline characters
`\n` : new line
```python
print("The itsy bitsy spider\nclimbed up the waterspout.")

```
If you want to put just one backslash inside a string, don't forget its escaping nature - you have to double it, e.g., such an invocation will cause an error:
`print("\")`
this wont:
`print("\\")`

##  Using multiple arguments
```python
print("The itsy bitsy spider" , "climbed up" , "the waterspout.")
```
- outputs them all on one line.
-  puts a space between the outputted arguments.

## The keyword arguments
- a keyword argument consists of three elements: a keyword identifying the argument (end here); an equal sign (=); and a value assigned to that argument;
- any keyword arguments have to be put after the last positional argument (this is very important)
```Python
print("My name is", "Python.", end=" ")
print("Monty Python.")
``` 
Results ->
 ```
My name is Python. Monty Python.
```

```Python
print("My name is", "Python.", end="\n")
print("Monty Python.")
``` 
Results -> 
```
My name is Python.
Monty Python.
```
```python
print("My", "name", "is", "Monty", "Python.", sep="-")
```
Results->
```
My-name-is-Monty-Python.
```
# **LAB**
## Estimated time
5 minutes

## Level of difficulty
Very Easy

## Objectives
becoming familiar with the print() function and its formatting capabilities;
experimenting with Python code.
## Scenario
Modify the first line of code in the editor, using the sep and end keywords, to match the expected output. Use the two print() functions in the editor.

Don't change anything in the second print() invocation.
## Expected output
`Programming***Essentials***in...Python`


```python
print("Programming","Essentials","in")
print("Python")
```
```python
print("Programming","Essentials","in", sep = "***", end = "...")
print("Python")
```

# **LAB**
## Estimated time
5-10 minutes

## Level of difficulty
Easy

## Objectives
experimenting with existing Python code;
discovering and fixing basic syntax errors;
becoming familiar with the print() function and its formatting capabilities.
## Scenario
We strongly encourage you to play with the code we've written for you, and make some (maybe even destructive) amendments. Feel free to modify any part of the code, but there is one condition - learn from your mistakes and draw your own conclusions.

## Try to:

- minimize the number of print() function invocations by inserting the \n sequence into the strings
- make the arrow twice as large (but keep the proportions)
- duplicate the arrow, placing both arrows side by side; note: a string may be multiplied by using the following trick: "string" * 2 will produce "stringstring" (we'll tell you more about it soon)
- remove any of the quotes, and look carefully at Python's response; pay attention to where Python sees an error - is this the place where the error really exists?
- do the same with some of the parentheses;
- change any of the print words into something else, differing only in case (e.g., Print) - what happens now?
- replace some of the quotes with apostrophes; watch what happens carefully.
```python
print("    *")
print("   * *")
print("  *   *")
print(" *     *")
print("***   ***")
print("  *   *")
print("  *   *")
print("  *****")
```
```
print("    *    " *2, "   * *   " *2,"  *   *  " *2," *     * " *2,"***   ***" *2,"  *   *  " *2,"  *   *  " *2,"  *****  " *2,sep = "\n")
```
## Literals - the data in itself
### Integers
when you use 
`print(2)`: The number is converted into machine representation (a set of bits). The print() function is able to show them both in a form readable to humans.
#### the numbers handled by modern computers are of two types:
- integers, that is, those which are devoid of the fractional part;
- and floating-point numbers (or simply floats), that contain (or are able to contain) the fractional part.
- In python, you can write a number either like this: 11111111, or like that: 11_111_111.
#### Octal and hexadecimal numbers
- If an integer number is preceded by an 0O or 0o prefix (zero-o), it will be treated as an octal value. This means that the number must contain digits taken from the [0..7] range only.

0o123 is an octal number with a (decimal) value equal to 83.
- The second convention allows us to use hexadecimal numbers. Such numbers should be preceded by the prefix 0x or 0X (zero-x).

0x123 is a hexadecimal number with a (decimal) value equal to 291. 
#### Floats
have a non-empty decimal fraction.
` 2.5`
`-0.4`
### String
Let's assume that we want to print a very simple message saying:
`I like "Monty Python"`
Use escape chareacters
`print("I like \"Monty Python\"")`
`print('I like "Monty Python"')`
#### Boolean
True/False 
<br/>
in numeric contexts:
<br/>
- True is equal to 1 
- False is zaro
<br/>
so...
<br/>
- print(True > False) --> True
- print(True < False) --> False

## Python as a calculator
- `+, -` : add subtract.
- `*, **` : multiply, power.
- `/, //` : devide with dec (always), without dec (rounded).
- `%` : does it dev? a remainder left after the integer division.
when the numbers are int the result will be in int too.



