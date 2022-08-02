# php-vs-python

Exploring the differences between PHP and Python…

## Same syntax

* Max value of array `max($arr)` vs `max(arr)`
* Min value of array `min($arr)` vs `min(arr)`
* Modulo `$a % $b` vs `a % b`

## Different syntax

* Ternary conditional operator `$condition ? $a : $b` vs `a if condition else b`
* Split string by character `str_split($str)` vs `list(str)`
* Join string by character (comma) `implode(',', $arr)` vs `','.join(arr)`
* Convert variable to int `intval($value)` vs `int(value)`

### Loops

* Iterate over array `foreach($arr as $value)` vs `for value in arr:`
* Iterate over array with index `foreach($arr as $index => $value)` vs `for index, x in enumerate(arr):`
* Iterate over associative array with index:
 
In PHP: 
```php
foreach($arr as $key => $value){
    echo $key . '->' . $value;
}
```

In Python ([dictionaries](https://www.w3schools.com/python/python_dictionaries.asp)): 
```py
for key in a_dict:
    print(key, '->', a_dict[key])
```

## Python unique syntax

* [pass](https://www.w3schools.com/python/ref_keyword_pass.asp) - a placeholder for future code
