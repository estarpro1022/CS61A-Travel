### expression

```python
>>>max(2, 3)
3
>>>min(2, 3)
2
>>>from operator import add, mul
>>>add(2, 3)
5
>>>mul(2, 3)
6
```
```python
>>>mul(add(2, 9), mul(3, 4))
132

```

#### Types of Expressions

* primitive expressions:
  * number of numeral: 2
  * name: radius
  * string: 'hello'
* call expression:
  * max   (2, 3)
  * operator (operand comma operand)   parenthesis

### name

```python
>>> from math import pi, sin
>>> pi
3.141592653589793
>>> sin (pi / 2)
1
```

```python
>>> radius = 10
>>> area, circ = pi * radius * radius, 2 * pi * radius
>>> area
314....
>>> radius = 20
>>> area
314....
# things are not sync
# evaluate pi * pi * radius, then the value get bounded to area, but area forget it was defined in terms of radius

# how might we keep them in sync
>>> def area():
...     return pi * radius * radius
...
>>> area()	# have no operands
1256(omission)
>>> pi * radius * radius
1256
>>> radius = 10
>>> area()
314
# keep them in sync by function
```

```python
>>> max
<built-in function max>
>>> f = max
>>> f
<built-in function max>
# f and max are both names for the function

>>> max = 7
# broke the origin max function, max means sth different
>>> f(1, 2, max)
7
>>> max = f
# fortunately, i have the name for that
>>> max
<built-in function max>
```

```python
>>>def square(x):
...    return mul(x, x)
...
>>> square
<function square at 0x000001C437536A60>
>>> def sum_squares(x, y):
    return square(x) + square(y)
>>> sum_square(3, 4)
25
```



* import a name
  * from operator import add, mul
* assign a value to name
  * radius = 10
* def statement by creating our own function
  * def area()





### Environment Diagrams

Keep track of what names mean

* Each name is bound to at most one value in a frame
* Within a frame, a name cannot be repeated



#### pythontutor visualize code, making it clearer

![image-20220304210637292](https://gitee.com/starriverflow/cloud-pictures/raw/master/img/image-20220304210637292.png)



#### How to draw an expression tree

* evaluate operator
* evaluate operands
* evaluate subexpression



![image-20220304211549262](https://gitee.com/starriverflow/cloud-pictures/raw/master/img/image-20220304211549262.png)
