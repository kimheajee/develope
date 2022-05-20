질문 ✔ 

1. JavaScript의 자료형과 JavaScript만의 특성은 무엇일까?
 

💁‍♀️   Javascript 의 자료형 
Primitive(기본형)과 Object(객체) 타입이 존재한다.
기본적으로 자바스크립트는 인터프리터가 알아서 변수의 타입을 파악하고 값을 저장해, 변수의 타입을 따로 쓰지 않는다.

ex )
var a = 10;
var b = 'k';
👉기본형 자료형
Boolean : 논리적인 요소, true와 false값이 있다.
null : 빈 값
undefined : 값을 할당하지 않은 변수가 가지는 값
Number : 숫자형으로 정수와 부동 소수점, 무한대 및 NaN(숫자가 아님)값을 포함한다.
String : 문자열


숫자형의 NaN과 Infinity
NaN은 숫자가 아님을 의미하며 Infinity는 무한대를 의미한다.
parseInt('blabla'), Math.sqrt(-1) 등의 함수는 Nan을 반환하게 되며, 42 / 0 처럼 무한대가 나오는 식은 Infinity를 반환한다.
자바스크립트의 문자형
자바스크립트에서는 char 형이 존재하지 않아 " 또는 '중 어떤 것으로 감싸도 문자열로 만들어진다.
이스케이프 문자를 사용 가능하다. 문자열끼리 이어 붙이거나 숫자를 붙일때는 + 연산자를 사용한다.
문자열 인덱싱도 가능하다.
👉Object 자료형
Reference 타입이라고도 한다. Object 클래스 뿐만 아니라, 배열과 함수, 사용자 정의 클래스도 모두 Object에 포함된다.
객체 자료형과 기본형 자료형의 가장 큰 차이점은 Reference(참조)에 있다. 원시 타입의 변수는 다른 변수에 값을 할당하거나 함수 인자로 넘길 때, 값을 복사하여 전달하지만, 객체는 메모리 주소를 복사시키며 값 자체는 복사되지 않아 같은 객체를 참조하게 된다. 배열도 객체의 일부이며, 함수의 인자로 넘기거나 다른 변수에 참조시킬 수 있다.

👉배열 자료형
자바스크립트의 배열은 숫자형이나 문자열과 마찬가지로 일반적인 스크립트 언어와 크게 다른 것이 없다. 배열은 []나 newArray()로 생성하며, 크기의 제약이 없고, 하나의 배열에 서로 다른 타입의 변수가 들어갈 수 있다.

ex )
var array = new Array(2,4,5,"a",'b');
자주사용되는 속성과 메소드
변수명.length() : 길이
변수명.push(추가할값) : 맨 뒤에 항목 추가
변수명.pop() : 맨뒤의 항목 제거
변수명.unshift(추가할값) : 맨 앞에 항목 추가
변수명.shift() : 맨 앞의 항목 제거
변수명.indexOf(찾을값) : 배열 내부 값의 위치 찾기
👉딕셔너리 자료형
키-값 형태를 저장할 수 있다.
중괄호 {}를 이용하여 생성하고, 콜론(:)을 사용해 키-값 쌍을 저장하며, 콘마(,)를 이용하여 여러개의 키-값 쌍을 저장 할 수 있다. 중괄호 대신 new Object() 생성자 사용도 가능하며, 인덱스 접근자 []를 사용하여 키-값을 설정할 수도 있다.

ex 1 ) var me = {'kim':'byeonguk','birth':1994};
ex 2 ) var me = {};
me['name'] = 'kimbyeonguk';
me['birth'] '1994';
ex 3 ) me.birth = 1994;
💁‍♀️  느슨한 타입(loosely typed)의 동적(dynamic) 언어
느슨한 타입(loosely typed)란 ?

- 타입없이 변수를 선언하는 것
- 자바스크립트가 변수를 선언할 때 타입없이 var(variable 약어)로만 선언함
 

- 느슨한타입과 반대되는 말은 강력한타입, 강력한타입은 반대로 변수를 선언할 때 타입을 선언해야함
- 타입없이 선언했다고해서 변수의 타입이 없는 것은 아님 : 내부적으로 정해짐

