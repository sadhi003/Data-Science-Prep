## 2. Variables and Types.
It is worthwhile to read the major difference of python with other programming language. Below links provide some ideas about this.
* https://www.educba.com/python-vs-c-plus-plus/
* https://www.geeksforgeeks.org/difference-between-c-and-python/
* https://www.python.org/doc/essays/comparisons/

The main difference can also be seen in the variables definition. As an example, for `c++`, the variables required to define before it's implementation. On the other hand, in python, it is not necessary to define variables beforehand. 

### Numeric
In python mostly there are two types of numerical variables, *int* and *float*. They are defined as,

``` 
  #integer 
  a = 8
  print a

  # float
  b = 8.7
  print b
  # different way float definition
  c = (float) 9
  print c
```

### String
   String variables are defined using single quote or double quote, such as,
  ```
    first_name = 'jack'
    last_name = "rancher"
    print first_name +" " + last_name 
```

 ***Check variable type***
` type(variable name) `


## 3. Basic Operator
Just like other programming language, `python` use same athematic operators such as `+`,`-`,`*`,`/`, `%`, `**`, `//`. Some of these act over numeric variable, some act over both numeric and string, and some act on both string and numeric together. 

```
# Try this out

sum_mul = 1+9*15/3

# module
remainder = 17%2
print (remainder)

# string with numeric, try and find error. 
print ("my name is " + "jack")
print ("Jack is " + 12 + "years old.")
print ("Jack"*3)
print (3**5)
print ("Jack age is " + "12 years.")

# integer division; gives integer only by truncating the remainder part

print ("integer is ", 5//2)
```
`%` operator can be use as formatting operator in the string. For example,
```
TH1F *h = new TH1F("h","histogram of energy higher than %f energy" %(3.5), 100, 2, 5)

# add multiple variable

e1 = 3
e2 = 5
TH1F *h = new TH1F("h","histogram of energy between %d and %d" %(e1,e2), 100, 2, 5)

# add name of histogram in string
name = histogram
e1 = 3
e2 = 5
TH1F *h = new TH1F("h","%s of energy between %d and %d" %(name,e1,e2), 100, 2, 5)

%f -> floating point numbers
%d -> integers
%s -> String or any object with a string representation

```

## 4. Control Structure

### Iteration with Loop
Iteration in python can be done with several options, such as `for`, `while`. A `for` loop can be used to iterate over `list` or `dictionary` (these are python data structure; more details will be included later). In contrast to other programming language, such as `c++`, a `for` loop does not require the initialization of a variable. A variable *i* is initialized and incremented in `c++` but the looping in python act as `for-each`, no need to any initialization and incrementation. For example,

```
# ex:1, for loop
name_list = ['Jack', 'Narvig', 'Katy', 'Honey']
for name in name_list:
    print name

# ex:2, for loop
roll_no= [7,9,13,45,34]
for ii in range(len(roll_no)):
     print roll_no[ii]

"** range **: is a python function, that acts as (a,b,1). Take values from a to b with increment 1. "
``` 

A `while` loop is another way to iterate in python. 
```
# example
j = 0
while (j < 10):
    print j
    j += 1 # increment is very important in while loop. Without this it will run forever.
``` 


### Conditional Statement
Conditional statement mostly use boolean login, `true` or `false` to help guide our decision process. The statement are structure using comparison operators like, `>`, `<`, `>=`, `<=`, `==`. And the conditional statement in control flow is accomplished using keywords such as `if`, `elif`, `else` in python. How to use these, presented in the following examples.

```
num = 5

if num<5:
   print "the number is smaller than 5"
elif num == 5:   # elif is short for else if, that is used in `c++`
   print "the number is equal to 5."
else:
   print "the number is greater than 5"

# if statement are more than two use `elif`, rather in general use `if` and `else`. 


``` 
Boolean data type in python are `True` and `False`. Boolean data type comes with boolean operator(logical), `or`, `and`, `not` in addition to relational operator (above).

```
name = false

if (name is True):
    print ("true statement")
else:
   print ("false statement")

```
**Be careful python is case sensitive programming language as like `c++` or `java`**




## 5. Function
Writing a function in python requires a declaration as `def`, that take one or more arguments and a `return`, that returns one or more values. Not like in other programming language, in python it is not necessary to provide data type of the return values. 

```
def name(first, last):
   return (first + last)

print name("Johnny", " Wright")

def twoNumber(a,b):
    return a,b
print twoNumber(5,6)


```

### Lambda function
Lambda function is often called anonymous function, because this function are defined without any name of the function. The general syntax of lambda function is

```
lambda argument: expression

```
Lambda function can have any number of arguments, but it should have only one expression. An example of lambda function,

```
square = lambda x: x*x

print (square(7))

```
In python lambda function are used when we need function for short period of time. For instance, lambda function are used to pass argument to the function. Lets implement this statement. 

```
def functionTest(y):
    return (lambda x: x*y)

result = function(4)

print (result(3))

```






## 6. Collection

