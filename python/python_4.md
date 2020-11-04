| [Introduction to Python and computer programming](python_1.md)  | [Data Types](python_2.md)   | [Variables/input](python_3.md) | [Booleanvalues,conditions,loops,listsandlogic](python_4.md)
# Day 9
# Boolean values, conditions, loops,lists and logic

## Comparison: equality operator

Question: are two values equal?

To ask this question, you use the == (equal equal) operator.

Don't forget this important distinction:

`=` is an assignment operator, e.g., `a = b` assigns a with the value of b;
`==` is the question are these values equal?; `a == b` compares a and b.
> It is a binary operator with left-sided binding. It needs two arguments and checks if they are equal.

Now imagine a programmer who suffers from insomnia, and has to count black and white sheep separately as long as there are exactly twice as many black sheep as white ones.

The question will be as follows:
`black_sheep == 2 * white_sheep`
but Due to the low priority of the `==` operator:
`black_sheep == (2 * white_sheep)`
> note: i dont know why it works the same :/
## Inequality: the not equal to operator (!=)
...as the name indecates.
## Comparison operators: greater than
`black_sheep > white_sheep # greater than`
## Comparison operators: greater than or equal to , less than or equal to .
`>=` , `<=`
--- 
## Conditions and conditional execution

The first form of a conditional statement, which you can see below is written very informally but figuratively:
```python
if true_or_not:
    do_this_if_true
```
notice:
- the if keyword;
- one or more white spaces;
- an expression (a question or an answer) whose value will be interpreted solely in terms of True (when its value is non-zero) and False (when it is equal to zero);
- a colon followed by a newline;
- an indented instruction or set of instructions (at least one instruction is absolutely required); the indentation may be achieved in two ways - by inserting a particular number of spaces (the recommendation is to use four spaces of indentation), or by using the tab character; note: if there is more than one instruction in the indented part, the indentation should be the same in all lines; even though it may look the same if you use tabs mixed with spaces, it's important to make all indentations exactly the same - Python 3 **does not allow mixing spaces and tabs for indentation**.

In real life, we often express a desire:
if the weather is good, we'll go for a walk
then, we'll have lunch ->
```python
if the_weather_is_good:
    go_for_a_walk()
have_lunch()
```
```python
if sheep_counter >= 120:
    make_a_bed()
    take_a_shower()
    sleep_and_dream()
feed_the_sheepdogs()
```
Feeding the sheepdogs is always done.
## Conditional execution: the if-else statement
```python
if true_or_false_condition:
    perform_if_condition_true
else:
    perform_if_condition_false
```
## Nested if-else statements

Read what we have planned for this Sunday. If the weather is fine, we'll go for a walk. If we find a nice restaurant, we'll have lunch there. Otherwise, we'll eat a sandwich. If the weather is poor, we'll go to the theater. If there are no tickets, we'll go shopping in the nearest mall.
```python
if the_weather_is_good:
    if nice_restaurant_is_found:
        have_lunch()
    else:
        eat_a_sandwich()
else:
    if tickets_are_available:
        go_to_the_theater()
    else:
        go_shopping()
```
## The elif statement
it's a shorter form of else if.
Used to check more than just one condition, and to stop when the first statement which is true is found.

If the weather is fine, we'll go for a walk, otherwise if we get tickets, we'll go to the theater, otherwise if there are free tables at the restaurant, we'll go for lunch; if all else fails, we'll return home and play chess.
```python
if the_weather_is_good
    go_for_a_walk()
elif tickets_are_available:
    go_to_the_theater()
elif table_is_available:
    go_for_lunch()
else:
    play_chess_at_home()
```
im lazzyyyyy bbyyeeeeee :) continue tommorow :)
# Day 9
## Pseudocode and introduction to loops
```python
largest_number = -999999999
number = int(input())
if number == -1:
    print(largest_number)
    exit()
if number > largest_number:
    largest_number = number
go to line 02
```
Lines 02 through 08 make a loop. We'll pass through them as many times as needed to review all the entered values.

there are build in functions like max(), min() that makes life eazier !

