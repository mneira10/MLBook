---
redirect_from:
  - "/python/notebooks/basics/04-iteration"
interact_link: content/python/notebooks/basics/04_iteration.ipynb
kernel_name: python3
has_widgets: false
title: 'Iteration'
prev_page:
  url: /python/notebooks/basics/03_dictionaries
  title: 'Dictionaries'
next_page:
  url: /python/notebooks/basics/05_control_structures
  title: 'Control Structures'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


# Iteration

One of the most basic operations in programming is iterating over a list of elements to perform some kind of operation.

In python we use the `for` statement to iterate. It is easier to use than the same statement in C, C++ or FORTRAN because instead of running over a integer index it takes as an input any iterable object and runs over it.

Let's see some examples



## Iterating over lists

Lists are ordered. Iteration is done in the same order as the input list.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
a = [4,5,6,8,10]
for i in a:
    print(i)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
4
5
6
8
10
```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
# A fragment of `One Hundred Years of Solitude`
GGM = 'Many years later, as he faced the firing squad, \
Colonel Aureliano Buendía was to remember that dist \
ant afternoon when his father took him to discover ice. \
At that time Macondo was a village of twenty adobe houses,\
built on the bank of a river of clear water that ran along \
a bed of polished stones, which were white and enormous,\
like prehistoric eggs.'
print(GGM)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
Many years later, as he faced the firing squad, Colonel Aureliano Buendía was to remember that dist ant afternoon when his father took him to discover ice. At that time Macondo was a village of twenty adobe houses,built on the bank of a river of clear water that ran along a bed of polished stones, which were white and enormous,like prehistoric eggs.
```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
dot = GGM.split()  # we create a list where each element is a word
print(dot)
for i in dot:
    print(i)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
['Many', 'years', 'later,', 'as', 'he', 'faced', 'the', 'firing', 'squad,', 'Colonel', 'Aureliano', 'Buendía', 'was', 'to', 'remember', 'that', 'dist', 'ant', 'afternoon', 'when', 'his', 'father', 'took', 'him', 'to', 'discover', 'ice.', 'At', 'that', 'time', 'Macondo', 'was', 'a', 'village', 'of', 'twenty', 'adobe', 'houses,built', 'on', 'the', 'bank', 'of', 'a', 'river', 'of', 'clear', 'water', 'that', 'ran', 'along', 'a', 'bed', 'of', 'polished', 'stones,', 'which', 'were', 'white', 'and', 'enormous,like', 'prehistoric', 'eggs.']
Many
years
later,
as
he
faced
the
firing
squad,
Colonel
Aureliano
Buendía
was
to
remember
that
dist
ant
afternoon
when
his
father
took
him
to
discover
ice.
At
that
time
Macondo
was
a
village
of
twenty
adobe
houses,built
on
the
bank
of
a
river
of
clear
water
that
ran
along
a
bed
of
polished
stones,
which
were
white
and
enormous,like
prehistoric
eggs.
```
</div>
</div>
</div>



## Iterating over dictionaries
Dictionaries are not ordered. Iterating over them does not have to produce an order sequence.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
a = {} # empty dictionary
a[1] = 'one'
a[2] = 'two'
a[3] = 'three'
a[4] = 'four'
a[5] = 'five'
print(a)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
{1: 'one', 2: 'two', 3: 'three', 4: 'four', 5: 'five'}
```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
for k in a.keys(): # iterate over the keys
    print(a[k])

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
one
two
three
four
five
```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
for v in a.values(): #iterate over the values
    print(v)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
one
two
three
four
five
```
</div>
</div>
</div>



## Iterating over a sequence

The function `range()` is useful to generate a sequence of integers that can be used to iterate.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print(range(10)) # range itself returns an iterable object
a = list(range(10)) # this translates that iterable object into a list
print(a) # be careful! the lists has 10 objects starting with 0

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
range(0, 10)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
for i in range(10): # if you given a single argument the iterations starts at 0.
    print(i)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
0
1
2
3
4
5
6
7
8
9
```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
for i in range(4,10): # you can algo give two arguments: range(start, end). 
    print(i)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
4
5
6
7
8
9
```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
for i in range(0,10,3): # if you give three arguments they are interpreted as range(start, end, step)
    print(i)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
0
3
6
9
```
</div>
</div>
</div>



# Exercise 4.01
Write a `for` cycle that prints the sequence: 5, 4, 3, 2, 1, 0.



# Exercise 4.02

The following can be used to generate a random number between 0 and 1:

```python
import random
a = random.random()
```
Use `random.random()` and a `for` cycle to compute the sum of 100 random numbers.



# Exercise 4.03

Use the results from the previous exercise to compute the standard deviation of 
a list of `1000` numbers where each number is itself the sum of `N=100` random numbers. 
What is the answer if `N=200`? `N=300`? 

