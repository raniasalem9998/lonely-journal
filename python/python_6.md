| [Introduction to Python and computer programming](python_1.md)  | [Data Types](python_2.md)   | [Variables/input](python_3.md) | [Booleanvalues,conditions,loops,listsandlogic](python_4.md) |[Lists](python_5.md)|[functions](python_6.md)|[tuple](python_7.md)|[modles](python_8.md)
# Functions

look at this snippet:

```python
print("We start here.")

def message():
    print("Enter a value: ")

message()

print("We end here.")
```

**A function is a block of code that performs a specific task when the function is called (invoked). You can use functions to make your code reusable, better organized, and more readable. Functions can have parameters and return values.**

## Shadowing

```python
def message(number):
    print("Enter a number:", number)

number = 1234
message(1)
print(number)
```

will show:

```
Enter a number: 1
1234
```

## Return 

```python
def strangeListFunction(n):
    strangeList = []
    
    for i in range(0, n):
        strangeList.insert(0, i)
    
    return strangeList

print(strangeListFunction(5)) #[4, 3, 2, 1, 0]
```

example from the past 
```python
def isYearLeap(year):
    if year%4 != 0 :
     return False
    elif year%100 != 0 :
     return True
    elif year%400 != 0 :
     return False
    else :
     return True

testData = [1900, 2000, 2016, 1987]
testResults = [False, True, True, False]
for i in range(len(testData)):
	yr = testData[i]
	print(yr,"->",end="")
	result = isYearLeap(yr)
	if result == testResults[i]:
		print("OK")
	else:
		print("Failed")
```

Calculating days in months:
```python
def isYearLeap(year):
    if year%4 != 0 :
     return False
    elif year%100 != 0 :
     return True
    elif year%400 != 0 :
     return False
    else :
     return True

def daysInMonth(year, month):
 day31 = [1,3,5,7,9]
 day30 = [4,6,8,10,11,12]
 feb = [28,29]
 if month in day31:
     return 31
 if month in day30:
     return 30
 if month == 2:
     if isYearLeap(year) == False:
         return 28
     else:
         return 29
 return
testYears = [1900, 2000, 2016, 1987]
testMonths = [2, 2, 1, 11]
testResults = [28, 29, 31, 30]
for i in range(len(testYears)):
	yr = testYears[i]
	mo = testMonths[i]
	print(yr, mo, "->", end="")
	result = daysInMonth(yr, mo)
	if result == testResults[i]:
		print("OK")
	else:
		print("Failed")
```
**this just wont work for other years than 1900 idk why**
```python
def isYearLeap(year):
    if year%4 != 0 :
     return False
    elif year%100 != 0 :
     return True
    elif year%400 != 0 :
     return False
    else :
     return True

def daysInMonth(year, month):
 day31 = [1,3,5,7,9]
 day30 = [4,6,8,10,11,12]
 feb = [28,29]
 if month in day31:
     return 31
 if month in day30:
     return 30
 if month == 2:
     if isYearLeap(year) == False:
         return 28
     else:
         return 29
 return
def dayOfYear(year, month, day):
 week = ['sun','mon','tus','wed','thu','fri','sat']
 days = 0
 for i in range(1900,year): # 1-1 monday
    for j in range(1,daysInMonth(i,month)):
        for k in range (0,day):
         days += 1
         day = int((days / 7 - days // 7)*10)
 print(days , day)
 return week[day]
print(dayOfYear(2000,12,31))
```
Prime number test:

```python
def isPrime(num):
    numbersToDevide = [2,3,5,7]
    for i in numbersToDevide:
        if num % i != 0:
            return num
        if num == i:
            return i
        else :
            return 

for i in range(1, 20):
	if isPrime(i + 1):
			print(i + 1, end=" ")

```