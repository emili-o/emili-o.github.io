---
type: note
tags:
  - computer-science/programming/python
  - loops
draft: false
parent: "[[Python]]"
aliases:
  - return
share: true
modified: 2024-07-07T23:20:10-04:00
---

# [[Python]]

## The `return` statement

- ends the execution of the function call, return result to the caller
- any code written after the `return` statement will **not** be executed!

```python
def cube(x):
	r = x ** 3
	return r
```
