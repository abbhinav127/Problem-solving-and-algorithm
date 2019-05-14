
# Recursion
fuction calling itself


breaking a complex problems into a sub problems of lower complexity.Keep repreating this process until we reach the smallest possible subproblems to which we known the solution.


# EXAMPLES:
power of a number
factorial
GCD
Towers of Hanoi
Binary search
Merge search
Fibonacii series

n ^ r

for(i=1 ; i<=r; i++)
    prod =




```python

```

### Recursive Power


```python
def recursivePower(n,r):
    if r == 1:
        return n
    else:
         return recursivePower(n, r-1) * n
        
recursivePower(2,3)        
```




    8



### iteration


```python
def power(n,r):
    prod =1
    for i in range(1,r + 1):
        prod*=n
    return prod

power(2,10)
```




    1024



## Factorial


```python
def factorial(n,r):
    if r==1:
        return n
    else:
        return n*factorial(n-1)

    

```

    enter a number:720
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-169-086a39b37e81> in <module>
         10     print("factorial of 0 is 1")
         11 else:
    ---> 12     print("The factorial of",num,"is",factorial(num))
         13 factorial(3,4)
         14 
    

    TypeError: factorial() missing 1 required positional argument: 'r'


# Problem GCD


```python
def gcd(a,b):
    if(b%a)==0:
        return a
    else:
        return gcd(b%a,a)
gcd (40,10)   
```




    10



# Problem Fibnoic series


```python
def fs(n):
    if(n==1):
        return 0
    if(n==2):
        return 1
    else:
        return fs(n-1)+fs(n-2)
    
fs(10)    
```




    34



# Problem: Towers of Hanoi


```python
def toh(n,s,t,d):
    if(n==1):
        print('move disk',n,'from',s,'to',d)
    else:
        (n-1,s,t,d)
        print('move',n,'disk from',s,'to,d')
        toh(n-1,s,t,d)
        return
toh(5,'a','b','c')   
```

    move 5 disk from a to,d
    move 4 disk from a to,d
    move 3 disk from a to,d
    move 2 disk from a to,d
    move disk 1 from a to c
    

## Problem 1

## Problem Statement:
Define a function to check if a given year is a leap year. Returns a boolean value

### Constraints:

### Test Cases:
* 2000 -> True
* 1900 -> False
* 2012 -> True
* 2020 -> True
* 0200 -> False


```python
def leapyear(n):
    if(n%4==0 and n%100!=0 or n%400==0): 
        return True
    else:
        return False
    
    
                
print(leapyear(2000))
print(leapyear(1900))
print(leapyear(2012))
print(leapyear(2020))
print(leapyear(200))
```

    True
    False
    True
    True
    False
    

# Problem 2:


## Problem Statement:
 Define a function to convert a decimal number to the corresponding binary number

## Constraints:

## Test Cases:
* decimalToBinary(15) -> 1111
* decimalToBinary(1) -> 1


```python
def decimaltoBinary(n):
    if n>1:
        decimaltoBinary(n//2)
    print(n%2,end='')    
    
            
(decimaltoBinary(15))

        
    
    
    
```

    1111

# Problem 3

## Problem Statement:
Define a function to convert a binary number to the corresponding decimal number

### Constraints:

## Test Cases:
* binaryToDecimal(1100) -> 12
* binaryToDecimal(1010) -> 10
* binaryToDecimal(111000) -> 56


```python
 def binarytoDecimal(n):
        add=0
        i=0
        while n>0:
            m=n%10
            add=add+m*2**i
            n=int(n/10)
            i=i+1
        return add    
print(binarytoDecimal(1100))
print(binarytoDecimal(1010))
print(binarytoDecimal(111000))
```

    12
    10
    56
    

# Problem 4:

## Problem Statement:
Design a Python script to determine the difference in date for given two dates in YYYY:MM:DD format(0 <= YYYY <= 9999, 1 <= MM <= 12, 1 <= DD <= 31) following the leap year rules. Return the total number of days existing between the two dates.

### Constraints:


### Test Cases:
* dateDifference('2019:05:10', '2019:05:01') -> 9
* dateDifference('0003:03:03', '0003:06:06') -> 95


```python
def dd(str1,str2):

def numDaysInMonth(month):
    monthDays ={'01':31,'03':31,'04':30,'05':31,'06':30,'07':31,'08':31,'09':30,'10':31,'11':30,'12':31}
    if
        
            
        
```


      File "<ipython-input-217-06c00e485e6d>", line 3
        def numDaysInMonth(month):
          ^
    IndentationError: expected an indented block
    


# Problem 5:

## Problem Statement:
 Define a function to find the average of all the outer elements of an N x M matrix.

### constraints:

### Test Cases:
averageOuterMatrix([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]] -> 4.5


```python

```

# Problem 6:

## Problem Statement:
 Define a function to print the sequence of spiral pattern elements for a given N x N matrix

### Constraints:

### Test Cases:
* spiralPattern([[1,2,3], [4,5,6], [7,8,9]]) -> 1 2 3 6 9 8 7 4 5



```python
def spiralpattern(n):
    a=len(n)
    for i in range(0,len(n)):
        if (len[1]==len[2]):
            print(a)
        else:
                b=len(n)
        
            
        
            
            
spiralpattern([[1,2,3],[4,5,6],[7,8,9]])            
            
        
        
    
    
    

```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-209-03770092b5f8> in <module>
         11 
         12 
    ---> 13 spiralpattern([[1,2,3],[4,5,6],[7,8,9]])
         14 
         15 
    

    <ipython-input-209-03770092b5f8> in spiralpattern(n)
          2     a=len(n)
          3     for i in range(0,len(n)):
    ----> 4         if (len[1]==len[2]):
          5             print(a)
          6         else:
    

    TypeError: 'builtin_function_or_method' object is not subscriptable


# Problem 7:

## Problem Statement:
Define a function to identity the number of times a substring is repeating in a given string

## Constraints:

## Test Cases:
* substringCount('str', 'substr') -> 1
* substringCount('1234567891122334455', '3') -> 3
* substringCount('abccddccc', 'cc') -> 3
* substringCount('aaaaaaa', 'aaa' ) -> 5


```python
def substring(str1,str2):
    count=0
    if(len(str1)>len(str2)):
        a=str1
        b=str2
    else:
        a=str2
        b=str1
    for i in range(len(a)):
        if b in  a[i:i + len(b)]:
            count=count+1
    return count
print(substring('str','substr'))
print(substring('1234567891122334455','3'))
print(substring('abccddccc','cc'))
print(substring('aaaaaaa','aaa'))
    
```

    1
    3
    3
    5
    

# Problem 8:

## Problem Statement:
Define a function to merge the characters of two strings alternatively. The remaining characters
of the longer string are printed in the same order at the end.

## constraints:


## Test Cases:
* mergeString('abcd', 'abcd') -> 'aabbccdd'
* mergeString('abc', '123456') -> 'a1b2c3456'
* mergeString('0', '123456') -> '0123456'


```python
def mergestring(str1,str2):
    if len(str1)<len(str2):
        small=str1       
    else:
        small=str2        
        for i in range(0,len(small)):
            print(str1[i]+str2[i],end="")
        j=len(small)
        if str1==small:
            while j<len(str2):
                print(str2[j],end="")
                j=j+1
            else:
                while j<len(str1):
                    print(str1[j],end="")
                    j=j+1

mergestring('abcd','abcd')

                       
        
```

    aabbccdd


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
