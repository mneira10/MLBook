---
redirect_from:
  - "/python/notebooks/basics/03-dictionaries"
interact_link: content/python/notebooks/basics/03_dictionaries.ipynb
kernel_name: python3
has_widgets: false
title: 'Dictionaries'
prev_page:
  url: /python/notebooks/basics/02_lists
  title: 'Lists'
next_page:
  url: /python/notebooks/basics/04_iteration
  title: 'Iteration'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


# Dictionaries

Dictionaries are a very useful data structure. They are similar to lists, but instead
of being indexed by integeres they are indexed by *keys* which can be of any type as long 
as they are immutable.  In a dictionary the *keys* are used to access *values*. 

A typical example would be the following:



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
d = {'Angela':  23746, 'Sofia': 2514, 'Luis': 3747, 'Diego': 61562}

```
</div>

</div>



In this example the keys are strings (corresponding to names) and the values are numbers.

We can acess now the values:



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
d['Angela']

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
23746
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
d['Diego']

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
61562
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
d['Luis']

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
3747
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
d['Sofia']

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
2514
```


</div>
</div>
</div>



Adding a new element in the dictionary is very simple



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
d['Valeriano'] = 1234

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print(d)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
{'Angela': 23746, 'Sofia': 2514, 'Luis': 3747, 'Diego': 61562, 'Valeriano': 1234}
```
</div>
</div>
</div>



deleting an item is also easy to do



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
d.pop('Angela')

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
23746
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print(d)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
{'Sofia': 2514, 'Luis': 3747, 'Diego': 61562, 'Valeriano': 1234}
```
</div>
</div>
</div>



It is possible to gather all the keys



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
list(d.keys())

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
['Sofia', 'Luis', 'Diego', 'Valeriano']
```


</div>
</div>
</div>



and also gather all the values



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
list(d.values())

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
[2514, 3747, 61562, 1234]
```


</div>
</div>
</div>



It is also easy to test whether a key (or value) is in the dictionary



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
'Miguel' in d.keys()

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
False
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
'Luis' in d.keys()

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
True
```


</div>
</div>
</div>



# Exercise 3.01

Create a dictionary with the integers `0` to `4` as keys and the vowels (a, e, i, o u) as values.



# Exercise 3.02

Use the following dictionary of dictionaries to create a new dictionary that has the same keys and the values correspond to the total number of hours used in all activities.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
activities = {
    'Monday': {'study':4, 'sleep':8, 'party':0},
    'Tuesday': {'study':8, 'sleep':4, 'party':0},
    'Wednesday': {'study':8, 'sleep':4, 'party':0},
    'Thursday': {'study':4, 'sleep':4, 'party':4},
    'Friday': {'study':1, 'sleep':4, 'party':8},
}

```
</div>

</div>

