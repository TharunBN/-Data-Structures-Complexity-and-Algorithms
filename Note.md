# Matrices & List comprehension
# Matrices in Python 3 #

**What is a matrix**
- A matrix is a representation of numbers, symbols or expressions in a 2-Dimensional Array
- In computer science, you create a data structure that has values in rows and coloumbs by using lists in inside lists. You can also import from Libraries and modules to   your python program to help you.
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
 
# Map & Filter in python 3 #: 