# LAB
## Scenario
Spathiphyllum, more commonly known as a peace lily or white sail plant, is one of the most popular indoor houseplants that filters out harmful toxins from the air. Some of the toxins that it neutralizes include benzene, formaldehyde, and ammonia.

Imagine that your computer program loves these plants. Whenever it receives an input in the form of the word Spathiphyllum, it involuntarily shouts to the console the following string: "Spathiphyllum is the best plant ever!"


Write a program that utilizes the concept of conditional execution, takes a string as input, and:

prints the sentence "Yes - Spathiphyllum is the best plant ever!" to the screen if the inputted string is "Spathiphyllum" (upper-case)
prints "No, I want a big Spathiphyllum!" if the inputted string is "spathiphyllum" (lower-case)
prints "Spathiphyllum! Not [input]!" otherwise. Note: [input] is the string taken as input.
```python
string = input("what plant do you want ?")
if string == "Spathiphyllum":
 print("Yes - Spathiphyllum is the best plant ever!")
elif string == "spathiphyllum": 
 print("No, I want a big Spathiphyllum!")
else :
 print("Spathiphyllum! Not [input]!")
 ```
# LAB
## Scenario
Once upon a time there was a land - a land of milk and honey, inhabited by happy and prosperous people. The people paid taxes, of course - their happiness had limits. The most important tax, called the Personal Income Tax (PIT for short) had to be paid once a year, and was evaluated using the following rule:

if the citizen's income was not higher than 85,528 thalers, the tax was equal to 18% of the income minus 556 thalers and 2 cents (this was the so-called tax relief)
if the income was higher than this amount, the tax was equal to 14,839 thalers and 2 cents, plus 32% of the surplus over 85,528 thalers.
Your task is to write a tax calculator.

It should accept one floating-point value: the income.
Next, it should print the calculated tax, rounded to full thalers. There's a function named round() which will do the rounding for you - you'll find it in the skeleton code in the editor.
Note: this happy country never returns money to its citizens. If the calculated tax is less than zero, it only means no tax at all (the tax is equal to zero). Take this into consideration during your calculations.
```python
income = float(input("Enter the annual income: "))

if income <= 85528:
 tax = 18*income/100 - 556.2
else:
 tax = 14839.2 + 32*(income- 85528)/100

if tax >=0:
 tax = round(tax, 0)
else:
 tax = 0.0
print("The tax is:", tax, "thalers")
```
# LAB
## Scenario
As you surely know, due to some astronomical reasons, years may be leap or common. The former are 366 days long, while the latter are 365 days long.

Since the introduction of the Gregorian calendar (in 1582), the following rule is used to determine the kind of year:

if the year number isn't divisible by four, it's a common year;
otherwise, if the year number isn't divisible by 100, it's a leap year;
otherwise, if the year number isn't divisible by 400, it's a common year;
otherwise, it's a leap year.
Look at the code in the editor - it only reads a year number, and needs to be completed with the instructions implementing the test we've just described.

The code should output one of two possible messages, which are Leap year or Common year, depending on the value entered.

It would be good to verify if the entered year falls into the Gregorian era, and output a warning otherwise: Not within the Gregorian calendar period. Tip: use the != and % operators.
```python
year = int(input("Enter a year: "))

if year%4 != 0 :
 print ("common year")
elif year%100 != 0 :
 print ("leap year")
elif year%400 != 0 :
 print("common year")
else :
 print ("leap year")
```
## Looping your code with while
```python
while conditional_expression:
    instruction
```
when the condition is met, if performs its statements only once; while repeats the execution as long as the condition evaluates to True.
press Ctrl-C (or Ctrl-Break on some computers) to exit endless loop. 
```python
while True:
    print("I'm stuck inside a loop.")
```
## Looping your code with for
```python
for i in range(10):
    print("The value of i is currently", i)
```
The range() function may also accept three arguments
starting num/ finishing num and the increment.
# LAB
## Scenario
The idea behind it is that adding the word Mississippi to a number when counting seconds aloud makes them sound closer to clock-time, and therefore "one Mississippi, two Mississippi, three Mississippi" will take approximately an actual three seconds of time! It's often used by children playing hide-and-seek to make sure the seeker does an honest count.

