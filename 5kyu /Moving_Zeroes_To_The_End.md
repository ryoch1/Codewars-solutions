# Moving Zeroes To The End

[This Kata on Codewars](https://www.codewars.com/kata/52597aa56021e91c93000cb0)

---

### Description:

Write an algorithm that takes an array and moves all of the zeros to the end, preserving the order of the other elements.

```c++
move_zeros([1, 0, 1, 2, 0, 1, 3]) # returns [1, 1, 2, 1, 3, 0, 0]
```

---

## Solution

```c++
#include <vector>

std::vector<int> move_zeroes(const std::vector<int>& input) {
  
  std::vector<int> res;
  int n = input.size();
  int counter_of_zeroes = 0;
  
  for (int i = 0; i < n; i++){
    if (input[i] != 0){
      res.push_back(input[i]);
    } else{
      counter_of_zeroes++;
    }
  }
  if (counter_of_zeroes == 0){
    return res;
  } else{
    for (int i = 0; i < counter_of_zeroes; i++){
      res.push_back(0);
    }
    return res;
  }
}
```

---
