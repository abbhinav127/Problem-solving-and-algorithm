
# Problem 1:
    

## Problem Statement:
You are given n words. Some words may repeat. For each word, output its number of occurrences. The output order should correspond with the input order of appearance of the word. 
First line of input contains the total number of words n. Next n lines contain words that need to processed.
First line of the output should contain the total number distinct words. Second line of output must contain the frequency of words the same order of their appearance as in the input


## Constarint:
* Sample Input : 6
* Sample Output : 3

## Test Cases:

* abcd
* ijkl
* abcd
* pqrs
* abcd
* ijkl
* 3 2 1


```python
def unique(ar):
    u=[]
    for x in ar:
        if x  not in u:
            u.append(x)
    print(len(u),end='\n')
    return u
def wordcount(a):
    u=unique(a)
    for x in u:
        count=0
        for j in range(len(a)):
            if x==a[j]:
                count=count + 1
        print(count,end='')
wordcount(['abcd','lijk','abcd','abcd','pqrs','lijk'])        
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
              
       
    
    
    
```

    3
    321

# Problem 2:


# Problem Statement:
Define a function to validate email addresses based on the following rules.
Email should be in the format username@domain.extension
username must start with an alphabet and can contain lowercase alphabet, digits, hyphen(-) and underscores( _ ).
username must not contain special characters, uppercase letters, whitespaces.
Length of username must be in the range (6, 16)
Domain can only contain lowercase alphabet and digits with length in range (3, 10) . No special characters are allowed
Extension can only contain lower case alphabet and its length must be in the range (2, 4)
First line of input contains total number of email addresses n. Next n lines contain n email addresses.


# Constraints:

# Test Cases:
Sample Input : 6
* abc456@gmail.com
* 456abc@yahoo.com
* abc_456@gitam.ed1
* abc-456@abc-d.in
* python@python.edu
* abc 456@edu.edu
* Sample Output : Valid
* Invalid
* Invalid
* Invalid
* Valid
* Invalid


```python

```

# Problem 3

# Problem Statement:
Define a function that take an array of integers A, and an integer K and returns the longest possible sub-set of A i.e A' such that the sum of no two elements in A' is divisible by K.
First line in input contains the length of A and the integer K. Second line of input contains len(A) space-separated integers.
Output must contain the length of A' list

# Constraints

# Test Cases:
* Sample Input : 4 3
* 1 7 2 4
* Sample Output : 3


```python
def sample(a,k):
     
```
