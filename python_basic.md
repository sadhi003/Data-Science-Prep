Welcome to the Python_tutorial wiki!
# Topics
## 1. Introduction
**How to execute a simple python command?**

Open your terminal and type python, it provides an interactive python environment. Start typing whatever you are familiar with. As an example, type `print "Hello World"`. And this command work if you have python version `< 3`. For python version `>= 3`, you have to include parenthesis, such as, `python ("Hello World")`. Caveat: this tutorial will follow the syntax for python version `2.7`. 

**Python from Anaconda**

For this tutorial, I would strongly recommend you to install a different version of python using **Anaconda**. [Here is how you can do it](https://docs.anaconda.com/anaconda/install/). 

After an installation of anaconda, `conda` environment is accessible. Future part of tutorial would require more packages to install. So, it is better to create an environment and work on that. [How to create environment is available here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html).

 

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