- 내부적으로 변수의 타입이 관리되기때문에 변수의 타입이 바뀔 때가 있음
 
그렇다면 동적인 언어와, 정적인 언어는 무엇일까 ?
정적 언어 (Statically Typed Language)
컴파일 시간에 변수의 타입이 결정되는 언어.
타입 즉, 자료형을 컴파일 시에 결정하는 것.
C, C++, Java 등은 대표적인 정적 언어이다.
정적 언어는 변수에 들어갈 값의 형태에 따라 자료형을 지정해주어야 한다.
컴파일 시에 자료형에 맞지 않는 값이 들어있을 경우 컴파일 에러가 발생한다.
컴파일 시간에 변수의 타입을 체크하므로 사소한 버그들을 쉽게 체크할 수 있는 장점이 있다.
즉 타입 에러로 인한 문제점을 초기에 발견할 수 있어 타입의 안정성이 올라간다.
💁‍♀️ 동적 언어 (Dynamically Typed Language)
런타임에 타입이 결정되는 언어.
즉, 소스가 빌드될 때 자료형을 결정하는 것이 아니라 실행 시 결정된다.
매번 타입을 써줄 필요가 없기 때문에 프로그래머가 빠르게 코드를 작성할 수 있다.
JavaScript, Ruby, Python 등은 대표적인 동적 언어이다.
런타임까지 타입에 대한 결정을 끌고 갈 수 있기 때문에 선택의 여지가 있다.
실행 도중에 변수에 예상치 못한 타입이 들어와 Type Error가 발생하는 경우가 생길 수 있다.
💁‍♀️  JavaScript 형 변환
함수와 연산자에 전달되는 값은 대부분 적절한 자료형으로 자동 변환된다,
이런 과정을 "형 변환(type conversion)"이라고 한다.
 

다음 표현식이 어떻게 될지 생각해보시기 바란다.

4 + 10 + "string"
"string" + 4 + 10
"true" == true
undefined == ''
8 * null
0 == "\n"
!![]+!!{}+!!"false"
~undefined
[2] > "1"
"hello" > 3
"hello" < 3
"-1" > "+1"
"-1" > +1
"b" + "a" + + "a" + "a"
[] + undefined + 1
[2,3,5] == [2,3,5]
{}+[]+{}+[1]
!+[]+[]+![]
!+[]+![]+[]
[1] + [2,3]
기본 이론
형변환은 명시적일 수도 있고, 암시적일 수도 있다. 

명시적 형변환(explicit coercion)은 Number("123") 처럼 프로그래머의 코드에서 암시적으로 자료형을 정해서 변환하는 과정이다.

암시적 형변환(implicit coercion)은 연산자 사용으로 인해 자연적으로 일어나는 형변환이다.

대표적인 예시로 ==, +, > 등 연산자의 사용이 있다. 예외적으로 ===는 형변환을 야기하지 않는다.

이 암시적 형변환을 잘 이용하면 더욱 가독성 있는 코드를 작성할 수 있지만 잘못 생각하면 프로그램의 버그가 될 수 있다.

 

JavaScript에서의 형변환은 세 가지가 있다.

String으로 형변환
Number로 형변환
Boolean으로 형변환
또, 원시 타입과 객체(object)에 대해 형변환이 다르게 적용된다.

 

JavaScript의 원시 타입 형변환
String conversion
명시적 형변환은 String() 함수를 쓰면 된다.

암시적 형변환은 + 연산자를 사용할 때 피연산자에 String이 있을 때 일어난다.

String으로의 변환은 자연스럽다. 출력되는 형태 그대로 변환되기 때문이다.

String(12345)                   // "12345"
String(-3.14)                   // "-3.14"
String(true)                    // "true"
String(false)                   // "false"
String(undefined)               // "undefined"
String(null)                    // "null"
String(BigInt(42))              // "42"
Symbol은 암시적 형변환이 되지 않기 때문에 명시적 형변환을 해야 한다.

