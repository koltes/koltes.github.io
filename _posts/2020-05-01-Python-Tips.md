---
title: PYTHON TIPS'N'TRICKS
tags:
    - python
    - touchdesigner
sidebar:
    nav: 'side'
---
[Copiado de un artículo de ALPHAMOONBASE][article] en la página de Touchdesigner.  

## Oneliner

Sometimes you want, or have to, write some statements into one line of code. Maybe, because you are working in a parameter.

#### IF statement

if you want to set a value depending on a condition, you can write the following:  

```python
variable = value if condition else othervalue
```

This can be used to to  set a parameter depending on another one.

#### LIST

If you need to fill a list with values, you do not have to write a complete loop over several  lines. You can  write the loop into the list itself.

```python
variable = [x for x in loopable]  
par.val = [row[0].val for row in op('table1').rows()]
# this will set the parametervalue to a list 
# of all the values in the first col of table1
```

## HAS, GET, set ATTR

One of the most asked questions about python is, how do I acces as parameter if i have the name as a string.

By using the attr functions. The names say it all.

```python
boolean  = hasattr(object, "attribute name")  
 hasparameter = hasattr( op('operator').par, 'Level') 

attribute = getattr(object, "attribute name")  
parameter = getattr( op('operator').par, 'Level')

setattr(object, "attribute name", vaulue)  
setattr( op('operator'), 'level', 100)

```
But, be aware, this functions take quite a lot of time. So use them rarely. Best is to call them once in save the results into:

## DICTIONARIES

Dicts are truly amazing and make programming with python so much easier. A dictionarie is a collection of values, accessable by a key.

```python
myDict = { key : value }  
myDict[key] return value
```
But the truly amazing thing is, that key and value are not bound to be strings or anything. They can be what ever you want. You can define funtions to be called at a certain key, or define a parameter object as the key. The following dictionary will use a debug or print statement, depending on the parameter you pass into the dictionary: 
```python 
myDict = { op('operator').par.Level      : debug,  
            op('operator').par.Intensity : print, }  
myDict[par](par.val)
```                                
  
When calling a function, you can pass the arguments as a dictionary using:

```python  
def myFunction(a, b, c = ''):  
`    debug(a, b, c)`  
argumentdict = { "a" : 1, 
                 "b" : 2,  
                 "c" : 'A text',  
               }  
myFunction(**argumentdict)
```

## JSON

I work more and more with webapplications, and JSON (JavaScript Object Notation) is a staple of the game. Its easy to read, edit and understand. (I know there are people defending XML. Poor souls.) The JSON notation looks something like the following: 
```json 
myJsonString = '{ "Name" : "Hibert" }'
```

Looks familiar? It basicly is the same as dicts in python. But not all the way. JSON is String only, so when working with json in touch, you will need to parse the string first. Luckily, Python supports JSON without problems, just import the json module.  

```python  
import json  
myJsonDict = json.loads(myJsonString)  
debug(myJsonDict['Name'])
```

And whats even better, you can turn basicly every python dict into a json string. You can, for example, store some configuration of the project into a dict and export is as a JSON File and only use that JSON file to bringt your config to the system. 
```python 
import json  
config_dict = { 'Level' : op.settings.par.Level.eval(),  
                'Brightness' : op.settings.par.Brightness.eval(), } 

config_json = json.dumps(config_dict, indent = 4``) 
#indent increases the readability alot  

op('text1').text = congig_json  
op('text1').save('config.json')
```

giving us a file looking like that:
```json  
{    
"Level": 0.0,     
"Brightness": 0.0  
}
```
## TDU REMAP

The tdu functions are another nice tool given to us by derivative. The tdu function are a set of function hardcoded into the engine and running extremly fast. By using them you can remove clutter from your project. Lets have a look. Here we have a RAMP Lfo driving two parameter with different range:

![multiapproach.PNG](https://derivative.ca/sites/default/files/field/body-images/multiapproach.PNG)


This takes up some space, and scales badly. Imagine how this looks like with 10 circles. Now let's delete the two mathChops and one of the nulls and lets use the tdu.remap function. It is defines the following:

```python
tdu.remap( value, from_min, from_max, to_min, to_max)
```

So now we can put the following expression in  our scale parameter: 
```python 
`tdu.remap( op('null2')['chan1'], 0, 1, 0.3, 0.4)
```


![ singleapproach.PNG](https://derivative.ca/sites/default/files/field/body-images/singleapproach.PNG)

**Note:**  
In  this case, one way is not specificly better then the other. It can help for bigger system to populate parameter dynamicly without the need to take care of additional nodes and connections.

**Thats all I have for you today, but more is to come. I'm pretty sure.**

---

[article]: https://derivative.ca/community-post/python-tipsntricks
