---
redirect_from:
  - "/python/notebooks/basics/01-numbers"
interact_link: content/python/notebooks/basics/01_numbers.ipynb
kernel_name: python3
has_widgets: false
title: 'Numbers'
prev_page:
  url: /python/pythonBasics
  title: 'Python basics'
next_page:
  url: /python/notebooks/basics/02_lists
  title: 'Lists'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


# Integer and floats

You can make the following operations with integer and floats (i.e. real mumbers)

| Operation | Result       |
| --------- | --------------- |
|    +      | Sum           |
|    -      | Substraction           |
|    *      | Multiplication  |
|    /      | Division        |
|    //     | Integer division |
|    \*\*   | Exponentiation        |

Some simple examples are



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
4+2

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
10-42

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
4 * 4

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
10/3

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
10//3

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
10**3

```
</div>

</div>



# Exercise 1.1

Compute the number of seconds since the day you were born



# Complex numbers

It is also posible to use complex numbers. Instead of using $i$ for $\sqrt{-1}$ python uses `j`.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
1j**2

```
</div>

</div>



# Some typical math operations

Very common mathematical operations, sucha as taking the logarithm, can only be used after importing the module math.

For instance:



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
import math

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
math.log(10) #natural logarithm

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
math.log10(10) #base 10 logarith,

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
math.sqrt(10) # square root

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
math.exp(2) # exponential

```
</div>

</div>



# Exercise 1.2

Compute the value for the golden ratio number $(1+\sqrt{5})/2$

