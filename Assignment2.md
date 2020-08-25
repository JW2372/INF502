```python
import math
import numpy as np

def pythagoreanTheorem(length_a, length_b):
    length_c = math.sqrt(pow(length_a, 2)+pow(length_b, 2))
    return length_c

def list_mangler(list_in):
    list_out = []
    for i in list_in:
        if i%2 == 0:
            list_out.append(i * 2)
        else:
            list_out.append(i * 3)
    return list_out

def grade_calc(grades_in, to_drop):
    grades_in.sort()
    del grades_in[:to_drop]
    if np.mean(grades_in) >= 90:
        grade = 'A'
    elif np.mean(grades_in) >= 80:
        grade = 'B'
    elif np.mean(grades_in) >= 70:
        grade = 'c'
    elif np.mean(grades_in) >= 60:
        grade = 'D'
    else:
        grade = 'F'
    return grade

def odd_even_filter(numbers):
    odd=[]
    even=[]
    for i in numbers:
        if i % 2 == 0:
            even.append(i)
        else:
            odd.append(i)
    odd_even = [[even],[odd]]
    return odd_even




print(pythagoreanTheorem(2, 2))
print(list_mangler([1, 2, 3, 4]))
print(grade_calc([100, 90, 80, 95], 2))
print(odd_even_filter([1, 2, 3, 4, 5, 6, 7, 8, 9]))
print(odd_even_filter([3, 9, 43, 7]))
print(odd_even_filter([71, 39, 98, 79, 5, 89, 50, 90, 2, 56]))
```