String(Symbol("Explicit"))      // "Explicit"
"and..." + Symbol("implicit")   // TypeError
Boolean conversion
명시적 형변환을 하려면 Boolean()을 호출하면 된다. 암시적으로는 ||, &&, !에 의해 일어난다. 

||와 &&는 조건에 맞는 실제 피연산자를 반환하지만, 내부적으로는 형변환이 일어난다.

Boolean형에는 true와 false밖에 없기 때문에, 거짓값(falsy value)를 열거하는 게 낫다.

'', 0, NaN, null, undefined, false, BigInt(0)가 전부이다.

나머지(객체, Date, 리스트, 함수 등등) 는 전부 true로 변환된다.

Number conversion
명시적 형변환을 하려면 Number()를 호출하면 된다. 암시적으로는 좀 많이 불린다.

비교 연산자 (>, <, <=, >=, !=, ==) (단, 두 피연산자가 모두 String일 때는 제외)
비트 연산자 (|, &, ^, ~)
산술 연산자 (-, +, *, /, %) (단, +의 연산자에 String이 있을 때는 제외)
단항 연산자 (+)
변환하는 과정은 조금 복잡하다.

String의 경우, 앞뒤 whitespace를 제외하고 빈 문자열이면 0으로, Number로 변환될 수 있으면 해당 Number로 (Infinity, 1e9 등), 아니면 NaN으로 변환된다
null은 0으로, undefined는 NaN으로 변환된다
Symbol은 명시적으로도 암시적으로도 변환될 수 없으며 TypeError를 야기한다.
null이나 undefined는 ==에서 형변환이 일어나지 않으며, null과 undefined가 == 연산자에서 true가 되는 경우는 이 두 가지 밖에 없다
NaN은 !== 연산자로도 false가 나온다.
BigInt는 명시적으로밖에 변환하지 못하며, 암시적 변환은 TypeError를 야기한다.
변환은 아니지만, 비트 연산에서 Infinity, -Infinity, NaN은 0으로 취급된다.
JavaScript의 object 형변환
그럼 [1] + [2,3] 같은 건 어떻게 적용되는 걸까?

우선 JavaScript 엔진은 객제를 원시 타입으로 바꾸려는 시도를 한다. 그리고 가능한 변환은 String, Number, Boolean밖에 없다. 

Boolean의 경우 앞서 말했듯이 무조건 true로 변환된다.

그 외로는 [[ToPrimitive]] 메서드를 이용해 변환되는데, 과정이 대략 다음과 같다.

[[ToPrimitive]] 메서드에 preferredType을 넘겨서 변환하고자 하는 형(Number나 String)을 명시할 수 있다 (필수는 아님).
Number 로 변환하든 String으로 변환하든 Object.prototype의 valueOf랑 toString을 사용하며, 임의의 object에 존재한다.
원시 타입이 입력으로 들어오면 그 입력을 그대로 반환한다.
두 경우 모두 valueOf와 toString을 기본적으로 호출하고, 그 결과가 원시 타입이면 이 값을 반환한다.
Number로 변환하고자 하면 valueOf를 toString에 앞서, String으로 변환하고자 하면 반대로 toString을 valueOf에 앞서 호출한다.
이러고도 원시 타입이 나오지 않으면 TypeError를 반환한다.
많은 내장 객체들이 valueOf가 정의되어 있지 않거나 (원시 타입이 아닌) this를 반환하는 경우가 많기 때문에, 어느 형변환을 하든 결과적으로 toString을 호출하게 된다.

각 연산자마다 preferredType을 지정해서 호출하지만, ==와 +는 preferredType에 default를 넘깁니다. 이 경우 Date를 제외한 타입은 Number로 변환된다.

 

예제)

