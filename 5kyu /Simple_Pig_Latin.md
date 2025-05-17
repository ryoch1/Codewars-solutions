# Simple Pig Latin

[This Kata on Codewars](https://www.codewars.com/kata/520b9d2ad5c005041100000f)

---

### Description:
Move the first letter of each word to the end of it, then add "ay" to the end of the word. Leave punctuation marks untouched.

### Examples

```python
pig_it('Pig latin is cool') # igPay atinlay siay oolcay
pig_it('Hello world !')     # elloHay orldway !
```

---

## Solution

```python
def pig_it(text):
    answer = []
    s = text.split()
    for i in s:
        if i.isalpha() == True:
            r = list(i)
            ch = r.pop(0)
            r.append(ch)
            res = "".join(r) + "ay"
            answer.append(res)
        else:
            answer.append(i)
    return " ".join(answer)
```

---
