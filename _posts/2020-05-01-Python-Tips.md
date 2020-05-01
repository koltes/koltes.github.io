---
title: PYTHON TIPS'N'TRICKS
tags:
    - python
sidebar:
    nav: 'side'
---

## Oneliner

Sometimes you want, or have to, write some statements into one line of code. Maybe, because you are working in a parameter.

#### IF statement

if you want to set a value depending on a condition, you can write the following:  
`variable = value if condition else othervalue`

This can be used to to  set a parameter depending on another one.

#### LIST

If you need to fill a list with values, you do not have to write a complete loop over several  lines. You can  write the loop into the list itself.

`variable = [x for x in loopable]  
par.val = [row[0].val for row in op('table1').rows()]     #this will set the parametervalue to a list of all the values in the first col of table1`

## HAS, GET, set ATTR

One of the most asked questions about python is, how do I acces as parameter if i have the name as a string.

By using the attr functions. The names say it all.

```
boolean  = hasattr(object, "attribute name")  
 hasparameter = hasattr( op('operator').par, 'Level') 

attribute = getattr(object, "attribute name")  
parameter = getattr( op('operator').par, 'Level')

setattr(object, "attribute name", vaulue)  
setattr( op('operator'), 'level', 100)

```

But, be aware, this functions take quite a lot of time. So use them rarely. Best is to call them once in save the results into: