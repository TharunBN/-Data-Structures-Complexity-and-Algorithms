# Matrices & List comprehension
# Matrices in Python 3 #

**What is a matrix**
- A matrix is a representation of numbers, symbols or expressions in a 2-Dimensional Array
- In computer science, you create a data structure that has values in rows and coloumbs by using lists in inside lists. You can also import from Libraries and modules to your python program to help you.

[*Example*]

![matrix_fig01](https://user-images.githubusercontent.com/129294830/233748137-da7c1133-1ffb-46b3-bb11-f411558898c0.png)

~ this is a mathematical notation of what a matrix should look ike
```Let A represent the matrix
Matrix A has m rows and n columns ... in this case 2 rows and 4 columns.

Row 1 has values of 1 2 3 4
Column 2 has values of 2 6
```
**Matrix A in python 3**:
[*Matrix in Python 3 example*](https://mrparkonline.github.io/courses/datastruct/matrices/):
```# Python 3 Representation of matrix A

matrix_A = [
    [1, 2, 3, 4],
    [5, 6, 7, 8]
]

# Accessing Matrix A
print('Row 1: %s' % matrix_A[0]) # Recall: Indexing starts at zero in Python
print('Value at Row 2 Column 2: %s' % matrix_A[1][1])

*Output*: The first output statement will print Row 1: [1, 2, 3, 4]
*Output*: The second output statement will print out row 2 Column 2: 6
```
- In Python 3, there is no such thing as the 'Matrix'. we use slist within a list
- All rows must be the same number of values
- Coloums must have the same number values
- all 2-D item data types be the same
- due to indexing starting at 0, that would mean that row one is technically located at matrix_A[0]

**List Comprehension 3**:
- A list comprehension a method to create a list in python 3
----
~ This technique is commonily used
 - The list is a result of some operations that are applied to all of its items
 - Usually made from another sequence or iterable data
 - It is a member of another list,sequence or even iterable data
**List Comprehension 1**:
[*Example*](https://mrparkonline.github.io/courses/datastruct/matrices/)
```# Old Method
squares = []
for i in range(10):
    squares.append(i ** 2)

print('Our result: %s' % squares)

# result:[0, 1, 4, 9, 16, 25, 36, 49, 64, 81] 
```
[*Exmaple*](https://mrparkonline.github.io/courses/datastruct/matrices/)

```# List Comprehension

squares = [i**2 for i in range(10)]

print('Our new result: %s' % squares)

new result: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

**How does it work?**:

- A list comprehension consists of:
    - A **square breacket** containing expressions that describe the list
    - one or more **For Clause** that explains its members
    - Then a zero or more **If Clause** depending on the complexity of the list
 
# Map & Filter in python 3: 

**The Map function**
 - The purpose of a map function is to apply a function to a iterable data
[*Map Function Example](https://mrparkonline.github.io/courses/datastruct/map/)
```
# Example
def square(num):
    ''' squares the given num argument '''
    return num ** 2
# end of square

array = list(range(1,11))
square_array = list(map(square, array))

print('Original Array:', array)
print('Array Squared:', square_array)

Output: Original Array: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
2nd Output: Array Squared: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```
- One thing aboutthe map function is that it doesnt return specific data but instead a python iterable data. So, to counter this, we execute a list function after a     map function

**Filter Function**:
- The idea of the filter function is it filters out items of the set from data that meets the **certain requirment**
[*Filter Function Example*](https://mrparkonline.github.io/courses/datastruct/map/)
```
# Example 3

def isOdd(x):
    ''' isOdd() returns True if x is odd.'''
    return x % 2 != 0

array = list(range(1,101))
odds = list(filter(isOdd, array))

print('Odd Numbers from 1 to 100:', odds)

#Results: Odd Numbers from 1 to 100: [1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51, 53, 55, 57, 59, 61, 63, 65, 67, 69, 71, 73, 75, 77, 79, 81, 83, 85, 87, 89, 91, 93, 95, 97, 99]
```
-----
[*Example of palindromic Numbers](https://mrparkonline.github.io/courses/datastruct/map/)
```
# Palindromic Numbers from 1 to 10000

def isPalindrome(x):
    ''' isPalindrome returns True if string X is a palindrome.'''
    return x == x[::-1]

array = list(range(1,10000))

palindromic_numbers = list(map(int, filter(isPalindrome, map(str, array))))
print('Palindromic Numbers from 1 to 10,000', palindromicNumbers)

Result:Palindromic Numbers from 1 to 10,000 [1, 2, 3, 4, 5, 6, 7, 8, 9, 11, 22, 33, 44, 55, 66, 77, 88, 99, 101, 111, 121, 131, 141, 151, 161, 171, 181, 191, 202, 212, 222, 232, 242, 252, 262, 272, 282, 292, 303, 313, 323, 333, 343, 353, 363, 373, 383, 393, 404, 414, 424, 434, 444, 454, 464, 474, 484, 494, 505, 515, 525, 535, 545, 555, 565, 575, 585, 595, 606, 616, 626, 636, 646, 656, 666, 676, 686, 696, 707, 717, 727, 737, 747, 757, 767, 777, 787, 797, 808, 818, 828, 838, 848, 858, 868, 878, 888, 898, 909, 919, 929, 939, 949, 959, 969, 979, 989, 999, 1001, 1111, 1221, 1331, 1441, 1551, 1661, 1771, 1881, 1991, 2002, 2112, 2222, 2332, 2442, 2552, 2662, 2772, 2882, 2992, 3003, 3113, 3223, 3333, 3443, 3553, 3663, 3773, 3883, 3993, 4004, 4114, 4224, 4334, 4444, 4554, 4664, 4774, 4884, 4994, 5005, 5115, 5225, 5335, 5445, 5555, 5665, 5775, 5885, 5995, 6006, 6116, 6226, 6336, 6446, 6556, 6666, 6776, 6886, 6996, 7007, 7117, 7227, 7337, 7447, 7557, 7667, 7777, 7887, 7997, 8008, 8118, 8228, 8338, 8448, 8558, 8668, 8778, 8888, 8998, 9009, 9119, 9229, 9339, 9449, 9559, 9669, 9779, 9889, 9999]
```
------
**Composition of Functions**
- Composition of Functions is the idea of **using funcitons inside a funciton call** or **applying a function for another function**

# Tuples in Python 3:

**What are Tuples?**

 - String and lists are basic iterable datat types that are very similar with **minor differences**
 - With a string, they only allow alphanumeric charatcers and special symbols to represent text
 - Lists on the other hand allow all type of data types as its items and memebers
 - Another difference is that strings are immutable while Lists are Mutable
~ Due to this, it causes problems when trying to follow data structure
 - it must be immutable
 - it must allow various datatypes as items
 - it should be iterable
 - it should be nestable

**How to use Tuple in Python 3**
- Tuples use round brackets
- () is a sign of an empty tuple
- (50,) this is called a singleton tuple, the comma is a must
- Tuples are sliceable meaning they are indexable using square brackets

[*Tuple Example*](https://mrparkonline.github.io/courses/datastruct/tuples/)
```
tup = ('C', ' Java', 'Python')
empty_tup = ()
single_tup = ('Park',)

print(tup)
print(empty_tup)
print(single_tup)

Result: ('C', ' Java', 'Python')
Result 2: ()
Result 3: ('Park',)
```

**Tuple Operators**
- Concatenation: Joining two tuples
- Repition: Repating a list mutliple times
- Membership: Check if a value exist in tuple

**Tuple Comprehension**
- If parentheses are taken off, the functionality would change and would be a different functionality in python. Therefore, comprehension would be a must.






