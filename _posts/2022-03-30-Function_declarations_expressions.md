---
title: 'about function declarations, expressions'
header:
  # image: /assets/images/unsplash-image-6.jpg
  # caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
categories:
  - Develop
  - TIL
tags:
  - javascript
  - coding
  - tech_interview
---

---

# function declarations, expressions

## function declarations

```javascript
// example
function funcDeclarations() {
  return 'A function declaration';
};
funcDeclarations(); // 'A function declaration'
```

## function expressions

```javascript
// example
var funcExpression = function () {
  return 'A function expression';
};
funcExpression(); // 'A function expression'
```


### Benefits of Function Expressions
There are several different ways that function expressions become more useful than function declarations.
- As closures
- As arguments to other functions (as callback function)
- As Immediately Invoked Function Expressions (IIFE)

---
