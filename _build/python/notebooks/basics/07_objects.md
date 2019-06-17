---
redirect_from:
  - "/python/notebooks/basics/07-objects"
interact_link: content/python/notebooks/basics/07_objects.ipynb
kernel_name: python3
has_widgets: false
title: 'Objects'
prev_page:
  url: /python/notebooks/basics/06_functions
  title: 'Functions'
next_page:
  url: /python/notebooks/basics/08_modules
  title: 'Modules'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


# Objects

*Python* is an object oriented language. As such it allows the definition of classes.

For instance lists are also classes, that's why there are methods associated with them (i.e. `append()`). Here we will see how to create classes and assign them attributes and methods.




## Definition and initialization

A class gathers functions (called methods) and variables (called attributes).
The main of goal of having this kind of structure is that the methods can share a common
set of inputs to operate and get the desired outcome by the programmer.

In *Python* classes are defined with the word `class` and are always initialized
with the method ``__init__``, which is a function that *always* must have as input argument the
word `self`. The arguments that come after `self` are used to initialize the class attributes.

In the following example we create a class called ``Circle``.




<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
class Circle:
    def __init__(self, radius):
        self.radius = radius #all attributes must be preceded by "self."

```
</div>

</div>



To create an instance of this class we do it as follows



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
A = Circle(5.0)

```
</div>

</div>



We can check that the initialization worked out fine by printing its attributes



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print(A.radius)

```
</div>

</div>



We now redefine the class to add new method called `area` that computes the area of the circle



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
class Circle:
    def __init__(self, radius):
        self.radius = radius #all attributes must be preceded by "self."
    def area(self):
        import math
        return math.pi * self.radius * self.radius

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
A = Circle(1.0)

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
print(A.radius)
print(A.area())

```
</div>

</div>



### Exercise 3.1

Redefine the class `Circle` to include a new method called `perimeter` that returns the value of the circle's perimeter.



We now want to define a method that returns a new Circle with twice the radius of the input Circle.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
class Circle:
    def __init__(self, radius):
        self.radius = radius #all attributes must be preceded by "self."
    def area(self):
        import math
        return math.pi * self.radius * self.radius
    def enlarge(self):
        return Circle(2.0*self.radius)

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
A = Circle(5.0) # Create a first circle
B = A.enlarge() # Use the method to create a new Circle
print(B.radius) # Check that the radius is twice as the original one.

```
</div>

</div>



We now add a new method that takes as an input another element of the class `Circle`
and returns the total area of the two circles



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
class Circle:
    def __init__(self, radius):
        self.radius = radius #all attributes must be preceded by "self."
    def area(self):
        import math
        return math.pi * self.radius * self.radius
    def enlarge(self):
        return Circle(2.0*self.radius)
    def add_area(self, c):
        return self.area() + c.area()

```
</div>

</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
A = Circle(1.0)
B = Circle(2.0)
print(A.add_area(B))
print(B.add_area(A))

```
</div>

</div>



### Exercise 3.2

Define the class `Vector3D` to represent vectors in 3D.
The class must have

* Three attributes: `x`, `y`, and `z`, to store the coordinates.

* A method called `dot` that computes the dot product

    $$\vec{v} \cdot \vec{w} = v_{x}w_{x} + v_{y}w_{y} + v_{z}w_{z}$$

  The method could then be used as follows
  
```python
v = Vector3D(2, 0, 1)
w = Vector3D(1, -1, 3)
```
    
```python
v.dot(w)
5
```

