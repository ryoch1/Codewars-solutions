# Largest product in a series

[This Kata on Codewars](https://www.codewars.com/kata/529872bdd0f550a06b00026e)

---

### Description: 

Complete the method so that it'll find the greatest product of five consecutive digits in the given string of digits.

For example: the greatest product of five consecutive digits in the string "123834539327238239583" is 3240.

The input string always has more than five digits.

Adapted from Project Euler.

---

## Solution

```python
def greatest_product(st):
    num_list = [int(i) for i in list(st)]
    return max([num_list[i] * num_list[i + 1] * num_list[i + 2] * num_list[i + 3] * num_list[i + 4] for i in range(0, len(num_list) - 4)])
```

---
