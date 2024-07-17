---
type: note
tags:
  - strings
  - data-types
  - computer-science/programming/javascript
aliases:
  - template strings
parent:
  - "[JavaScript](JavaScript.md)"
created: 2024-06-11T20:54
updated: 2024-06-29T01:17
draft: true
share: true
modified: 2024-07-10T07:01:32-04:00
---

# Javascript


## Template literals (template strings)

- strings which are declared using backticks
- can be declared over multiple lines.
- more readable way of doing string concatenation.

```js
const name = "Emilio";
const greeting = `Hello, ${name}`;
console.log(greeting); // "Hello, Emilio"
```

- can also include JavaScript expressions

```js
const song = "Parsec";
const album = "Dots and Loops";
const score = 10;
const highest_score = 10;
const output = `I like the song ${song} from Stereolab's\
 album ${album}. The album itself is a ${score} out of\
 ${highest_score} for me, \
 ${(score / highest_score) * 100}%.`;
console.log(output);
```

## Nesting template literals

You can embed template literals within other template literals.

- useful for constructing strings dynamically that themselves contain dynamic content

### Direct nesting

```js
const innerLiteral = `inner content`;
const outerLiteral = `This is the outer content and here is the ${innerLiteral}.`;
console.log(outerLiteral);
```

### Function-based nesting

```js
function createInnerLiteral(name) {
  return `Hello, ${name}!`;
}

const name = "Emilio";
const outerLiteral = `This is the outer content and here is the ${createInnerLiteral(name)}.`;
console.log(outerLiteral);
```

### Advanced example

```js
function createListItem(content) {
  return `<li>${content}</li>`;
}

const items = ["Item 1", "Item 2", "Item 3"];
const list = `
<ul>
	${items.map((item) => createListItem(item)).join("")} </ul>
`;

console.log(list);
```

## Tagged templates

```js
const person = "Emilio";
const age = 29;

function myTag(strings, personExp, ageExp) {
  const str0 = strings[0];
  const str1 = strings[1];
  const str2 = strings[2];

  const ageStr = ageExp < 100 ? "youngster" : "centenarian";

  return `${str0}${personExp}${str1}${ageStr}${str2}`;
}

const output = myTag`That ${person} is a ${age}.`;

console.log(output);
```
