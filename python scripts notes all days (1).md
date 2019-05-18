

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
    



```python

```

# Pandas

# Problem 1
# Problem Statement:
Define a function to read for a CSV file using Pandas library display the file data as output CSV(comma separated values)


```python
#1
import pandas as pd

def readCSV(filename):
    df = pd.read_csv(filename)
    return df   
df=readCSV('Data Files/income.csv')
#2
df.columns
#3
#for row in df.values:
#    print('GeoID: ', row[0], 'State : ',row[1])------------------------------------------------below data is for accessing data
#df.index[3]
#type(df) #df=data frame . frame:View 
df.head(2) # for first three rows and colums are automatically printed
df.tail(6)# all five
df.iat[3,9]     # it will print the first row and no of column
df.loc[2][0]  # it will print the entire state of data   iat and loc almost both r same

```




    GEOID    04000US01
    State      Alabama
    2005         37150
    2006         37952
    2007         42212
    2008         44476
    2009         39980
    2010         40933
    2011         42590
    2012         43464
    2013         41381
    Name: 0, dtype: object




```python
print("abbhinav")
```

    abbhinav
    

# Problem 2:
# Problem Statement:
adding new data


```python
def addRowCSV(filename,rowdata):
    df = readCSV('Data Files/income.csv')
    df.loc[len(df)] = rowdata
    
    return df
rowdata = ['01010109','statename',1236421521124,12345678,2345679084,7485215,23456789,9876543,45678,123123141,9078558455]
addRowCSV('Data Files/income.csv',rowdata)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-104-ec35366f1237> in <module>
          5     return df
          6 rowdata = ['01010109','statename',1236421521124,12345678,2345679084,7485215,23456789,9876543,45678,123123141,9078558455]
    ----> 7 addRowCSV('Data Files/income.csv',rowdata)
    

    <ipython-input-104-ec35366f1237> in addRowCSV(filename, rowdata)
          1 def addRowCSV(filename,rowdata):
          2     df = readCSV('Data Files/income.csv')
    ----> 3     df.loc[len(df)] = rowdata
          4 
          5     return df
    

    ~\Anaconda3\lib\site-packages\pandas\core\indexing.py in __setitem__(self, key, value)
        188             key = com.apply_if_callable(key, self.obj)
        189         indexer = self._get_setitem_indexer(key)
    --> 190         self._setitem_with_indexer(indexer, value)
        191 
        192     def _validate_key(self, key, axis):
    

    ~\Anaconda3\lib\site-packages\pandas\core\indexing.py in _setitem_with_indexer(self, indexer, value)
        443                         if is_list_like_indexer(value):
        444                             if len(value) != len(self.obj.columns):
    --> 445                                 raise ValueError("cannot set a row with "
        446                                                  "mismatched columns")
        447 
    

    ValueError: cannot set a row with mismatched columns


# Problem 3
# Problem Statement:
define a function to update/modify a row in a csv file 


```python
def updateRowCSV(filename, rowindex, rowdata):
    df = readCSV(filename)
    df.loc[rowindex] = rowdata
    df.to_csv(filename)
    return df
updateRowCSV('Data FILES/income.csv',6,1)
    
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>Unnamed: 0.1</th>
      <th>Unnamed: 0.1.1</th>
      <th>GEOID</th>
      <th>State</th>
      <th>2005</th>
      <th>2006</th>
      <th>2007</th>
      <th>2008</th>
      <th>2009</th>
      <th>2010</th>
      <th>2011</th>
      <th>2012</th>
      <th>2013</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>04000US01</td>
      <td>Alabama</td>
      <td>37150</td>
      <td>37952</td>
      <td>42212</td>
      <td>44476</td>
      <td>39980</td>
      <td>40933</td>
      <td>42590</td>
      <td>43464</td>
      <td>41381</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>04000US02</td>
      <td>Alaska</td>
      <td>55891</td>
      <td>56418</td>
      <td>62993</td>
      <td>63989</td>
      <td>61604</td>
      <td>57848</td>
      <td>57431</td>
      <td>63648</td>
      <td>61137</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>04000US04</td>
      <td>Arizona</td>
      <td>45245</td>
      <td>46657</td>
      <td>47215</td>
      <td>46914</td>
      <td>45739</td>
      <td>46896</td>
      <td>48621</td>
      <td>47044</td>
      <td>50602</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>04000US05</td>
      <td>Arkansas</td>
      <td>36658</td>
      <td>37057</td>
      <td>40795</td>
      <td>39586</td>
      <td>36538</td>
      <td>38587</td>
      <td>41302</td>
      <td>39018</td>
      <td>39919</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>04000US06</td>
      <td>California</td>
      <td>51755</td>
      <td>55319</td>
      <td>55734</td>
      <td>57014</td>
      <td>56134</td>
      <td>54283</td>
      <td>53367</td>
      <td>57020</td>
      <td>57528</td>
    </tr>
    <tr>
      <th>5</th>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>04000US07</td>
      <td>Chicago</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>7</td>
      <td>7</td>
      <td>10101</td>
      <td>statename</td>
      <td>123</td>
      <td>4325</td>
      <td>4565</td>
      <td>9084</td>
      <td>6984</td>
      <td>234</td>
      <td>567</td>
      <td>999</td>
      <td>123</td>
      <td>90</td>
    </tr>
  </tbody>
