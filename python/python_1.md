| [Introduction to Python and cmputer programming](python_1.md)  | [Data Types ](python_2.md)   |
|---|---|
## 
# Day 2
# Part1 -Basics-
## Introduction to Python and cmputer programming
A computer, even the most technically sophisticated, is devoid of even a trace of intelligence. You could say that it is like a well-trained dog - it responds only to a predetermined set of known commands.

The commands it recognizes are very simple. We can imagine that the computer responds to orders like "take that number, divide by another and save the result".

A complete set of known commands is called an **instruction list (IL)**. Different types of computers may vary depending on the size of their ILs, and the instructions could be completely different in different models.
###### A program written in a high-level programming language is called a source code.
## 
## Ways of transforming a program from a high-level programming language into machine language:
- **COMPILATION** : the source program is translated once; the program that performs this translation is called a compiler or translator.
- **INTERPRETATION** : you (or any user of the code) can translate the source program each time it has to be run; the program performing this kind of transformation is called an interpreter, you cannot just distribute the source code as-is, because the end-user also needs the interpreter to execute it.
##
## What does this all mean for you?
- Python is an interpreted language. This means that it inherits all the described advantages and disadvantages. Of course, it adds some of its unique features to both sets.
- If you want to program in Python, you'll need the Python interpreter. You won't be able to run your code without it. Fortunately, Python is free. This is one of its most important advantages.
##
## One of the amazing features of Python is the fact that it is actually one person's work (Guido van Rossum)!
##
## Why not Python?
Despite Python's growing popularity, there are still some niches where Python is absent, or is rarely seen:
- low-level programming (sometimes called "close to metal" programming): if you want to implement an extremely effective driver or graphical engine, you wouldn't use Python;
- applications for mobile devices: although this territory is still waiting to be conquered by Python, it will most likely happen someday.
##
### You should use Python 3,Python 3 is the newer (to be precise, the current) version of the language. It's going through its own evolution path, creating its own standards and habits.
##
## Python aka CPython
Guido van Rossum used the "C" programming language to implement the very first version of his language and this decision is still in force. All Pythons coming from the PSF are written in the "C" language. 
##
## Cython
Cython is one of a possible number of solutions to the most painful of Python's trait - the lack of efficiency. Large and complex mathematical calculations may be easily coded in Python (much easier than in "C" or any other traditional language), but the resulting code's execution may be extremely time-consuming.
Cython is intended to do - to automatically translate the Python code (clean and clear, but not too swift) into "C" code (complicated and talkative, but agile). *since C runs faster than python* 
##
## Other
- Jthon
- PyPy and RPython
##
## Get to work!
- Download Python 3 latest version.
- look at the checkbox named Add Python 3.x to PATH and check it.
- IDLE is an acronym: Integrated Development and Learning Environment.
- The first step is to create a new source file and fill it with code. Click File in the IDLE’s menu and choose New file.
![image](https://geek-university.com/wp-content/images/python/python_idle_new_file.jpg)
## 
As you can see, IDLE opens a new window for you. You can use it to write and amend your code.

- **This is the editor window.**
- **->write your cod then (RUN), The result should appear in the Shell**
![image](https://geek-university.com/wp-content/images/python/run_python_code_idle_shell.jpg)