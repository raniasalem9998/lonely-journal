# Day 12

## List

 > from today will write the Labs onely to save time

 ```python
 # step 1
beatles = []
print("Step 1:", beatles)

# step 2
beatles.append('John Lennon')
beatles.append('Paul McCartney')
beatles.append('George Harrison')
print("Step 2:", beatles)

# step 3
members = ['Stu Sutcliffe','Pete Best']
for i in members:
    beatles.append(i)
print("Step 3:", beatles)

# # step 4
for i in beatles:
    for j in members:
        if i == j:
            del beatles[beatles.index(i)]
print("Step 4:", beatles)

# step 5
beatles.insert(0,'Ringo Starr')
print("Step 5:", beatles)


# testing list legth
print("The Fab", len(beatles))
```

Write a program that reflects these changes and lets you practice with the concept of lists. Your task is to:

- step 1: create an empty list named beatles;
- step 2: use the append() method to add the following members of the band to the list: John Lennon, Paul McCartney, and George Harrison;
- step 3: use the for loop and the append() method to prompt the user to add the following members of the band to the list: Stu Sutcliffe, and Pete Best;
- step 4: use the del instruction to remove Stu Sutcliffe and Pete Best from the list;
- step 5: use the insert() method to add Ringo Starr to the beginning of the list;

## Sorting Lists

```python
myList = [8, 10, 6, 2, 4] # list to sort
swapped = True # it's a little fake - we need it to enter the while loop

while swapped:
    swapped = False # no swaps so far
    for i in range(len(myList) - 1):
        if myList[i] > myList[i + 1]:
            swapped = True # swap occured!
            myList[i], myList[i + 1] = myList[i + 1], myList[i]

print(myList)
```

How many passes do we need to sort the entire list?

We solve this issue in the following way: we introduce another variable; its task is to observe if any swap has been done during the pass or not; if there is no swap, then the list is already sorted, and nothing more has to be done. We create a variable named swapped, and we assign a value of False to it, to indicate that there are no swaps. Otherwise, it will be assigned True.

myList = [8, 10, 6, 2, 4] # list to sort;

### Others ways

```python
myList = [8, 10, 6, 2, 4]
myList.sort()
print(myList)
```

## The inner life of a List

The assignment: list2 = list1 copies the name of the array, not its contents. In effect, the two names (list1 and list2) identify the same location in the computer memory. Modifying one of them affects the other, and vice versa;

```python
list1 = [1]
list2 = list1
list1[0] = 2
print(list2)
# will give [2]
```

## Powerful slices

A slice is an element of Python syntax **that allows you to make a brand new copy of a list, or parts of a list**.
`start` is the index of the first element included in the slice;
`end is` the index of the first element not included in the slice.

```python
# Copying the whole list
list1 = [1]
list2 = list1[:]
list1[0] = 2
print(list2)

# Copying part of the list
myList = [10, 8, 6, 4, 2]
newList = myList[1:3]
print(newList)
```

Your task is to write a program which removes all the number repetitions from the list. The goal is to have a list in which all the numbers appear not more than once.

```python
myList = [1, 2, 4, 4, 1, 4, 2, 6, 2, 9]
newList = []
for i in range(len(myList[:])):
    if myList[i] not in newList:
        newList.append(myList[i])
        # print(myList[i],'is added')
myList = newList  
print("The list with unique elements only:")
print(myList)
```

## List in List

```python
squares = [x ** 2 for x in range(10)]
odds = [x for x in squares if x % 2 != 0 ]
print(squares) #[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(odds) #[1, 9, 25, 49, 81]
```

