
# Problem Solving and Programming

## Day 11

### Date:9 May 2019

### Problem 1:

#### Problem Statement: Even or Odd


```python
n1=int(input("enter any number"))
if(n1 % 2==0):
    print("even")
else:
    print("odd")

```

### Problem 2:

#### Problem Statement:check divisibilty


```python
def checkdivisibilty(n1):
    if(n1%2==0 and n1%3==0 and n1%4!=0):
        print("true")
    else:
        print("false")
checkdivisibilty(27)        
```

    false
    

## Problem 3:

### Problem Statement:Random Numbers

### Test Cases
* RandomGenerator(1,100)


```python
import random

def randomGenerator(lb,ub):
    return random.randrange(lb+1,ub)
    
randomGenerator(1,101)    
```




    3



### Problem 4:


## Problem statement: 
Given an integer N,calculate the random numbers in the range (0,100000000000000)


```python
import random

def sumRandomNumbers(n,lb,ub) :
    sum =0
    for count in range(1, n+1):
        sum = sum + random.randint(lb,ub)
    return sum

sumRandomNumbers(100,0,1000000000000000)
```




    52058463361783243



## Problem 5:

## Problem Statement:Factorial


```python
def factorialnumber(n):
    c=1
    fact=1
    for c in range(1,n+1):
         fact=fact * c
    return fact 
        
factorialnumber(5)        

    
    
    
```




    120



### Problem 6:

### Problem Statement: Linear Search
Design a procedure to perform Linear search on list of N unsorted unique numbers it take and array and the key element to be searched and returns the index of the element of key element if found.Else returns -1


### Constraints:

### Test cases
* Linearsearch([1,4,8,0,3,5,6],3) 4
* linearsearch([15,12,9,6,3,-3],0) -1
* linearsearch([321,456,789,123],789) 2


```python

def linearsearch(a,key):
    for i in range(0,len(a)):
        if(a[i] == key):
            return i
    return -1
linearsearch([15,12,9,6,3,-3],0)
linearsearch([321,456,789,123],789)
```




    2



### Problem 7

### Problem Statement:Factors


```python
def factorlist(n):
    i=1
    for i in range(1,n + 1):
        if(n%i)==0:
            print(i)
         
factorlist(20)    

```

    1
    2
    4
    5
    10
    20
    

### Problem 8:

### Problem Statement:prime number


```python
def primenumber(n):
    i=2
    for i in range(2,n):
        if(n%i==0):
            return(n,"it is prime")
        else:
            return(n,"it is not prime")
            

primenumber(27)
           
               
```




    (27, 'it is not prime')



### Problem 9:

### Problem Statement:Palindrome


```python
def palindrome(n):
    rn=n[-1::-1]
    if(n==rn):
        return True
    return False
    
palindrome("rsdgjk")    
```




    False



### Problem 10:

### Problem Statement: Natural numbers


```python
def naturalnumbers(n):
    for i in range(1,n + 1):
        print(i)
naturalnumbers(30)        
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    11
    12
    13
    14
    15
    16
    17
    18
    19
    20
    21
    22
    23
    24
    25
    26
    27
    28
    29
    30
    

## Problem 11:

## Problem Statement:Square Root


```python
def squareroot(n):
    return n**0.5
    
    

squareroot(36)
```




    6.0