4 + 10 + "string"               // "14string"
"string" + 4 + 10               // "string410"
"true" == true                  // false
undefined == ''                 // false
8 * null                        // 0
0 == "\n"                       // true
!![]+!!{}+!!"false"             // 3
~undefined                      // -1
[2] > "1"                       // true
"hello" > 3                     // false
"hello" < 3                     // false
"-1" > "+1"                     // true
"-1" > +1                       // false
"b" + "a" + + "a" + "a"         // "baNaNa"
[] + undefined + 1              // undefined1
[2,3,5] == [2,3,5]              // false
{}+[]+{}+[1]                    // "0[object Object]1"
!+[]+[]+![]                     // "truefalse"
!+[]+![]+[]                     // "1"
[1] + [2,3]                     // "12,3"
하나하나 분석해보도록 하겠습니다.

4 + 10 + "string"에선 4 + 10이 먼저 계산되어 14가 되고, 이후 14 + "string"이 되어 "14string"이 됩니다.

"string" + 4 + 10에선 "string" + 4가 먼저 계산되어 "string4"가 되고, 이후 "string4" + 10이 계산되어 "string410"이 됩니다. +에 String이 들어가면 계속 String이라 보시면 됩니다.

"true" == true에서, == 에 의해 numeric conversion이 일어나 "true"가 NaN이 되고 true는 1이 됩니다.

때문에 전체 식은 false가 됩니다.

undefined == ''에선, ==에 undefined가 있기 때문에 numeric conversion이 일어나지 않습니다. 전체 식은 false가 됩니다.

8 * null에선 null이 0으로 변환되어 전체 식이 0이 됩니다.

0 == "\n"에선 numeric conversion이 일어나 "\n"이 0으로 변환됩니다. 때문에 전체 식은 true가 됩니다.

!![]+!!{}+!!"false"에선 !!~sth~의 ~sth~가 Boolean으로 true로 변환되므로, 두 번 complement를 해 true + true + true가 됩니다. 이후는 numeric conversion이 일어나 3이 됩니다.

~undefined는 undefined가 NaN으로 형변환되고, 비트 연산에서 NaN이 0으로 간주되기 때문 ~NaN은 -1로 계산됩니다.

[2] > "1"의 경우, numeric conversion이 일어나 [2]는 valueOf 메서드에 의해 2로, "1"은 1로 변환되기 때문에 true가 됩니다.

"hello" > 3과 "hello" < 3에서 "hello"는 NaN으로 변환되기 때문에 비교 결과도 둘 다 NaN이 됩니다.

"-1" > "+1"는 conversion이 일어나지 않습니다. -의 ASCII 코드(45)가 +보다 크므로(43), true가 됩니다.

"-1" > +1는 타입이 일치하지 않으므로 numeric conversion이 일어납니다. 결과는 -1 > 1이 되어 false입니다.

"b" + "a" + + "a" + "a"는 서두의 그림에 있던 예시입니다. 흐름을 표현하면 다음과 같습니다.

>> "b" + "a" + + "a" + "a"
 - ("b" + "a") + + "a" + "a"
 - ("ba" + (+ "a")) + "a"
 - ("ba" + NaN) + "a"
 - "baNaN" + "a"
 - "baNaNa"
[] + undefined + 1에서 우선 [] + undefined이 계산됩니다. numeric conversion에 의해[].valueOf()가 호출되는데, 이는 자기 자신이므로 원시 타입이 아니어서 numeric conversion이 실패합니다. Number([])이 0임에도 불구하고 []가 object이기 때문에 그렇습니다. 때문에 string conversion이 일어나고 이 땐 "" + "undefined"가 되어 "undefined"가 됩니다. 이후 결과는 당연히 "undefined1"이 됩니다.

[2,3,5] == [2,3,5]는 타입이 같아서 형변환이 일어나지 않고, 둘이 같은 객체가 아니므로 false가 됩니다. 이와 달리 [2,3,5] == "2,3,5"는 string conversion이 일어나므로 true가 됩니다.

{}+[]+{}+[1]는 원 포스트 최상단에 있는 예제인데, 약간의 낚시가 들어가 있습니다. 우선, 첫 중괄호 ({})는 scope로 인식되어 연산에 아무런 영향이 없습니다. 실제 연산은 +[]부터 시작합니다.

