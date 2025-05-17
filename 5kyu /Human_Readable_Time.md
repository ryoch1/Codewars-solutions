# Human Readable Time

[This Kata on Codewars](https://www.codewars.com/kata/52685f7382004e774f0001f7)

---

### Description:

Write a function, which takes a non-negative integer (seconds) as input and returns the time in a human-readable format (HH:MM:SS)

- HH = hours, padded to 2 digits, range: 00 - 99
- MM = minutes, padded to 2 digits, range: 00 - 59
- SS = seconds, padded to 2 digits, range: 00 - 59
The maximum time never exceeds 359999 (99:59:59)

You can find some examples in the test fixtures.

---

## Solution

```python
def make_readable(seconds):
    h = seconds // 3600
    m = seconds // 60 % 60
    s = seconds % 60
    return f"{h:0>2d}:{m:0>2d}:{s:0>2d}"
```
