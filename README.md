# php-vs-python

Exploring the differences between PHP and Python…

## Same syntax

* Assignment operator `$foo = 'bar';` vs `foo = 'bar'`
* Max value of array `max($arr)` vs `max(arr)`
* Min value of array `min($arr)` vs `min(arr)`
* Modulo `$a % $b` vs `a % b`
* Return statement `return $result;` vs `return result`

## Different syntax

* Convert variable to int `intval('5')` vs `int('5')`
* Convert variable to string `strval(5)` vs `str(5)`
* Check if value exists in array `in_array(2, [1, 2, 3])` vs `2 in [1, 2, 3]`
* Check if the value and type of the operands is the same `$a === $b` vs `a == b`
* Function declaration `function foo(){ }` vs `def foo():`
* Join array elements with a string `implode(',', $arr)` vs `','.join(arr)`
* Map callback to the elements of the array `array_map('intval', $arr)` vs `map(int, arr)`
* Ternary conditional operator `$condition ? $a : $b` vs `a if condition else b`
* Search element in array and get their index `array_search(1, [1, 2, 3])` vs `[1, 2, 3].index(2)`
* Convert a string to an array. 
  * Chunk size is 1. `$chunks = str_split($str)` vs `chunks = list(str)`
  * Chunk size is N. `$chunks = str_split($str, $n)` vs `chunks = [str[i:i+n] for i in range(0, len(str), n)]`
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