>> +[]+{}+[1]
 - +''+{}+[1]       // numeric conversion에서 []이 toString에 의해 ''로 변환
 - +0+{}+[1]        // 이후 ''이 (계속된 numeric conversion에 의해) 0으로 변환
 - 0+{}+[1]         // {}이 toString에 의해 "[object Object]"로 변환
 - "0[object Object]" + [1]
 - "0[object Object]1"
!+[]+[]+![]도 위랑 비슷합니다. !+[]는 !0이 되므로 true가 되며, true+[]에서 []는 ''으로 변환되어 "true"가 됩니다. 이후 나머지도 String이 되기에 결과적으로 "truefalse"가 됩니다.

!+[]+![]+[]는 비슷하지만 약간 다릅니다. !+[]가 true, ![]는 false이므로 둘이 더해서 1이 되며, 이후 []가 ''으로 변환되어 결과적으로 "1"이 됩니다.

[1] + [2,3]에선 valueOf가 원시 타입을 반환하지 않으므로 toString이 사용되어 "1" + "2,3"이 되기에 "12,3"이 됩니다.

 

 

💁‍♀️  = =, = = = 
 

==는 Equal Operator이고,  ===는 Strict Equal Operator이다.

==는 a == b 라고 할때, a와 b의 값이 같은지를 비교해서, 같으면 true, 다르면 false라고 한다.(값만 같으면 true이다.)

 

===는 Strict, 즉 엄격한 Equal Operator로써, "엄격하게" 같음을 비교할 때 사용하는 연산자이다. 

===는 a === b 라고 할때, 값과 값의 종류(Data Type)가 모두 같은지를 비교해서, 같으면 true, 다르면 false라고 한다. 

 

💁‍♀️ 느슨한 타입의 동적언어의 문제점은 무엇이고 보완 할 수 있는 방법은 무엇이 있을까?
느슨한 타입(loosely typed)의 동적(dynamic) 언어의 문제점은

무엇이고 보완할 수 있는 방법 동적타입 언어는

런타임 시 확인할 수 밖에 없기 때문에, 코드가 길고 복잡해질 경우 타입 에러를 찾기가 어려워 진다.

-> 이러한 불편함을 해소하기 위해 TypeScipt나 Flow 등을 사용할 수 있다.

💁‍♀️ undefined와 null의 미세한 차이들을 비교해 보세요.
undefined 은 변수를 선언하고 값을 할당하지 않은 상태,

null 은 변수를 선언하고 빈 값을 할당한 상태(빈 객체)이다. 즉, undefined 는 자료형이 없는 상태이다.

 
2. JavaScript 객체와 불변성이란?
 

💁‍♀️ 기본형 데이터와 참조형 데이터

위 그림과 같이 자바스크립트의 데이터 타입에는 두 가지 종류가 있다. 기본형과 참조형이다.
기본형 (Primative Type)
기본형은 값을 그대로 할당한다.

Number
String
Boolean
Symbol(ES6에 추가, 객체 속성을 만드는 데이터 타입)
null
undefined
기본형 데이터는 값을 그대로 할당하고, 메모리상에 고정된 크기로 저장되며

원시 데이터 값 자체를 보관하므로, 불변적이다.

각각의 변수는 영역을 가지고 있고, 변수는 직접적으로 비교할 수 있다.
보통 같은 데이터는 하나의 메모리를 사용한다. (재사용이 가능)

참조형 (Reference Type)
값이 저장된 주소값을 할당 (참조)

Object
Array
Function
RegExp
Map
등등
참조형 데이터는 기본형의 데이터 집합이라 볼 수 있다.

메모리에 할당되는 과정은 기본형 데이터가 할당되는 과정과 비슷하다.

정리하자면, 비어있는 데이터 공간을 확보하고, 객체 속 프로퍼티에 대한 공간을 다시 확보한다.
객체의 프로퍼티 명과 주소를 매칭하고 확보했던 두번째 주소에 데이터를 할당한다.

전체적으로 비교하자면 변수를 선언하면 데이터가 담길 공간을 확보하고, 확보된 데이터의 주소값을 가지고 변수면과 매칭시키는 선언과정까지 동일하나, 할당과정에 차이를 갖는다.

