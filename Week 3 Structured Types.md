## 1. Tuples


* Tuples: an ordered sequence of elements, can mix element types, _**Immutable**_, represented with parenthese


```python
tup = ()

t = (2, 'haha', 3)

t + (4, 5)  #evalutes to (2, 'haha', 3, 4, 5)

t[0:1] #evalutes to (2,)   

t [1] = 2 # error 
```

* Conveniently used to **swap** variable values

```python
temp = x
x = y
y = temp 

#or
(x, y) = (y, x)

#return more than one variable from a function

def quotient_and_remainder(x, y):
      q = x//y
       r = x%y
      return(q, r)
(quot, rem) = quotient_and_remainder(4,5)
```

* Can **Iterate over tuples:**

```python
def get_data(aTuple):
     nums= ()
     words = ()
     for t in aTuple:
          nums= nums+ (t[0],)
          if t[1] not in words:
                 words = words + (t[1],)
     min_nums= min(nums)
     max_nums= max(nums)
     unique_words= len(words)
     return(min_nums, max_nums, unique_words)
```
 
2. Lists

+ An ordered sequenceof information, accessible by index, denoted by square brackets,  [ ]
Contains elemtns that usually are homogenous (can contain mixed types) 
**_mutable _**
* Iterating over a list: compute the sum of elements of a list


```python
a_list= []
b_list= [2, 'a', 4, True]

b_list[0]  #evalutes to 2, index can be a variable or expression

b_list[0] = 4 #mutable

#Iteration


total = 0 
 for i in L:
    total += i
 print(total)
 
#remember iteration from 0 to n-1 
```

##3. List Operations


* example
```python
L = [2, 1, 3]
L. append(5) # L is now [2, 1, 3, 5]
```

* The dot in L.append: 
    List are __python objects__, objects have data, methods and functions. 
    Access the information by __object_name.do_something()__
    
```python
L.extend()  #look for the last one and extend it (mutated)

del(L[3]) #delete a specific element

L.pop() #remove elements at the end of list and returns the removed element 
```

+ Convert string to list

```python
# a string s

s = 'a < b'
list(s)
s.split( '<' )   # evaluates to [ 'a ' , 'b'] 

L = [ 'a', 'b', 'c' ]
''. join(L)        #  'abc'
'_'.join(L)       # 'a_b_c' 
```
* Sort the list and reverse
```python
sorted(L)    #descending  = False, does not mutate it
L.sort()      # descending = True
L.reverse   
```

* Bringing together LOOPS, FUNCTIONS, range and LISTS:
    - range is a special procedure and it returns something that behaves like a tuple.
    - range (5)   -> [0,1,2,3,4] tuple
      range (5, 2, -1) -> [5, 4, 3] tuple
    - when use _range_ in a _for_loop, what the loop variable iterates over behaves like a list