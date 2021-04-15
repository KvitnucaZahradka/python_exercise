# PYTHON FUNCTIONS: EXERCISES

### PROBLEM 0: `*`

- (refresher) Write a function that can take 2 **integers**, `upper_bound` and `power` and return the **list** 
  of all powers of integers in the **range** between `0` (inclusive) and `upper_bound` (exclusive).
  
- For example; if `upper_bound = 3`  and `power = 3`; I expect to get: `[0, 1, 8]` as a function return.

- **EDGE CASES** (always think about edge cases): If `upper_bound` is `0` then I expect to get an empty list `[]`.

- Formal definition:

```Python
from typing import List

def list_of_powers(upper_bound: int, power: int) -> List[int]:
    """This function takes the upper_bound and a power and returns 
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

### PROBLEM 1: `*`

- Create the function