💁‍♀️ 불변 객체를 만드는 방법
불변 객체 (Immutable Object)
객체 내부 프로퍼티를 변경할 때마다

새로운 객체를 만들어 재할당하기로 정하거나
자동으로 새로운 객체를 만드는 도구를 활용하여 (ex. immutable.js, immer.js 등의 라이브러리)
➡️ 불변성 확보

불변 객체가 필요한 경우
객체에 변화를 가해도 원본이 그대로 남아있어야 하는 경우
ex) 정보가 바뀌었으면 알림 전송하는 경우, 바뀌기 전의 정보와 바뀐 후의 정보를 보여줘야하는 경우 등

var user = {
  name: "namju",
  gender: "male",
};

var changeName = function (user, newName) {
  var newUser = user;
  newUser.name = newName;
  return newUser;
};

var user2 = changeName(user, "yun");

// 아래의 if문은 무시되어 지나침
if (user !== user2) {
  console.log("유저 정보가 변경되었습니다.");
}

console.log(user.name, user2.name); // yun yun
console.log(user === user2); // true
➡️ 유저 정보가 변경되었음을 감지하지 못함!

불변 객체 만들기
새 객체를 하드코딩
var user = {
  name: "namju",
  gender: "male",
};

var changeName = function (user, newName) {
  return {
    name: newName,
    gender: user.gender,
  };
};

var user2 = changeName(user, "yun");

if (user !== user2) {
  console.log("유저 정보가 변경되었습니다."); // 유저 정보가 변경되었습니다.
}

console.log(user.name, user2.name); // namju yun
console.log(user === user2); // false
➡️ 👎 객체에 프로퍼티가 많을수록 하드코딩해야하는 수고가 너무 늘어남
프로퍼티 개수에 상관 없이 모든 프로퍼티를 복사하는 함수를 만드는 것이 좋음

💁‍♀️ 얕은 복사와 깊은 복사
바로 아래 단계의 값들만 복사하는 방법

: for in 반복문으로 새 객체에 원래 객체의 프로퍼티들을 복사하는 함수

var copyObject = function (target) {
  var result = {};
  for (var prop in target) {
    result[prop] = target[prop];
  }
  return result;
};
이 함수를 이용해 새로운 객체를 만들어 프로퍼티를 변경할 수 있음

var user = {
  name: "namju",
  gender: "male",
};

var user2 = copyObject(user);
user2.name = "yun";

if (user !== user2) {
  console.log("유저 정보가 변경되었습니다."); // 유저 정보가 변경되었습니다.
}

console.log(user.name, user2.name); // namju yun
console.log(user === user2); // false
👎 이 방법의 단점

프로토타입 체이닝 상의 모든 프로퍼티를 복사
getter / setter는 복사하지 않음
얕은 복사만 수행함
➡️ 게다가 협업하는 모든 개발자들에게 무조건 copyObject 함수를 사용하기로 합의시키는 것이 어려움!

프로토타입 체이닝
모든 객체(함수 포함)에는 프로토타입 객체가 포함되어 있음
그렇기 떄문에 얕은 복사를 한 객체는 부모(원본) 객체의 프로토타입에도 접근할 수 있어짐
(스코프 체이닝처럼 계속 상위로 가서 탐색을 하는 식)

깊은 복사
내부의 모든 값들을 하나하나 찾아서 전부 복사하는 방법

얕은 복사 만으로는 중첩된 객체를 제대로 복사할 수 없음 (바로 아래 단계의 값들만 새로운 데이터 주소로 복사시키는 것)

var user = {
  name: "namju",
  info: {
    hobby: "bike",
    location: "seoul",
    happy: true,
  },
};

var user2 = copyObject(user);
user.name = "yun namju";
user.info.hobby = "read";
user.info.location = "busan";

