# DATA STRUCTURES: EXERCISES

### PROBLEM 0: "unique strings" `*`

- write a function, that takes a **list** of strings and returns a **list** of unique strings 
  (in any order).

- For example, if I have a list of strings: `["matko", "matko", "lenka", "lucka", "peto"]`,
then I want to return a list `["lucka", "lenka", "matko", "peto"]` (again the order of the final 
  list is not important in this exercise)
  
- Lets define the function we want:

```python

from typing import List

def unique_strings(in_list: List[str]) -> List[str]:
    """This function takes the list of strings and returns the list of unique strings.
    
    Parameters
    ----------
    in_list: List[str]
        is the list of input strings
    
    Returns
    -------
    List[str]
        is the list of output strings
    
    """    

```

- For example if `in_list=["matko", "matko", "Matko"]` I want the function 
  `unique_strings` to do:
  - `unique_strings(in_list)` will return `["matko", "Matko"]`
    
- Again, think about edge cases, what should happen if the list is empty? 
  (I want back an empty list)
  

### PROBLEM 1: "small database and it's backup" `*`

- in this exercise we will create 2 functions.

- The first function should take an input database (in our case a **dictionary**) and will save
a value under some (immutable) key.
  
- Remember this is just a refreshing exercise (since we coded this together).

- Nevertheless, we want the function **upload_value** with the following definition

```python

def upload_value(in_database: dict, key, value):
    """This function takes the `in_database` and a key and a value
    and will "upload" a value under the given key. This function returns NOTHING
    but rather executes some action.
    
    Parameters
    ----------
    in_database: dict
        is a dictionary, that will serve the role of our small key value database
    
    key
        is some immutable (or more precisely hashable) key
    
    value
        is some value, we want to store under the given key. 
    
    """

```

- more concretely, we want our function **upload_value** to do the following:

    - 0: for the database (for example an empty database) `in_database = {}`
    - 1: for the `key = 'matko'` and value `35`
    - 2: we want our function `upload_value(in_database, 'matko', 35)` to add value `35`
    under key `matko`.
    - 3: So after execution of **upload_value** the `in_database` will look like: `{'matko': 35}`
    
- NOW, in the next step (I mean once the function **upload_value** function works). 
  I want you to modify it in a way that in the situation when you have a clashing keys, 
  you will raise a `KeyError`.
  
- I.e. the modified function will have the following properties:

```python

def upload_value(in_database: dict, key, value):
    """This function takes the `in_database` and a key and a value
    and will "upload" a value under the given key. This function returns NOTHING
    but rather executes some action.
    
    Parameters
    ----------
    in_database: dict
        is a dictionary, that will serve the role of our small key value database
    
    key
        is some immutable (or more precisely hashable) key
    
    value
        is some value, we want to store under the given key. 
        
    Raises
    ------
    KeyError
        this is error that is thrown, when the input `key` is already a key in the database.
    
    Returns
    -------
    None
    
    """

```

- FINALLY, I want to write a function that:

- can take 2 databases (i.e. the python dictionaries)

- one database will be called `main_database` and another will be called 
`backup_database`.
  
- this function will be called **upload_value_with_backup** will upload the 
value for given key into the `main_database` as well as into the `backup_database`.
  
- Agin, it will also throw the `KeyError` if the key is either in the `main_database` or in 
  `backup_database`.
  
- More concretely I want the function with the following properties:

```python

def upload_value_with_backup(main_database: dict, backup: dict, key, value):
    """This function uploads the value, under given key into the main_database
    as well as into the backup_database. It will also raise the KeyError when there is
    already a key in the main database or in the backup.
    
    Parameters
    ----------
    main_database: dict
        is the main database where we will be saving our data
    backup: dict
        is the backup database where we will be storing our data (but this one will 
        be maintained for the backup purposes)
        
    key
        is the hashable key
        
    value
        is the value we want to store under the key
    
    Returns
    -------
    None
    
    """

```