</table>
</div>




```python
import pandas as pd

def readCSV(filename):
    df = pd.read_csv(filename)
    return df

filename = 'Data Files/income.csv'
df = readCSV(filename)
#df.columns
#df.values[1]
#for row in df.values:
 #   print('GeoID : ', row[0], 'State : ', row[1])


df.tail(5) # Retrieving the last 5 rows
df.head(2) # Retrieving the first 2 rows
df.iat[2, 0] # Accessing the 7th element in the 2nd row

#df = df.drop('Unnamed: 0.1', axis=1)
#df.to_csv('DataFiles/Income.csv', index=False)
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>Unnamed: 0.1</th>
      <th>Unnamed: 0.1.1</th>
      <th>Unnamed: 0.1.1.1</th>
      <th>Unnamed: 0.1.1.1.1</th>
      <th>GEOID</th>
      <th>State</th>
      <th>2005</th>
      <th>2006</th>
      <th>2007</th>
      <th>2008</th>
      <th>2009</th>
      <th>2010</th>
      <th>2011</th>
      <th>2012</th>
      <th>2013</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>04000US01</td>
      <td>Alabama</td>
      <td>37150</td>
      <td>37952</td>
      <td>42212</td>
      <td>44476</td>
      <td>39980</td>
      <td>40933</td>
      <td>42590</td>
      <td>43464</td>
      <td>41381</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>04000US02</td>
      <td>Alaska</td>
      <td>55891</td>
      <td>56418</td>
      <td>62993</td>
      <td>63989</td>
      <td>61604</td>
      <td>57848</td>
      <td>57431</td>
      <td>63648</td>
      <td>61137</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>04000US04</td>
      <td>Arizona</td>
      <td>45245</td>
      <td>46657</td>
      <td>47215</td>
      <td>46914</td>
      <td>45739</td>
      <td>46896</td>
      <td>48621</td>
      <td>47044</td>
      <td>50602</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>04000US05</td>
      <td>Arkansas</td>
      <td>36658</td>
      <td>37057</td>
      <td>40795</td>
      <td>39586</td>
      <td>36538</td>
      <td>38587</td>
      <td>41302</td>
      <td>39018</td>
      <td>39919</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>04000US06</td>
      <td>California</td>
      <td>51755</td>
      <td>55319</td>
      <td>55734</td>
      <td>57014</td>
      <td>56134</td>
      <td>54283</td>
      <td>53367</td>
      <td>57020</td>
      <td>57528</td>
    </tr>
    <tr>
      <th>5</th>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>04000US07</td>
      <td>Chicago</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
      <td>-999</td>
    </tr>
    <tr>
      <th>6</th>
      <td>6</td>
      <td>6</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>7</td>
      <td>7</td>
      <td>7</td>
      <td>7</td>
      <td>10101</td>
      <td>statename</td>
      <td>123</td>
      <td>4325</td>
      <td>4565</td>
      <td>9084</td>
      <td>6984</td>
      <td>234</td>
      <td>567</td>
      <td>999</td>
      <td>123</td>
      <td>90</td>
    </tr>
    <tr>
      <th>8</th>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
    </tr>
  </tbody>
</table>
</div>




```python
def addRowCSV(filename, rowdata):
    df = readCSV(filename) # Get dataframe from CSV
    df.loc[len(df)] = rowdata # Add a row to the dataframe
    df.to_csv(filename, index=False) # Send the dataframe back to CSV
    return df

