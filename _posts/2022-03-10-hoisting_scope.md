---
title: 'about function hoisting, scope'
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

# function hoisting, scope

## Hoisting

함수 안에 있는 선언들을 모두 끌어올려서 해당 함수 유효 범위의 최상단에 선언하는 것을 말한다.

-  자바스크립트 함수는 실행되기 전에 함수 안에 필요한 변수값들을 모두 모아서 유효 범위의 최상단에 선언한다.
    -  자바스크립트 Parser가 함수 실행 전 해당 함수를 한 번 훑는다.
    -  함수 안에 존재하는 변수/함수선언에 대한 정보를 기억하고 있다가 실행시킨다.
    -  유효 범위, 함수 블록 안에서 유효.
- 함수 내에서 하부에 존재하는 내용 중 필요한 값들을 끌어 올리는 것.
    -  실제 코드가 올려지는 것은 아니다.
    -  javacript parser 내부적으로 끌어올려서 처리.
    -  실제 메모리에서는 변화가 없다.
    

## Hoisting 대상
- `var`변수 선언과 함수선언문에서만 hoisting이 발생
    -  var 변수/함수의 선언만 위로 끌어 올려지며, 할당은 끌어 올려지지 않는다.
    -  let/const 변수 선언과 함수 표현식에서는 호이스팅이 정상적으로 발생하지 않는다. (호이스팅은 발생하지만 에러또한 발생한다.)

    ```javascript
    // 호이스팅이 발생해 에러를 출력하는 예시 
    let foo = 2;
    {
      console.log(foo);
      let foo = 3;
    }

    // VM15:3 Uncaught ReferenceError: Cannot access 'foo' before initialization at <anonymous>:3:15
    ```

---
