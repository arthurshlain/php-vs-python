# php-vs-python

Exploring the differences between PHP and Python…

## Same syntax

* Assignment operator `$foo = 'bar';` vs `foo = 'bar'`
* Create an empty array `$foo = [];` vs empty list `foo = []`
* Create an array with values `$foo = [1, 2, 'str'];` vs list with values `foo = [1, 2, 'str']`
* Max value of array `max($arr)` vs `max(arr)`
* Min value of array `min($arr)` vs `min(arr)`
* Modulo `$a % $b` vs `a % b`
* Return statement `return $result;` vs `return result`

## Different syntax

* Convert a string to an array. 
  * Chunk size is 1. `$chunks = str_split($str)` vs `chunks = list(str)`
  * Chunk size is N. `$chunks = str_split($str, $n)` vs `chunks = [str[i:i+n] for i in range(0, len(str), n)]`
* Convert variable to int `intval('5')` vs `int('5')`
* Convert variable to string `strval(5)` vs `str(5)`
* Check if value exists in array `in_array(2, [1, 2, 3])` vs `2 in [1, 2, 3]`
* Check if the value and type of the operands is the same `$a === $b` vs `a == b`
* Filter array values by condition `array_filter([1, 2, 'foo'], 'is_int');` vs `[e for e in [1, 2, 'foo'] if isinstance(e, int)]`
* Function declaration `function foo(){ }` vs `def foo():`
* Join array elements with a string `implode(',', $arr)` vs `','.join(arr)`
* Map callback to the elements of the array `array_map('intval', $arr)` vs `map(int, arr)`
* Search element in array and get their index `array_search(1, [1, 2, 3])` vs `[1, 2, 3].index(2)`
* Split a string by a string (return array): `explode(',', $str)` vs `str.split(',')`
* Split a string by a string with limit: `explode(',', $str, 3)` vs `str.split(',', 3)`
* Reverse a string `$str = strrev($str)` vs `str = str[::-1]`
* Round fractions up and down:
  * In PHP:
  ```php
  ceil(1.5); // → 2
  floor(1.5); // → 1
  ```
 
  * In Python:
  ```py
  import math
  
  math.ceil(1.5) # → 2
  math.floor(1.5) # → 1
  ```
  
* Ternary conditional operator `$condition ? $a : $b` vs `a if condition else b`

### Loops

* Iterate over array `foreach($arr as $value)` vs `for value in arr:`
* Iterate over array with index `foreach($arr as $index => $value)` vs `for index, x in enumerate(arr):`
* Iterate over associative array with index:
 
  * In PHP: 
  ```php
  foreach($arr as $key => $value){
      echo $key . '->' . $value;
  }
  ```

  * In Python ([dictionaries](https://www.w3schools.com/python/python_dictionaries.asp)): 
  ```py
  for key in a_dict:
      print(key, '->', a_dict[key])
  ```

## Python unique syntax

* [pass](https://www.w3schools.com/python/ref_keyword_pass.asp) - a placeholder for future code
