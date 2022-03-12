---
title: 'var, let, const'
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

# var, let, const 차이

- `var` 는 `function-scope`
- `let`,`const`는 `block-scope`

```javascript
// var는 function-scope이기 때문에 for문이 끝난다음에 j를 호출하면 값이 출력이 잘 된다.
// 이건 var가 hoisting이 되었기 때문이다.
for (var j = 0; j < 10; j++) {
  console.log('j', j);
}
console.log('after loop j is ', j); // after loop j is 10

// 아래의 경우에는 에러가 발생한다.
function counter() {
  for (var i = 0; i < 10; i++) {
    console.log('i', i);
  }
}
counter();
console.log('after loop i is', i); // ReferenceError: i is not defined
```

- es2015에는 `let`, `const`가 추가 되었다.
이전에는 javascript 에 `var`만이 존재 했었기 때문에 아래와 같은 불편함이 있었다.
```javascript
// 이미 만들어진 변수이름으로 재선언했는데 아무런 문제가 발생하지 않는다.
var a = 'test'
var a = 'test2'

// hoisting으로 인해 ReferenceError에러가 안난다.
c = 'test'
var c
```
두개의 공통점은 var와 다르게 변수 재선언 불가능이다.

- let은 변수에 재할당이 가능하지만,
- const는 변수 재선언, 재할당 모두 불가능하다.
```javascript
// let
let a = 'test'
let a = 'test2' // Uncaught SyntaxError: Identifier 'a' has already been declared
a = 'test3'     // 가능

// const
const b = 'test'
const b = 'test2' // Uncaught SyntaxError: Identifier 'a' has already been declared
b = 'test3'    // Uncaught TypeError:Assignment to constant variable.
```
---