console.log(user.name === user2.name); // false
console.log(user.info.hobby === user2.info.hobby); // true : 두 객체가 모두 변경됨
console.log(user.info.location === user2.info.location); // true : 두 객체가 모두 변경됨
한 단계 더 nesting 된 info 객체의 프로퍼티들에는 기존의 데이터를 그대로 참조하고 있는 것!
➡️ 이런 nested 된 모든 프로퍼티들에 대한 복사를 재귀적으로 수행해야 깊은 복사가 됨

 

객체의 깊은 복사를 수행하는 함수

var copyObjectDeep = function (target) {
  var result = {};

  if (typeof target === "object" && target !== null) {
    for (var prop in target) {
      result[prop] = copyObjectDeep(target[prop]); // 재귀적 호출
    }
  } else {
    result = target;
  }

  return result;
};
➕ hasOwnProperty 메서드를 통해 프로토타입 체이닝을 통해 상속된 프로퍼티는 복사하지 않도록 할 수 있음
➕ ES6, ES2017의 경우 Object.getOwnPropertyDescriptor, Object.getOwnPropertyDescriptors를 통해 getter/setter를 복사할 수 있음

 

✨ 깊은 복사를 하는 다른 방법 - JSON

객체를 JSON 문법의 문자열로 만들었다가 다시 JSON 객체로 만드는 것 (JSON.stringify, JSON.parse)

메서드, __proto__, getter/setter는 JSON으로 변경 불가능하여 무시됨
httpRequest로 받은 데이터 등의 순수한 정보를 다룰 때 활용
 
3. 호이스팅과 TDZ는 무엇일까?
💁‍♀️ 스코프, 호이스팅, TDZ
호이스팅(Hoisting)의 개념

함수 안에 있는 선언들을 모두 끌어올려서 해당 함수 유효 범위의 최상단에 선언 하는것을 말한다.
var 변수 선언과 함수선언문에서 호이스팅이 일어난다.
let/const 변수 선언도 호이스팅은 되지만 TDZ에 의해 ReferenceError가 발생한다.
함수표현식은 호이스팅이 일어나지 않음
함수표현식보다 함수선언문을 더 자주 사용하자.

 

TDZ(Temporal Dead Zone)?

일시적인 사각지대라는 뜻, 스코프의 시작 지점 부터 초기화 시작 지점까지의 구간
var은 선언과 초기화를 동시에 하므로 undefined/
let은 선언과 초기화가 분리되어 참조 에러(ReferenceError)
const는 선언+초기화+할당 동시에 해야 에러가 안남 const name =jin
javascript에서의 변수는 선언,초기화,할당 이라는 3가지 단계의 걸쳐서 생성
스코프(Scope)?

'범위' 라는 뜻. 즉, 스코프(Scope)란 '변수에 접근 할 수 있는 범위'.

자바스크릅트에서는 스코프는 2가지 타입이 있다.

바로 global(전역)과 local(지역)

var a = 1; // 전역 스코프
function prin() { // 지역(함수)스코프
	var a = 111;
    console.log(a);
}
print();
console.log(a);
💁‍♀️ 함수 선언문과 함수 표현식에서 호이스팅 방식의 차이
함수 선언식과 함수표현식이란?
함수 선언식 (function declartion)

함수명이 정의되어 있고, 별도의 할당 명령이 없는 것

function sum(a,b) {
    return a + b;
}
함수 표현식 (function Expression)

정의한 function을 별도의 변수에 할당하는 것

const sum = function(a,b) {
    return a + b;
}
함수 선언식과 함수 표현식의 차이
주요 차이점은, 호이스팅에서 차이가 발생합니다.

함수 선언식은 함수 전체를 호이스팅 합니다. 정의된 범위의 맨 위로 호이스팅되서 함수 선언 전에 함수를 사용할 수 있다는 것입니다.

함수 표현식은 별도의 변수에 할당하게 되는데, 변수는 선언부와 할당부를 나누어 호이스팅 하게 됩니다. 선언부만 호이스팅하게 됩니다.

💁‍♀️ let, const,var,function이 어떤 원리로 실행되는지 알 수 있다.
💁‍♀️ 실행 컨텍스트와 콜 스택
Execution context(실행 컨텍스트)

