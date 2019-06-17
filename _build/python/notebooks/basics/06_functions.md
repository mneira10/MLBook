---
redirect_from:
  - "/python/notebooks/basics/06-functions"
interact_link: content/python/notebooks/basics/06_functions.ipynb
kernel_name: python3
has_widgets: false
title: 'Functions'
prev_page:
  url: /python/notebooks/basics/05_control_structures
  title: 'Control Structures'
next_page:
  url: /python/notebooks/basics/07_objects
  title: 'Objects'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


# Functions

As in any other language *Python* allows for the definition of functions.
Functions are a set of sequence of instructions that receive well define inputs
and produce some outputs.

To define a function *Python* uses the word `def`. The value that the function returns
must be preceded by a `return`. The syntax would be:

```python
def FUNCTION_NAME(INPUTS):
    INSTRUCTIONS
    return OUTPUTS 
```

or

```python
def FUNCTION_NAME(INPUTS):
    INSTRUCTIONS
```

The `return` function is optional. Not every function should return an output. 
Some functions simply modify the inputs without producing any output.


**Important**:
The instructions and the return statements belonging to the fuction must be indented by *4 spaces* inside the header. Indentation is the only way that *Python* has to group lines of code.

Let's have some simple examples



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
def square(a):
    return a*a

print(square(1), square(2), square(5))

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_stream}
```
1 4 25
```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
square('a') # This should give an error

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">
{:.output_traceback_line}
```

    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-2-1e255ec27deb> in <module>()
    ----> 1 square('a') # This should give an error
    

    <ipython-input-1-8adcfd68d410> in square(a)
          1 def square(a):
    ----> 2     return a*a
          3 
          4 print(square(1), square(2), square(5))


    TypeError: can't multiply sequence by non-int of type 'str'


```
</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
def minimum(a, b):
    if a<b:
        return a
    elif b<a:
        return b
    else:
        return a

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
minimum(4,5)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
4
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
minimum(4,0)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
0
```


</div>
</div>
</div>



# Optional parameters

Functions can have default parameters. These parameters are defined using the syntaxis `arg=value`, 
where `arg` is the argument name and `value` is the default value for that argument.

Here are some examples



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
def power(a, b=2):
    return a**b

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
power(2)

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
4
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
power(2, b=5) # This is the prefered way to change the default parameters 

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
32
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
power(2,5) # This works as well

```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
32
```


</div>
</div>
</div>



# Exercise 2.1

Define a function `distance` that takes as arguments two lists `a,b` and computes
the Euclidean distance between the two:

$$
\sqrt{\sum_{i=0}^{N-1} (a_i - b_i)^2}
$$

Check your function with these three values
```python
distance([0,0], [1,1])
1.4142135623730951
```

```python
distance([1,5], [2,2])
3.1622776601683795
```

```python
distance([0,1,2], [2,3,4])
3.4641016151377544
```

