1. JavaScript 항목 1, 5, 6, 7, 8, 9, 14, 15번
2. ECMAScript6 항목 : 1번

JS 5
1. 변수
var x; // 변수의 선언
x = 6; // 정수값의 할당

2. 값
var str = 'Hello World'; // str : 이름, 'Hello World' : 값

2-2. 리터럴
// Number
var num1 = 1001;
var num2 = 10.50;

// String
var string1 = 'Hello';
var string2 = "World";

// Boolean
var bool = true;

// null
var foo = null;

// undefined
var bar;

// Object
var obj = { name: 'Lee', gender: 'male' };

// Array
var array = [ 1, 2, 3 ];

// function
var foo = function() {};

3. 연산자
// 산술 연산자
var area = 5 * 4; // 20

// 문자열 연결 연산자
var str = 'My name is ' + 'Lee'; // "My name is Lee"

// 할당 연산자
var color = 'red'; // "red"

// 비교 연산자
var foo = 3 > 5; // false

// 논리 연산자
var bar = (5 > 3) && (2 < 4);  // true

// 타입 연산자
var type = typeof 'Hi'; // "string"

// 인스턴스 생성 연산자
var today = new Date(); // Sat Dec 01 2018 00:57:19 GMT+0900 (한국 표준시)

피연산자의 타입 반드시 일치할 필요 X
var foo = 1 + '10'; // '110'
var bar = 1 * '10'; // 10

4. 키워드
// 변수의 선언
var x = 5 + 6;

// 함수의 선언
function foo (arg) {
  // 함수 종료 및 값의 반환
  return ++arg;
}

var i = 0;
// 반복문
while (1) {
  if (i > 5) {
    // 반복문 탈출
    break;
  }
  console.log(i);
  i++;
}

5. 주석
한줄 주석은 // 다음에 작성하며 여러 줄 주석은 /*과 */의 사이에 작성
주석은 해석기(parser)가 무시하며 실행되지 않음

6. 문
단계별로 수행될 명령어 집합
리터럴, 연산자(Operator), 표현식(Expression), 키워드(Keyword) 등으로 구성되며 세미콜론( ; )으로 끝나야 함
코드블록(code block,{...})으로 그룹화 가능
위에서 아래로 순서대로 실행
var time = 10;
var greeting;

if (time < 10) {
  greeting = 'Good morning';
} else if (time < 20) {
  greeting = 'Good day';
} else {
  greeting = 'Good evening';
}

console.log(greeting);

7. 표현식
하나의 값으로 평가
// 표현식
5             // 5
5 * 10        // 50
5 * 10 > 10   // true
(5 * 10 > 10) && (5 * 10 < 100)  // true

9. 함수
// 함수의 정의(함수 선언문)
function square(number) {
  return number * number;
}

// 함수의 호출
square(2); // 4

10. 객체
var person = {
  name: 'Lee',
  gender: 'male',
  sayHello: function () {
    console.log('Hi! My name is ' + this.name);
  }
};

console.log(typeof person); // object
console.log(person); // { name: 'Lee', gender: 'male', sayHello: [Function: sayHello] }

person.sayHello(); // Hi! My name is Lee

11. 배열
var arr = [1, 2, 3, 4, 5];

console.log(arr[1]); // 2

JS 6 Data type & Variable 데이터 타입과 변수

1. 데이터 타입
원시 타입 (primitive data type)
-boolean
-null
-undefined
-number
-string
-symbol (ES6에서 추가)
객체 타입 (object/reference type) : 변경 뷸가능(immutable value), 값에 의한 전달(pass-by-value)
-object

3가지 특별한 값들도 표현 rksmd

Infinity : 양의 무한대
-Infinity : 음의 무한대
NaN : 산술 연산 불가(not-a-number)

// typeof 연산자는 타입을 나타내는 문자열을 반환한다.

변수의 값이 없다는 것을 명시하고 싶은 경우 undefined를 할당하는 것이 아니라 null을 할당

일치 연산자 : ===

null 타입을 확인할 때 typeof 연산자를 사용하면 안되고 일치 연산자 사용(typeof 연산자로 null 값을 연산해 보면 null이 아닌 object가 나옴)

심볼(symbol)은 ES6에서 새롭게 추가된 7번째 타입으로 변경 불가능한 원시 타입
이름의 충돌 위험이 없는 유일한 객체의 프로퍼티 키(property key)를 만들기 위해 사용
// 심볼 key는 이름의 충돌 위험이 없는 유일한 객체의 프로퍼티 키
var key = Symbol('key');
console.log(typeof key); // symbol

var obj = {};
obj[key] = 'value';
console.log(obj[key]); // value

2. 변수
var, let, const 키워드를 사용하여 선언