Your task is very simple here: write a program that uses a for loop to "count mississippily" to five. Having counted to five, the program should print to the screen the final message "Ready or not, here I come!"

```python
import time

# Write a for loop that counts to five.
    # Body of the loop - print the loop iteration number and the word "Mississippi".
    # Body of the loop - use: time.sleep(1)
for i in range (5):
 print(i+1 ,  "Mississippi")
 time.sleep(1)
# Write a print function with the final message.
print ("Ready or not, here I come!")
```
## The break and continue statements
## Scenario
The break statement is used to exit/terminate a loop.

Design a program that uses a while loop and continuously asks the user to enter a word unless the user enters "chupacabra" as the secret exit word, in which case the message "You've successfully left the loop." should be printed to the screen, and the loop should terminate.

Don't print any of the words entered by the user. Use the concept of conditional execution and the break statement.
```python
word = input()
while word != "chupacabra":
 if word == "chupacabra":
  breake
 word = input()
 
print("You've successfully left the loop.")
```
## Scenario
The continue statement is used to skip the current block and move ahead to the next iteration, without executing the statements inside the loop.

It can be used with both the while and for loops.

Your task here is very special: you must design a vowel eater! Write a program that uses:

- a for loop;
- the concept of conditional execution (if-elif-else)
- the continue statement.
Your program must:

- ask the user to enter a word;
- use userWord = userWord.upper() to convert the word entered by the user to upper case; we'll talk about the so-called string methods and the upper() method very soon - don't worry;
- use conditional execution and the continue statement to "eat" the following vowels A, E, I, O, U from the inputted word;
- print the uneaten letters to the screen, each one of them on a separate line.
```python
# Prompt the user to enter a word
word = input("=")
# and assign it to the userWord variable.
userWord = word.upper()
for letter in userWord:
 if letter == "A":
  continue
 if letter == "E":
  continue
 if letter == "I":
  continue
 if letter == "O":
  continue
 if letter == "U":
  continue
 print (letter.lower())
 
```
## Scenario
Your task here is even more special than before: you must redesign the (ugly) vowel eater from the previous lab (3.1.2.10) and create a better, upgraded (pretty) vowel eater! Write a program that uses:

a for loop;
the concept of conditional execution (if-elif-else)
the continue statement.
Your program must:

ask the user to enter a word;
use userWord = userWord.upper() to convert the word entered by the user to upper case; we'll talk about the so-called string methods and the upper() method very soon - don't worry;
use conditional execution and the continue statement to "eat" the following vowels A, E, I, O, U from the inputted word;
assign the uneaten letters to the wordWithoutVovels variable and print the variable to the screen.
```python
wordWithoutVovels = ""

userWord = input("= ")
userWord = userWord.upper()

for letter in userWord:
 if letter == "A":
  continue
 if letter == "E":
  continue
 if letter == "I":
  continue
 if letter == "O":
  continue
 if letter == "U":
  continue
 wordWithoutVovels = wordWithoutVovels + letter

print(wordWithoutVovels)
```
## Scenario
Listen to this story: a boy and his father, a computer programmer, are playing with wooden blocks. They are building a pyramid.

Their pyramid is a bit weird, as it is actually a pyramid-shaped wall - it's flat. The pyramid is stacked according to one simple principle: each lower layer contains one block more than the layer above.

The figure illustrates the rule used by the builders:
  []
 [][]
[][][]

Your task is to write a program which reads the number of blocks the builders have, and outputs the height of the pyramid that can be built using these blocks.

Note: the height is measured by the number of fully completed layers - if the builders don't have a sufficient number of blocks and cannot complete the next layer, they finish their work immediately.
```python
blocks = int(input("Enter the number of blocks: "))

height = 0
numberOfBlocks = 0

while numberOfBlocks <= blocks:
 if numberOfBlocks >= blocks:
  break
 height = height + 1
 numberOfBlocks = height*(height+1)//2 
 if numberOfBlocks > blocks:
  height = height - 1
 print(height , numberOfBlocks)

 # 1-1 9-4
 # 2-2 10-4
 # 3-2
 # 4-3
 # 5-3
 # 6-3
 # 7-4
 # 8-4
 
print("The height of the pyramid:", height)
```
 > this one gave me headache ooof!