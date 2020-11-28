| [Introduction to Python and computer programming](python_1.md)  | [Data Types](python_2.md)   | [Variables/input](python_3.md) | [Booleanvalues,conditions,loops,listsandlogic](python_4.md) |[Lists](python_5.md)|[functions](python_6.md)|[tuple](python_7.md)|[modles](python_8.md)
# How to use a tuple?
Tuple is a un editable list. you can onely read it.
these will have the results ahead:

```python
myTuple = (1, 10, 100)

t1 = myTuple + (1000, 10000)
t2 = myTuple * 3

print(len(t2)) # 9
print(t1) # (1, 10, 100, 1000, 10000)
print(t2) # (1, 10, 100, 1, 10, 100, 1, 10, 100)
print(10 in myTuple) # True
print(-10 not in myTuple) # True
```
# a dictionary
**is a set of key-value pairs**.
- Note:
- each key must be unique - it's not possible to have more than one key of the same value;
- a key may be data of any type (except list): it may be a number (integer or float), or even a string;
- a dictionary is not a list - a list contains a set of numbered values, while a dictionary holds pairs of values;
- the len() function works for dictionaries, too - it returns the numbers of key-value elements in the dictionary;
- a dictionary is a one-way tool - if you have an English-French dictionary, you can look for French equivalents of English terms, but not vice versa.
```python
{'dog': 'chien', 'horse': 'cheval', 'cat': 'chat'}
{'Suzy': 5557654321, 'boss': 5551234567}
{}
```
**Can dictionaries be browsed using the for loop, like lists or tuples?**

**No and yes**.

No, because a dictionary is not a sequence type - the for loop is useless with it.

Yes, because there are simple and very effective tools that can adapt any dictionary to the for loop requirements (in other words, building an intermediate link between the dictionary and a temporary sequence entity).
```python
dictionary = {"cat" : "chat", "dog" : "chien", "horse" : "cheval"}

for key in dictionary.keys():
    print(key, "->", dictionary[key])
for key in sorted(dictionary.keys()):
    print(key, "->", dictionary[key]) # same but sorted
```
Another way is based on using a dictionary's method named items(). The method returns tuples (this is the first example where tuples are something more than just an example of themselves) where each tuple is a key-value pair.

This is how it works:
```python
dictionary = {"cat" : "chat", "dog" : "chien", "horse" : "cheval"}

for english, french in dictionary.items():
    print(english, "->", french)
```
values method:
```python
dictionary = {"cat" : "chat", "dog" : "chien", "horse" : "cheval"}

for french in dictionary.values():
    print(french)
```
You can also insert an item to a dictionary by using the update() method, e.g.:
or deleat. To remove the last item in a dictionary, you can use the popitem() method.
```python
dictionary = {"cat" : "chat", "dog" : "chien", "horse" : "cheval"}

dictionary.update({"duck" : "canard"})
del dictionary['dog'] 

```
this code will calculate the average of students grades :
```python
school_class = {}

while True:
    name = input("Enter the student's name (or type exit to stop): ")
    if name == 'exit':
        break
    
    score = int(input("Enter the student's score (0-10): "))
    
    if name in school_class:
        school_class[name] += (score,)
    else:
        school_class[name] = (score,)
        
for name in sorted(school_class.keys()):
    adding = 0
    counter = 0
    for score in school_class[name]:
        adding += score
        counter += 1
    print(name, ":", adding / counter)

```