In python there a number of powerful built-in collection classes. Some of those are ordered such as List, tuple and strings. Whereas some are unordered such as sets and dictionaries. 


### List
In python list are written as square brackets `[]`. All the items within list are delimited with commas. For python, list can be created using any data type together or separately. For example, a python list is `[4, 5.5, True, "jack"]`, is possible. Some basic operation that can be done in python are listed below.

```
dataList = ["jack", "freezy", "romeo", 6.5, 5.2, 6, True, False, True] 
# indexing 
dataList[3] 

# concatenate

list1 = ["jack", "freezy", "romeo"]
list2 = [6.5, 5.2, 6, True, False, True] 
dataList = list1 + list2

# length
len(dataList)

# looping
for item in dataList:
    print item

# slicing

dataList[1:4], this gives all items from index 1 to 3 excluding 4. 

# range
list(range(4))
list(range(5,20))

list(range(0,35,5))

```

Beside these there are other methods that list also supports. Such as,
```
append, insert, pop, sort, reverse, del, index, count, remove
``` 

### Strings
Strings are collection of characters. In python string are assigned using quotation mark (either double or single). 

``` 
my_string = "MyName"

print (my_string[2])

```

Since string is a sequence of character, all the basic method that used for list can also be applied to this. 

``` 
print len(my_string)
```
Some other important method acts on strings are,

```
split, upper, lower, find

# some application 

my_statement = " I am proud to be a "

my_statement = my_statement.split(); if we are not giving splitting point, the method split from space. 
print (len(my_statement))
```

Strings are similar in some sense with list, but the main difference is, these are immutable while list are mutable. Mutable means, any item of list can be changed while processing. But in string we can not do that. That's why method like append can not be used.  


## Array

Do we have array in python? The answer is yes, and the initialization of array in python require to be declared. For example,

```
from numpy import array
a = [1,2,5,8] # list
b = array(a) # array
```
So, in contrast to `list` which came out of nowhere in python (inbuilt method), `array` need to be called from package named `numpy`. Here are some similarity and difference between `list` and `array`.
Similarity;

* Data stored in the similar way within square bracket, and the iteration process is same. 
* Indexing is similar as well as slicing. 
* Both data types are mutable. 

Difference;

* Array stored data in more compact way than list. 
* I would say the main difference is, in array we can use athematic operation but not in list. For example,

```
# Try It Yourself
a = [2,4,6]
b = array(a)

print (b/2)
print (a/2)

``` 
The output of array is another array with divided result whereas list spit out an error. In more detail, we will cover during the numpy discussion.  



## Tuple
In python tuple is similar to list, the only difference is tuple are immutable, while list are mutable. In general, the tuples are created using parenthesis `( )`, where the elements in it are separated by commas. The following examples shows other possible representation of tuples. 

```

my_tuple1 = (3, "double", 8.5, "wrong")

#packing method
my_tuple2 = "right", 3, 6.7, "?"
 
#unpack
a , b ,c, d = my_tuple2

# single element
my_tuple3 = (4,)

# more definition 
my_tuple4 = ([1,2,3], "crazy",("nuts", 3, 5.6))
# indexing +ve and -ve
print (my_tuple4[0][1])
print (my_tuple4[-1][0])
```

Possible function that is applicable for tuple as of list are `count`, `find`. At the end, the question is why tuple, since we have list? The greater strength of tuple is immutable. Think how you can explain advantages of tuple over list, based on this property. 


### Dictionary 

As naming, the python dictionary is arrange in the key, value structure. Where a unique key could have same or different values. The key must be immutable datatype whereas value does not care. Example of definition,

```
my_dict = {key: value}

# with data 
my_dict1 = {'ram':2, 'shyam':3}
# another initialization
my_dict2 = dict([(2,"hero"), (3,6)])
# how to get value; require key

print (my_dict1['ram'])  
print (my_dict1.get('ram'))

# want to add element in previously existed dictionary

my_dict1['hari'] = 4

# another way to look the key in dictionary is get function
my_dict1.get('hari')

# lets do a for looping to create dictionary

my_dict3 = {}

for ii in range(2,12,2): 
    my_dict3[ii]=ii*ii

```

Lets make more complicated dictionary

``` 
animal = {'dog':
              {'type':'pet','leg':4,'size':'middle'},
           'frog':
              {'type':'amphi','leg':4,'size':'small'},
            'bird':
              {'type':'fly','leg':2,'size':'small'}}

print (animal['dog'][1])

# add another property in dictionary
animal['dog']['height']='medium'
animal['bird']['height']='tiny'

```

             


### Set

A set is a data type for mutable unordered collections of unique elements. One application of a set is to quickly remove duplicates from a list. For example, 

```
list1 = [1,7,3,2,4,2,9,2]
print (set(list1))
```

As like list, new element can be added to list, but the method is not append but is `add`. 
```
list1.add(99)
```
Since set is mutable, we can use `pop` method. Due to unordered structure of set, `pop` gives a random value rather than the last item as in the case of list. 

Set can be used to operate the mathematical operation done such as union, intersection and so on. 




