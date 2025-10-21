

<h5 align="left">Webpack</h5>
<p align="left">
   <span>노트 정리 : <a href="https://justin-jig.github.io/justin-book/front/core/">https://justin-jig.github.io/justin-book/front/core/</a></span><br/>
</p>

#### 개념
js 소스 예제

변수 선언 variable declaration이란 변수를 생성하는 것을 말한다.

값을 저장하기 위한 메모리 공간을 확보(allocate)
변수 이름과 확보된 메모리 공간의 주소를 연결 (name binding)
변수 선언에 의해 확보된 메모리 공간은 확보가 해제(release)되기 전 까지는
누구도 확보된 메모리 공간을 사용할 수 없도록 보호되므로 안전하게 사용 할 수 있다.

변수를 사용하려면 반드시 선언이 필요하다.

변수를 선언할 때는 var, let const 키워드를 사용한다.
ES6 이전에는 전역 변수 var 키워드를 사용해 선언
ES6 이후에는 let,const,var 키워드를 통해 사용한다.

변수 var let, const 
var는 블록 레벨 스코프 (block-level scope)를 지원하지 않고
함수 레벨 스코프 (function-level scope)를 지원한다.

자바스크립트 엔진은 변수 선언을 다음과 같은 2단계에 거쳐 수행한다.

- 선언 단계 : 변수 이름을 등록해서 자바스크립트 엔진에 변수의 존재를 알린다.
- 초기화 단계 : 값을 저장하기 위한 메모리 공간을 확보하고 암묵적으로 undefined를 할당해
초기화한다.


변수 이름은 어디에 등록되는가?

변수 이름을 비롯한 모든 식별자는 실행 컨테스트에 등록된다.
실행 컨테스트(execution context)는 자바스크립트 엔진이 소스코드를 평가하고
실행하기 위해 필요한 환경을 제공하고 코드의 실행 결과를 실제로 관리하는 영역이다.
자바스크립트 엔진은 실행 컨테스트를 통해 식별자와 스코프를 관리한다.
변수 이름과 변수 값은 실행 컨텍스트 내에 키key/값 value 형식인 객체로 등록되어 관리함.
