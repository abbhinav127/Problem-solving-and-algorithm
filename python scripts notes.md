

```python
package:
    It is a collection f python programmes
module:
    python scripts
    
```


```python
from pythonscripts.test9 import  factorial
factorial(5)
```




    120




```python
from pythonscripts.strings.stringfunction import alternateCharacters as ac
ac('python')
```




    'pto'




```python
#import math(library name)

```


```python
type(123.4555)
```




    float



# Regular Expressions:



0123456789
[0-9]
[a-z] set of all char from lower case from a to z
s* next follows the alphabets



```python
for i in [0-9]:
    print(i)## it will print only last value from the set

```

    -9
    


```python
for i in [o:9]:
    
```


```python
import re

#pattern ='^gmail$'
#pattern ='^g....'
pattern ='^[a-z]{0,9}$'#[a-z] it represents only one character# {} it represents the twice of [a-z] if $ is present#to represents 5 characters then {3,9}
#in this 9 exclsive so it will have only 8 characters
domain = 'gmail'

if re.match(pattern,domain):
    print('match')
else:
        print('no match')
    
```

    match
    


```python
import re
Pattern='^[1-9][0-9]{5}$'

code='100006'

if re.match(Pattern,code):
    print('match')
else:
    print("not match")


```

    match
    


```python
import re
pattern='^[0-9][0-9]{5,9}[@][a-z]{5}[.][a-z]{2,3}'
email='2210416127@gitam.in'
if re.match(pattern,email):
    print('match')
else:
    print('not match')
```

    match
    


```python
password validation:
    one upper case length(6,21)
    one special character
    start with uppercase or lowercase
    contain digits atleast 1
    
    
```


```python
import re
pattern="^[a-z][a-z]{6,20}[0-9]{1}[!@#$%^&*]{1}[A-Z]{1}$"
password='abbhinav1@A'
if re.match(pattern,password):
    print('match')
else:
    print('not match')
```

    match
    


```python
iteration:
    defination isrepetition
    
it is in Lists,Tuples,Strings

```


```python
li=[1,2,3,4,5,6,7,8,9]

type(li)
it =iter(li)
type(it)
next(it)dfghjkl;

```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-121-13a40a2899b1> in <module>
          5 type(it)
          6 next(it)
    ----> 7 it=it + 1
    

    TypeError: unsupported operand type(s) for +: 'list_iterator' and 'int'


# Generators


```python
li=[i**2 for i in range(1,10)]
li#for square of numbers in the rangfe of 1,10

sum(li)
```




    285




```python
li=[i**2 for i in range(1,10)]
li#for square of numbers in the rangfe of 1,10

gn=(i**2 for i in range(1,11))

for i in gn:
    print(i,end ='             ')
```

    1             4             9             16             25             36             49             64             81             100             

# Functional Programming



```python
map(func, 1)
def func
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-138-58c3bede1e11> in <module>
    ----> 1 map(func, 1)
          2 func=10
    

    NameError: name 'func' is not defined

