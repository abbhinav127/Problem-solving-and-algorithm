
# Problem solving and Programming

## Day 12

## Date: 10 May 2019

## Problem 12

## Problem Statement:
Design a flowchart to evaluate the polynomial
f(x)= x^3 + 2 X^2 + 3 X - 10 for x in the range [1, 1000]

## Test Cases:
f(x)= x^3 + 2 X^2 + 3 X - 10 for x in the range [1, 1000]



```python
def randomGenerator(x):
    return (x^3 + 2*x^2 + 3*x -10)
randomGenerator(5)    

   

            
```




    15



## Problem 13

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



## Problem 14

## Problem Statement:
Procedure to check if a given number is a Perfect Number. ( Perfect number is a number for which the sum of all it's divisors is equal to the number itself)

## constarints

## Test Cases:
* IsPerfect(3) -> False
* IsPerfect (6) -> True  
 

def  perfectNumber(n):
    sum=0
    for i in range(1,n):
         if(n%i==0): 
            sum=sum+i
            if (n==sum):
            return True
        return False
        
        

        
perfectNumber(6)   

## Problem 15

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
    

# Problem 16

## Problem Statement:
Procedure to generate multiplication tables. MT(3, 5, 7) -> 3 X 5 = 15 3 X 6 = 18 3 X 7 = 21

## Constraints:

## Test Cases:
MT(3, 5, 7) -> 3 X 5 = 15 3 X 6 = 18 3 X 7 = 21



```python
def mt(n,lb,ub):
    
    for i in range(lb,ub+1):
        
            a=n*lb
            print(n,"x",lb,"=",a)
            lb=lb +1
            
             
            
mt(3,5,8)            
    
    
```

    3 x 5 = 15
    3 x 6 = 18
    3 x 7 = 21
    3 x 8 = 24
    

# Problem 17

# Problem Statement:
 Procedure to count the number of digits in a given number.


# Constraints:

# Test Cases:
CountDigits(123456) -> 6 CountDigits (0) -> 1


```python

def fun(n):
    
    a=len(str(n))
    return (a)
fun(1232345678987654323456787)    
```




    25



# Problem 18

# Problem Statement:
Given 2 ints, a and b, return True if one if them is 10 or if their sum is 10.

# Constraints:


# Test Cases:
* makes10(9, 10) → True
* makes10(9, 9) → False
* makes10(1, 9) → True


```python
def fun(lb,ub):
    a=10
    sum=lb + ub
    if(sum==10 or lb==10 or ub==10):
        
        return True
    else:
        return False 
print(fun(9,10))
print(fun(9,9))
print(fun(1,9))
```

    True
    False
    True
    

# Problem 19

## Problem Statement:
Given an int n, return True if it is within 10 of 100 or 200. Note: abs(num) computes the absolute value of a number.


## Constraints:

## Test Cases:
* near_hundred(93) → True
* near_hundred(90) → True
* near_hundred(89) → False


```python
def absNum(n):
    if((n>=90 and n<=110) or (n<=200 and n>=190)):
        print(True)
    else:
        print(False)
print(absNum(93))
print(absNum(90))
print(absNum(89))
```

    True
    None
    True
    None
    False
    None
    

# Problem 20

## Problem Statement:
Procedure to generate the first N perfect numbers. GeneratePerfect(2) 

## Constraints


## Test Cases:
* GeneratePerfect(2) -> 6 28 
* GeneratePerfect (4) -> 6 28 496 8128


```python
def gp(n):
    n=[]
    sum=1
    for i in range(0,len(n)):
        if(n%sum==0):
            sum=sum + i
            
            print(sum)
            
n=[2]        
gp(6)        
```

# Problem 21

## Problem Statement:
Design a procedure to determine the frequency count of numbers in a given list

## Constraints:

## Test Cases:
Frequency( a[1,3,2,1] ) -> 1 : 2, 2 : 1, 3 : 1


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
