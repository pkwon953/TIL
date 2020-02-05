# **Python_Basic**

Basic defined functions in python

* assert - In general, we use 'if' and 'Except' phrases in python. In the same meaning we can use 'assert' . 

Basic Grammar of assert

> ```python
> assert condition, 'message' 
> # if the condition is True in all circumstances,returns None.
> # if one of them is False returns Assertion Error which is kin of safe code.  
> ```

Basic Grammar of split & sep

> ```python
> data.split('splitter') #splits data with the known splitter
> os.path.sep #splits automatically
> ```

* zip - To concatenate two different data zip function comes in handy.

> ```python
> a = list(zip([1,1],[2,2]))
> # To see the zipped data after using zip function convert the data type to list or tuple. If not, type will be printed
> ```

* get - Used function in dictionary data. Returns value from the insisted key.

> ```python
> car = {
>   "brand": "Ford",
>   "model": "Mustang",
>   "year": 1964
> }
> x= car.get('model')
> #value for model which the value is Mustang will be printed
> ```

Creating an Infinite loop

> ```python
> while True: 
>   '''stopper += 1
>   if (stopper >= 10):
>     break''' # If this code is not written, the loop keeps on going
> ```
>

* 'for' statement codes

> ```python
> for i in range(n):# n is for integers or variables that can be integers
> # if n<=0 the code does run in the for statement.
> ```







