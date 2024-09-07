# 04. 변수

- 변수
- 식별자
- 선언

## 4.1 변수

변수란 데이터를 저장하는 공간, 또는 공간을 참조하기 위한 식별자를 의미한다. 사람이 이해할 수 있는 값 '소프트웨어 엔지니어'를 프로그램에서 자주 사용한다.
자주 사용하는 값을 매번 사용하는 것도 가능하다. 하지만 사람은 실수하기 마련이다. 또한 인지하는데 비용이 든다.
'소프트웨어 엔지니여'처럼 한 글자를 수정했다. 육안에 들어오는가. 실수를 방지하고자 JavaScript에서는 자주 사용하는 값을 저장하는 '변수'를 사용한다.

변수는 이름을 붙여줄 수 있다. 이때 변수의 이름(naming)은 상당히 중요하다. 코드는 누구든지 작성할 수 있다. 하지만 '읽기 좋은 코드'를 작성하는 것은 어렵다.
간단한 프로그램 일지라도 '읽기 좋은 코드'를 작성하는 습관을 들이자. 아무것도 배우지 않은 상황에서 습관을 만드는 것은 쉽다. 하지만 잘못된 습관을 좋은 습관으로
변경하는 것은 몹시 어렵다. 부디 습관으로 삼자. (best practice)

## 4.2 식별자

변수란 '공간을 판별하기 위한 식별자'라고 표현했다. 식별자를 이해하기 위해서는 컴퓨터를 조금 더 이해해야 한다. 간단하게 알아보자.

> 10 + 20

다음 값을 컴퓨터는 2진수로 해석해서 메모리에 저장한다. 10이라는 값을 2진수로 변환해서 메모리에 저장하고 연산자를 저장한다. 더불어 20이라는 값도 2진수로 변환해서 저장한다.
각 값은 메모리에 저장된다. 이때 메모리 주소를 식별자라 한다. JavaScript는 직접적으로 메모리 주소를 다룰 수 없다. 만약 메모리 주소를 다룰 수 있다고 하더라도 사람이 이해하고
사용하기 어렵다. 따라서 JavaScript는 직접적으로 접근하는 방식보다, 메모리 주소를 식별할 수 있는 이름을 붙인다. 이것이 '식별자'다.

다시 알아보면 10 + 20 연산의 결과인 '30'이라는 값을 또 다른 메모리에 저장한다.

> 식별자는 '변수'에서만 다루는 개념이 아니다. 함수, 메서드드등 전반적인 개념에서 사용한다. 따라서 간단하지만 꼭 이해해야 한다.

## 4.3 선언

> 내가 그의 이름을 불러주기 전에는<br>
> 그는 다만<br>
> 하나의 몸짓에 지나지 않았다.
> 
> 내가 그의 이름을 불러주었을 때<br>
> 그는 나에게로 와서<br>
> 꽃이 되었다.
> 
> <출처: 김춘수 - 꽃>

변수를 선언하지 않으면 데이터에 불과하다. 그렇다면 어떻게 선언할 수 있을까? JavaScript에서는 `var`, `let`, `const`키워드를 사용한다.

> 키워드란 자주 사용하는 개념을 미리 정의해둔 예약어다. *인프런 예약어

### var

```javascript
var poem;
```

var 키워드는 이전에 자주 사용했다. poem라는 이름의 변수를 선언한다. 변수의 선언은 초기화, 할당 단계를 가진다. 

1. var 키워드를 사용해서 poem이라는 식별자를 붙인 `undefined` 값의 변수를 선언한다.
2. poem의 값을 따로 할당하지 않았으므로 값은 여전히 `undefined`다.

> JavaScript의 값은 할당하지 않으면 undefined가 할당된다.

그렇다면 값은 어떻게 할당할까?

```javascript
var poem = '김춘수 - 꽃';
```

1. 위와 동일
2. poem에 리터럴 값 '김춘수 - 꽃'을 할당한다. 따라서 peom을 참조하면 '김춘수 - 꽃'을 만날 수 있다.

var 키워드로 변수를 선언하는 방법을 알아봤다. 예제만 봤을 때 var 키워드로 충분한 것 같다. 설명을 마친다.

그렇지 않다. var 키워드로 선언한 변수는 문제가 있다. 

> 문제란 잘못됐다가 아니라 '불편하고 인지하는데 더 많은 비용을 사용한다'라는 뜻이다.

var 키워드의 문제를 해결하기 위해서 `let`, `const` 키워드가 등장했다.

> 새로운 문법의 등장은 이전 기술의 문제를 해결하기 위해, 또는 더 편리하게 사용하기 위해서 등장한다. 따라서 이전의 문법을 사용한 선배들은 어떤 어려움을 겪었는지
> 간단하게 알아보고 넘어가는 것이 새로운 기술을 더 빠르게 이해하는데 유리하다.

- var 키워드의 문제점
- let, const의 등장

다음 부분은 다음 시간에 알아본다.

### 변수는 어디로 갔을까?

JavaScript는 모든 식별자를 '실행 컨텍스트'에 저장한다. '모든 식별자'라는 표현이 인상 깊다. 실행 컨텍스트는 JavaScript에서 꼭 이해해야 하는 핵심 개념 중 하나다.