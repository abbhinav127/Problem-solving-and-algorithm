
# Problem solving and Programming

## Day 12

## Date: 10 May 2019

## Problem 13

## Problem Statement:
Design a flowchart to evaluate the polynomial
f(x)= x^3 + 2 X^2 + 3 X - 10 for x in the range [1, 1000]

## Test Cases:
f(x)= x^3 + 2 X^2 + 3 X - 10 for x in the range [1, 1000]



```python
def randomGenerator(x):
    if(0<x<1000):
        return (x^3 + 2*x^2 + 3*x -10)
    
randomGenerator(3)    

   

            
```




    11



## Problem 14

## Problem Statement:
Designing procedures for Basic Arithmetic operations

### constraints

### Test Cases:
(+,-,*,%)


```python
def arithmeticoperations(a,b):
    c=a + b
    d=a -b
    e=a*b
    f=a%b
    return c,d,e,f
arithmeticoperations(5,3)
```




    (8, 2, 15, 2)



## Problem 15:

## Problem Statement:
Given an int n, return True if it is within 10 of 100 or 200. Note: abs(num) computes the absolute value of a number.

### Constraints:
n

### Test cases:
* near_hundred(93) → True
* near_hundred(90) → True
* near_hundred(89) → False
* near_hundred(192) → True

def absoluteNumber(n): 
    return (90 <=n <100 or 190<= n <=200)
print("absoluteNumber(93) is",absoluteNumber(93))
print("absoluteNumber(90) is",absoluteNumber(90))
print("absoluteNumber(89) is",absoluteNumber(89))
print("absoluteNumber(192) is",absoluteNumber(192))


## Problem 16

## Problem Statement:
Procedure to check if a given number is a Perfect Number. ( Perfect number is a number for which the sum of all it's divisors is equal to the number itself)

## constarints

## Test Cases:
* IsPerfect(3) -> False
* IsPerfect (6) -> True  
 


```python
def perfectNumber(n):
    
        i=1
        j=2
        for i in range(1,n+1):
            if(n%i)==0:
                print(i)
        for j in range(1,j+1):
            if(n%j)==0:
                print(j)
            
            
             
                
            
perfectNumber(35)       
    
```

    1
    5
    7
    35
    1
    

## Problem 17

## Problem Statement:
Design a procedure calculate the maximum, minimum and average of N numbers

### Constraints:


### Test Cases:
* data( a[1,2,3,4,5] ) -> Max = 5, Min = 1, Avg = 3
* data( a[3,2,5,7,6,5] ) -> Max = 9, Min = 2, Avg = 5.333


```python
def MaxMinAvg(n):
    print("maximum of a is",max(n))
    print("minimum of a is",min(n))
    
    m=1
    for i in range(1,len(n)):
        m=m + n[i]
        print(m/(len(n)))
print(MaxMinAvg([1,2,3,4,5]))
print(MaxMinAvg([3,2,5,7,6,5,9]))
```

    maximum of a is 5
    minimum of a is 1
    0.6
    1.2
    2.0
    3.0
    None
    maximum of a is 9
    minimum of a is 2
    0.42857142857142855
    1.1428571428571428
    2.142857142857143
    3.0
    3.7142857142857144
    5.0
    None
    


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