자바스크립트 코드가 실행되는 환경을 의미한다.
자바스크립트에서 대표적으로 두 가지 타입의 Execution context가 있다.

실행할 코드에 제공할 환경 정보들을 모아놓은 객체들로
자바스크립트의 동적 언어로서의 성격을 가장 잘 파악할 수 있는 개념이다.

Global Execution context
자바스크립트 엔진이 처음 코드를 실행할 때 Global Execution Context가 생성된다. 생성 과정에서 전역 객체인 Window Object (Node는 Global) 를 생성하고 this가 Window 객체를 가리키도록 한다.
Function Execution context
자바스크립트 엔진은 함수가 호출 될 때마다 호출 된 함수를 위한 Execution Context를 생성한다.
모든 함수는 호출되는 시점에 자신만의 Execution Context를 가진다.
자바스크립트는 실행 컨텍스트가 활성화되는 시점에 다음과 같은 현상이 발생한다.

호이스팅이 발생한다(선언된 변수를 위로 끌어올린다)
외부 환경 정보를 구성한다
this 값을 설정한다.
call stack
코드가 실행되면서 생성되는 Execution Context를 저장하는 자료구조

엔진이 처음 script를 실행할 때, Global Execution Context를 생성하고 이를 Call Stack에 push한다.

그 후 엔진이 함수를 호출할 때 마다 함수를 위한 Execution Context를 생성하고 이를 Call Stack에 push 한다.

자바스크립트 엔진은 Call Stack의 Top에 위치한 함수를 실행하며 함수가 종료되면 stack에서 제거(pop)하고 제어를 다음 Top에 위치한 함수로 이동한다.

1줄 요약 : 프로그램이 함수 호출을 추적할때 사용한다.

 


💁‍♀️ 스코프 체인, 변수 은닉화
스코프 체인(scope chain)이란?
스코프 체인(Scope Chain)은 일종의 리스트로서 전역 객체와 중첩된 함수의 스코프의 레퍼런스를 차례로 저장하고, 의미 그대로 각각의 스코프가 어떻게 연결(chain)되고 있는지 보여주는 것을 말한다.

하지만 스코프 체인(scope chain)을 이해하기 위해서 먼저 자바스크립트의 실행 컨텍스트(Execution context)를 알아야 한다.

그렇다면 실행 컨텍스트란 무엇인가? 
실행 컨텍스트(Execution context)는 우리가 작성한 코드가 실행되는 환경을 말하며, scope, hoisting, this, function, closure 등의 동작원리를 담고 있는 자바스크립트의 핵심원리를 말한다.

 

4. 실습 과제
 

콘솔에 찍힐 b 값을 예상해보고, 어디에서 선언된 “b”가 몇번째 라인에서 호출한 console.log에 찍혔는지, 왜 그런지 설명해보세요. 주석을 풀어보고 오류가 난다면 왜 오류가 나는 지 설명하고 오류를 수정해보세요.

let b = 1;

function hi () {
	const a = 1;
	let b = 100;
	b++;
	console.log(a,b);
}

//console.log(a);
console.log(b); 
hi();
console.log(b);
출력)

let b = 1;

function hi () {
	const a = 1;
	let b = 100;
	b++;
	console.log(a,b);
}

//console.log(a);
console.log(b); //1이 출력됨
hi(); // console.log(a,b); 이 출력됨. 1, 101
console.log(b); // 첫 줄 let b = 1; 이 출력됨. 1
console.log 주석 풀고 오류나는 이유 )

let b = 1;

function hi () {
	const a = 1;
	let b = 100;
	b++;
	console.log(a,b);
}

console.log(a); // a가 지역(local)스코프로 선언되어 바깥의 범위에서는 undefined.
console.log(b); 
hi();
console.log(b);
답안 )

let b = 1;
let a = 1; // a가 전역(global)스코프로 선언되어 바깥의 범위에서 1 출력
function hi () {
	const a = 1;
	let b = 100;
	b++;
	console.log(a,b);
}

console.log(a);
console.log(b); 
hi();
console.log(b);