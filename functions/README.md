# PYTHON FUNCTIONS: EXERCISES

### PROBLEM 0: "list_of_powers" `*`

- (refresher) Write a function that can take 2 **integers**, `upper_bound` and `power` and return the **list** 
  of all powers of integers in the **range** between `0` (inclusive) and `upper_bound` (exclusive).
  
- For example; if `upper_bound = 3`  and `power = 3`; I expect to get: `[0, 1, 8]` as a function return.

- **EDGE CASES** (always think about edge cases): If `upper_bound` is `0` then I expect to get an empty list `[]`.

- Formal definition:

```Python
from typing import List

def list_of_powers(upper_bound: int, power: int) -> List[int]:
    """This function takes the `upper_bound` and a `power` and returns 
    the list of integers, where the list has all poowers of integers to a given 
    power within the range, given by the upper_bound.
    
    Parameters
    ----------
    upper_bound: int
    power: int
    
    Returns
    -------
    List[int]
    """
```

### PROBLEM 1: "magic_triangle" `*`

- Create the function that takes an integer `triangle_height` and a string `triangle_brick`, 
and create function that prints a triangle of a given `triangle_height` composed of `triangle_brick`s.
  
- For example if `triangle_height` is 3 and `triangle_brick` is "*" then we expect to see (in the console):

```shell
$ *
$ * *
$ * * *
$ * *
$ *
```

- For example, if `triangle_height` is 2 and `triangle_brick` is "Matko" then we expect to see (in the console):

```shell
$ Matko
$ Matko Matko
$ Matko
```

- Edge cases: Can you think about any? Well, what happens if `triangle_height` is 0. In that case we do not want 
  to print anything. Can you think about how would you check whether the input value is correct, i.e. 
  a positive integer?

- Note, this function **IS NOT RETURNING ANYTHING**. So, this function is an example of function that 
  **DOES NOT RETURN** but just **EXECUTES** some action (in our case printing).
  
- Note, the function in previous exercise was a function that actually returned some object.

- Note, technically (from the Python perspective) even the function that does not return a value, it secretly 
returns **None**.
  
```Python

def magic_triangle(triangle_height: int, triangle_brick: str):
  """This function takes `triangle_height` and `triangle_brick` and prints the triangle, composed
  from triangle bricks with the highest point given by triangle_height.
  
  Parameters
  ----------
  triangle_height: int
  triangle_brick: str
  """

```

### PROBLEM 2: "exchanger" `**`

1. We want to create a function that takes:
  - a `list of integers` (of any size) let's call it `in_list`
  - an `index` (an integer, that is guaranteed to be between `0` and `length of in_list minus 1`)
  - a `new_value`, also an integer.
  
2. Then the function will **exchange** the value in the `in_list` at the position given by `index` to 
a new value given by the `new_value`.
   
- More concretely I mean this:

  - let my `in_list = [1, 1024, 3]`
  - let my `index = 1`
  - let my `new_value = 2`
  
- Then I want a function, let's call it `exchanger` to do this:
  - after the execution of: `exchanger(in_list, index, new_value)`
  - I want my `in_list` have values: `[1, 2, 3]`
  
- Note, the `exchanger` function should **NOT** return anything (it is like the `magic_triangle`) function. 
  But, it should **execute** the exchange. 
  
- Note, this kind of operation is called `in place`; so you can google something like "replace list value in place".
  
- Edge cases: think about edge cases for this function. What are some "hackerish" combinations of input values, 
  that cann either break the function or cause some unexpected behavior. 


```Python
from typing import List

def exchanger(in_list: List[int], index: int, new_value: int):
    """This function takes the `in_list` and replaces the old value that the `in_list` has
    under the index (i.e. value of `in_list[index]` ) with a new value given by `new_value`.
    So, after this exchange the `in_list` will have stored value: `in_list[index]` equal to the new_value.
    
    Parameters
    ----------
    in_list: List[int]
    index: int
    new_value: int
    
    """
```

### PROBLEM 3: "randomial": `***`

- This function is a funny generalization of normal factorial. 
  
- The normal factorial is a function, usually denoted by `!`.

- The function `!` (factorial) takes a **non-negative integer** `n` and returns another non-negative integer 
  obtained as a multiplication of all the integers in the range between 1 and `n`.
  
- For example `3!` is a number given by: `1 * 2 * 3`.

- The normal factorial `!` is also defined for `0` as `0! = 1`.

- In this exercise we will create a funny randomized generalization of a factorial.

- This function takes:
  1. an **integer** `n`
  2. an **integer** replacement value `replacer`
  
- This function returns a value that is given by the following procedure:
  1. in the normal factorial calculation of `n!` (that is again given as: `1 * 2 * 3 * ... * n`)
  2. replace random integers with a `replacer` value.
  
- For example:
  1. If I have `6!`, that is given as `1 * 2 * 3 * 4 * 5 * 6`
  2. and my `replacer` is given by `replacer = 77`
  3. then, I want to calculate `randomial(6, 77)`
  4. that result might be for example given by: `1 * 77 * 3 * 4 * 77 * 6`.
  5. **EXTREMELY IMPORTANT** this replacement must be random every time.
  6. This means: in the next run of `randomial(6, 77)` I might get the value that 
     is given by: `1 * 2 * 3 * 77 * 5 * 6`.
  7. Another time `randomial(6, 77)` might give value: `77 * 77 * 77 * 77 * 5 * 6`
  
- Hint: the build in module called `random` might be of help. Google "python random stackoverflow"

- Edge Cases: again think about edge cases for this function! What can break this function, what are 
some input values, that can cause some unexpected behavior.

```Python

def randomial(n: int, replacer: int) -> int:
    """This function takes an non-negative integer `n` and a non-negative integer `replacer`. It 
    will calculate an integer whose value is given by a product of an integers in range, but some of them
     are randomly replaced by a `replacer`.
     
    Parameters
    ---------- 
    n: int
        is the randomial input non-negative integer
    
    replacer: int
        is a non-negative integer that replaces random values in the factorial calculation.
        
    Returns
    -------
    int
        is the integer obtained by randomly replacing values in factorial calculation with a replacer.
      
    """
```



