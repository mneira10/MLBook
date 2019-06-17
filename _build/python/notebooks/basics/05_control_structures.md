---
redirect_from:
  - "/python/notebooks/basics/05-control-structures"
interact_link: content/python/notebooks/basics/05_control_structures.ipynb
kernel_name: python3
has_widgets: false
title: 'Control Structures'
prev_page:
  url: /python/notebooks/basics/04_iteration
  title: 'Iteration'
next_page:
  url: /python/notebooks/basics/06_functions
  title: 'Functions'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


# If (elif, else)

This is probably the most used conditional structure in programming. 
Here is the syntax in *Python*



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
a = 1
b = 4

if a < b:
    print('a is smaller than b')
elif a > b:
    print('a is larger than b')
else:
    print('a is equal to b')

```
</div>

</div>



*Important*: the lines of code after the `if`, `elif`, `else` statement have to be indented by 4 spaces to indicate that they are part of the same instructions block.

The table below includes some of the operators that can be used inside the `if` conditions. They all return a boolean variable (True or False).


| Operator | Meaning
| -------- | ---------
|   ==     | Equal to 
|   !=     | Not equal        
|   <      | Smaller than
|   >      | Larger than
|   <=     | Smaller-equal than
|   >=     | Larger-equal than
|   not    | Logiccal Negation 
|   in     | Checks whether an element is in a list
|   and    | Checks whether two conditions are True
|   or     | Checks whether at least one condition is True
|   is     | Checks whether an elemenent is equal to another.

Let see some examples:



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
5 in [1, 2, 4]

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
3 in [1, 2, 3]

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
not (2 == 5)

```
</div>

</div>



# while

This control structure also checks for a condition to be `True` in order to execute a series of instructions. The 4 space rule for indentantion also applies.




<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
a = []
while len(a) < 10:
    a.append(0) # add elements to the list until I have 10.
print(a)

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
# This is an example of random walk.
import random

position = 0
n_steps = 0
while abs(position) < 10: # I will walk until I am a distance of 10
    step = 2.0*(random.random()-0.5) # this is a random variable between -1 and 1
    position += step
    n_steps += 1
    
print(position, n_steps) # this is the final position and the number of steps

```
</div>

</div>



# Exercise 1.1

Compute how many times, on average, do you have to throw a die (with only six faces) in order to reach reach a minimum of 100 points. In this game you start with 0 points, you throw the die and add the number you get to the total account. Use the results of random.random() to implement the die throw.

