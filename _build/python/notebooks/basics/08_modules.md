---
redirect_from:
  - "/python/notebooks/basics/08-modules"
interact_link: content/python/notebooks/basics/08_modules.ipynb
kernel_name: python3
has_widgets: false
title: 'Modules'
prev_page:
  url: /python/notebooks/basics/07_objects
  title: 'Objects'
next_page:
  url: /other/suggestions
  title: 'Suggestions and stuff'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


# Using modules

Python has a great variety of modules that can be used for differente tasks.
For instance, there are modules to read/write Excel files, processing large amounts of data, 
manipulating astronomical coordinates or making plots.

There are at least three options to use modules in *Python*.



## Using `import`




The first option to use a module is with the command `import` followed by the module name.

```python
import math
```
Whenever we want to use a function from that module we have to do it by writing the libraty name followed by a dot (`.`) and the function. 
If you write `math.` and use the Tab key, that should show a list with the functions that are part of the module.




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
math.

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
# we can use now some function
math.sin(math.pi/2)

```
</div>

</div>



## Using `from`

Another option is importing only the function that you need 


```python
from math import sin
```

In this case only the function `sin` is imported and not the rest of the library



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
from math import sin

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
sin(1.0)

```
</div>

</div>



However, you cannot use `pi` because it has not been imported



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
sin(pi/2)

```
</div>

</div>



you could import it in the same way as we did with `sin`



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
from math import sin, pi # now pi is available

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
sin(pi/2)

```
</div>

</div>



## Using `import as`

You can also rename a module at the moment of importing it.

```python
import math as mt
```

In this case, instead of using `math.sin()` we can use `mt.sin()`



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
import math as mt

```
</div>

</div>



You can then use the following to see the documentation of a function



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
mt.sin?

```
</div>

</div>



### Exercise 4.1

Import the module `random` and use the function `shuffle` to shuffle the contents of a list that has the integers from 0 to 9. Print the list before and after shuffling. Use `random.shuffle?` to read the documentation string for that function.





<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
import random

```
</div>

</div>

