# Split Strings 

[This Kata on Codewars](https://www.codewars.com/kata/515de9ae9dcfc28eb6000001)

---

### Description:

Complete the solution so that it splits the string into pairs of two characters. If the string contains an odd number of characters then it should replace the missing second character of the final pair with an underscore ('_').

### Examples:

```python
'abc' =>  ['ab', 'c_']
'abcdef' => ['ab', 'cd', 'ef']
```

---

## Solution

```python
def solution(s):
    return [s[x:x+2] if x < len(s) - 1 else s[-1] + "_" for x in range(0, len(s), 2)]
```

---
