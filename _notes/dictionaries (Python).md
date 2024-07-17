---
created: 2024-07-08T00:14:54-04:00
modified: 2024-07-10T05:54:26-04:00
type: note
tags:
  - computer-science/programming/python
  - cs50p
draft: false
parent: "[[Python]]"
share: true
dg-share: true
---

# [[Python]]

## Dictionaries

- one of four collection [data types](Basic%20data%20types%20in%20Python.md) (arrays) in Python
- used to store data of any type in `key:value` pairs
- ordered[^1], changeable[^2], does **not** allow duplicates

### Syntax

```python
fakedict = {
	"brand": "Apple",
	"model": "M1 Macbook Air",
	"year": "2021"
}
print(fakedict)
```

- can be indexed using the **key name**, will return the **value**

```python
fakedict = {
	"brand": "Apple",
	"model": "M1 Macbook Air",
	"year": "2021"
}
print(fakedict[“model”])
```

#### the `dict()` constructor

```python
fakedict = dict(brand = "Apple", model = "M1 Macbook Air", year = "2021")
```

[^1]: the items have a defined order that will **not** change

[^2]: we can change, add, or remove items after the dict has been created
