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