rowdata = ['010101', 'statename', 123, 4325, 4565, 9084, 83123, 423, 987, 345, 765,678]
addRowCSV('Data Files/income.csv', rowdata)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-109-b8034844c2ad> in <module>
          6 
          7 rowdata = ['010101', 'statename', 123, 4325, 4565, 9084, 83123, 423, 987, 345, 765,678]
    ----> 8 addRowCSV('Data Files/income.csv', rowdata)
    

    <ipython-input-109-b8034844c2ad> in addRowCSV(filename, rowdata)
          1 def addRowCSV(filename, rowdata):
          2     df = readCSV(filename) # Get dataframe from CSV
    ----> 3     df.loc[len(df)] = rowdata # Add a row to the dataframe
          4     df.to_csv(filename, index=False) # Send the dataframe back to CSV
          5     return df
    

    ~\Anaconda3\lib\site-packages\pandas\core\indexing.py in __setitem__(self, key, value)
        188             key = com.apply_if_callable(key, self.obj)
        189         indexer = self._get_setitem_indexer(key)
    --> 190         self._setitem_with_indexer(indexer, value)
        191 
        192     def _validate_key(self, key, axis):
    

    ~\Anaconda3\lib\site-packages\pandas\core\indexing.py in _setitem_with_indexer(self, indexer, value)
        443                         if is_list_like_indexer(value):
        444                             if len(value) != len(self.obj.columns):
    --> 445                                 raise ValueError("cannot set a row with "
        446                                                  "mismatched columns")
        447 
    

    ValueError: cannot set a row with mismatched columns


# Problem 4
# Problem Statement:
Define a function to read for a CSV file using pandas library display the file data as output CSV


```python
def updaterow(filename,rowindex)
```

# Problem 5
# Problem statement:
generate marks of 2000 students in csv file with columns,roll number,marks (add row,


```python
import pandas as pd
def addMarksDataCSV(marksfile,nr,roll):
    df=readCSV(filename)
    df.loc[len(df)]=rowdata
    df.to_csv(filename, index=False) # Send the dataframe back to CSV
    return df
rowdata = ['010101', 'statename', 123, 4325, 4565, 9084, 83123, 423, 987, 345, 765]
addRowCSV('Data Files/roll.csv', rowdata)    
```


    ---------------------------------------------------------------------------

    EmptyDataError                            Traceback (most recent call last)

    <ipython-input-119-ef701d58ea21> in <module>
          6     return df
          7 rowdata = ['010101', 'statename', 123, 4325, 4565, 9084, 83123, 423, 987, 345, 765]
    ----> 8 addRowCSV('Data Files/roll.csv', rowdata)
    

    <ipython-input-109-b8034844c2ad> in addRowCSV(filename, rowdata)
          1 def addRowCSV(filename, rowdata):
    ----> 2     df = readCSV(filename) # Get dataframe from CSV
          3     df.loc[len(df)] = rowdata # Add a row to the dataframe
          4     df.to_csv(filename, index=False) # Send the dataframe back to CSV
          5     return df
    

    <ipython-input-106-68f94c309d44> in readCSV(filename)
          2 
          3 def readCSV(filename):
    ----> 4     df = pd.read_csv(filename)
          5     return df
          6 
    

    ~\Anaconda3\lib\site-packages\pandas\io\parsers.py in parser_f(filepath_or_buffer, sep, delimiter, header, names, index_col, usecols, squeeze, prefix, mangle_dupe_cols, dtype, engine, converters, true_values, false_values, skipinitialspace, skiprows, skipfooter, nrows, na_values, keep_default_na, na_filter, verbose, skip_blank_lines, parse_dates, infer_datetime_format, keep_date_col, date_parser, dayfirst, iterator, chunksize, compression, thousands, decimal, lineterminator, quotechar, quoting, doublequote, escapechar, comment, encoding, dialect, tupleize_cols, error_bad_lines, warn_bad_lines, delim_whitespace, low_memory, memory_map, float_precision)
        700                     skip_blank_lines=skip_blank_lines)
        701 
    --> 702         return _read(filepath_or_buffer, kwds)
        703 
        704     parser_f.__name__ = name
    

    ~\Anaconda3\lib\site-packages\pandas\io\parsers.py in _read(filepath_or_buffer, kwds)
        427 
        428     # Create the parser.
    --> 429     parser = TextFileReader(filepath_or_buffer, **kwds)
        430 
        431     if chunksize or iterator:
    

    ~\Anaconda3\lib\site-packages\pandas\io\parsers.py in __init__(self, f, engine, **kwds)
        893             self.options['has_index_names'] = kwds['has_index_names']
        894 
    --> 895         self._make_engine(self.engine)
        896 
        897     def close(self):
    

    ~\Anaconda3\lib\site-packages\pandas\io\parsers.py in _make_engine(self, engine)
       1120     def _make_engine(self, engine='c'):
       1121         if engine == 'c':
    -> 1122             self._engine = CParserWrapper(self.f, **self.options)
       1123         else:
       1124             if engine == 'python':
    

    ~\Anaconda3\lib\site-packages\pandas\io\parsers.py in __init__(self, src, **kwds)
       1851         kwds['usecols'] = self.usecols
       1852 
    -> 1853         self._reader = parsers.TextReader(src, **kwds)
       1854         self.unnamed_cols = self._reader.unnamed_cols
       1855 
    

    pandas/_libs/parsers.pyx in pandas._libs.parsers.TextReader.__cinit__()
    

    EmptyDataError: No columns to parse from file



```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```
