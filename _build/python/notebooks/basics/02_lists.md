---
redirect_from:
  - "/python/notebooks/basics/02-lists"
interact_link: content/python/notebooks/basics/02_lists.ipynb
kernel_name: python3
has_widgets: false
title: 'Lists'
prev_page:
  url: /python/notebooks/basics/01_numbers
  title: 'Numbers'
next_page:
  url: /python/notebooks/basics/03_dictionaries
  title: 'Dictionaries'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


# Lists and strings

Lists are data arrays. They can contain elements of different types (integers, floats).

An example of a list is



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l = [1,4.5, 6, 9.0, 10, -1]

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
[1, 4.5, 6, 9.0, 10, -1]
```


</div>
</div>
</div>



The most basic operation on a list is extracting its elements at a given position.
For that we use the position in the list keeping in mind that the first element starts at `0`.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[0]

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
1
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[5]

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
-1
```


</div>
</div>
</div>



The indexing also works backwards using negative numbers



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[-1]

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
-1
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[-3]

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
9.0
```


</div>
</div>
</div>



If you try to use an index beyond the list size you will get an error



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[6]

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_traceback_line}
```

    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    <ipython-input-7-cb842cca7e42> in <module>()
    ----> 1 l[6]
    

    IndexError: list index out of range


```
</div>
</div>
</div>



Lists are mutable. That means you can change the value of an item as follows



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[0] = 100

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
[100, 4.5, 6, 9.0, 10, -1]
```


</div>
</div>
</div>



## Slicing

Arguably, the most useful list operation is *slicing*.
You can use it to quickly select a subset from the list. 
Slicing consists in using two different indices separated by `:` to select the elements
with the syntax `l[start:end]`


Here are some examples. Please be sure that you understand how tthe `start:end` indexing works!. That's the whole point of slicing, if some of the examples are unclear, please ask!



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print(l) # this is the full list

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
[100, 4.5, 6, 9.0, 10, -1]
```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[0:4] #start=0, end=4

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
[100, 4.5, 6, 9.0]
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[2:4] #start=2, end=4

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
[6, 9.0]
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[-4:-1] #start=-4, end=-1, negative values are allowed.

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
[6, 9.0, 10]
```


</div>
</div>
</div>



Slicing also works if you use only one index.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[3:]

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
[9.0, 10, -1]
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l[:4]

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
[100, 4.5, 6, 9.0]
```


</div>
</div>
</div>



The mathematical operations `+` and `*` can also be used with lists.
The first operation is used for concatenation and the second for repetition.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
m = [45, -56]
print('l=', l)
print('m=', m)
n = l + m
print('n=',n) # this is the concatenation

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
l= [100, 4.5, 6, 9.0, 10, -1]
m= [45, -56]
n= [100, 4.5, 6, 9.0, 10, -1, 45, -56]
```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
m + l #sum of lists does not commute!

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
[45, -56, 100, 4.5, 6, 9.0, 10, -1]
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
2 * l # here I am reapeating the list `l` two times.

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
[100, 4.5, 6, 9.0, 10, -1, 100, 4.5, 6, 9.0, 10, -1]
```


</div>
</div>
</div>



The function `sorted` can be used on lists to reorder the objects



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
l_sorted = sorted(l)
print(l_sorted)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
[-1, 4.5, 6, 9.0, 10, 100]
```
</div>
</div>
</div>



and the function `len` gives you the number of items in the list



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
len(l)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
6
```


</div>
</div>
</div>



In python the strings are defined as a list of characters



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
given_name = "Silvia"
family_name = "Rivera Cusicanqui"

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print(given_name + " " + family_name) # This is the concatenations of the strings

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
Silvia Rivera Cusicanqui
```
</div>
</div>
</div>



These strings have many useful methods



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
given_name.upper() #convert to upper case

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
'SILVIA'
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
given_name.replace('i', 'y') #replace 'i' with 'y'

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
'Sylvya'
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
given_name.count('i') # count how many times 'i' is the string

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
2
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
family_name.split() # split the original string in the places with spaces, the result is a new list.

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
['Rivera', 'Cusicanqui']
```


</div>
</div>
</div>



# Exercise 2.01

* Define a list with the integers from 1 to 10 and use slicing print the second half of the list.



# Exercise 2.02

* Build a list with 100 repetitions of the sequence `1`, `-1` (i.e. `[1,-1,1,-1,1,-1,...]`)



# Exercise 2.03

* Build a list that contains a `1` surrounded by 15 zeroes on the left and the right.



# Exercise 2.04

* Compute the median of the following list

`a = [21, 48, 79, 60, 77, 
    15, 43, 90,  5,  49, 
    15, 52, 20, 70, 55,  
    4, 86, 49, 87, 59]`

