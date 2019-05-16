

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


# Date:16 may 2019
# Day:18


# Problem 1:
# Problem Statement:
define function to read data from a text file
# Test Cases:


```python
def readFileData(filename):
    with open(filename,'r') as f:
        f=open(filename,'r')
    ##filedata=f.readline()   #it will read only first line
        filedata = f.read()         #it will read entire lines
    ##filedata +=f.readline()  #it will read the second line
    ##f.close()
    return filedata

readFileData('Data files/datafile.txt')
```




    'Data in line1 Data in line2 Data in line3'




```python
def readFileData(filename):
    with open(filename,'r') as f:
        #for line in f:
           # print(line,end=' ')
            print(f.read())   
    return


def writeIntoFile(filename,data,mode):  ### it is to create a new text file in old folder and adding a data.This works by this method   
    ##with open(filename,'w') as f:
    with open(filename,mode) as f:
        f.write(data) # f as filehandling
    return     
writeIntoFile('Data Files/writefile.txt','01' , 'a')  ## it is for the append a extra line in the new line
```


```python
from random import randrange
def writeIntoFile(filename):
    with open(filename,'w') as f:
        for i in range(1,1301):
            f.write(str(randrange(0,101)))
            f.write('\n')
            
        
    return
writeIntoFile('Data Files/marksfile.txt') # write the data ghgj
```

# Problem 2:
# Problem Statement:
Define a function to generate a Marks datafile(text) from 1300 students such that each marks is entered in a new linw.Marks range from 0 to 100(inclusive) as random numbers

# Problem 3:
# Problem Statement:
generate a report on the marks data with the following indicators
* Highest Marks
* lowest Marks
* average Marks
* no of students with distinction(>80):
* no of students with first class(>60): 
* no of students with second class(>50):
* no of students with third class(>40):
* no of students with failed(<40):
        


```python
from random import randrange
def readFileData(filename):
    with open(filename,'r') as f:
         f=open(filename,'r')
    filedata=f.readline()   #it will read only first line
    filedata = f.read()     
def writeIntoFile(filename):
    with open(filename,'w') as f:
        count=0
        for i in range(1,1301):
            
            f.write(str(randrange(0,101)))
            f.write('\n')
        for i in range(0,101):
            if(100<80):
                count=count + 1
                return count
            ##f.write('distinction'=+str(count)+'\n')
                
            
            f.write(str())
                
                
writeIntoFile('Data Files/marksfile.txt')
```

aavvvvv




```python
def square(n):
    return n*n
li=[1,2,3,4,5,6]
s=list(map(str,li))
s
```




    ['1', '2', '3', '4', '5', '6']




```python
import timeit
def square(n):
    return n*n
st=timeit.default_timer()
li=[1,2,3,4,5,6]
s=list(map(str,li))
s
s=[float(i) for i in s]
print(timeit.default_timer()-st)
s
```

    9.557300018059323e-05
    




    [1.0, 2.0, 3.0, 4.0, 5.0, 6.0]




```python
import timeit
def square(n):
    return n*n
st=timeit.default_timer()
li=[1,2,3,4,5,6]
s=list(map(str,li))
s
s=[float(i) for i in s]
print(timeit.default_timer()-st)
s
```

    9.671099996921839e-05
    




    [1.0, 2.0, 3.0, 4.0, 5.0, 6.0]




```python
import timeit
def square(n):
    return n*n
st=timeit.default_timer()
li=[1,2,3,4,5,6]
s=list(map(str,li))
s
s=[float(i) for i in s]
print(timeit.default_timer()-st)
s
def distinction(marks):
    return marks >=80


dis = sum(map(distinction,maksdata))


failed = sum([1 for i in  marksdata if i < 40 ])
failed



          
    
```

    9.727999986353097e-05
    


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-28-a17372053fa8> in <module>
         13 
         14 
    ---> 15 dis = sum(map(distinction,maksdata))
         16 
         17 
    

    NameError: name 'maksdata' is not defined


# LIBRARIES:
WEBSITE CALLED SCIPY.ORG


```python
matrix is by numpy
```


```python
#tensor
tensor it will join n matrixs into one list
```


      File "<ipython-input-29-2340707fad2d>", line 2
        tensor it will join n matrixs into one list
                ^
    SyntaxError: invalid syntax
    


# Pandas


```python

```
