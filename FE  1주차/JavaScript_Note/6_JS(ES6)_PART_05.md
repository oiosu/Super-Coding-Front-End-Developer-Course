### 6_JS(ES6)_PART_05

> * 자바스크립트 언어의 특징
> * 컴파일러 vs 인터프리터 
> * JIT 컴파일러 



✔ 공부방법 참고하기 

* 블로그에 공부한 내용을 정리해 보기 (나의 언어로)

  > 이글의 목적, 이글의 예상 독자, 인트로, 당연한 문제 등
  > ___어떤 문제를 마주했고 어떻게 해결하고자 노력했는지 작성
  >
  > *  실제 코드를 첨부하면서 글 작성 
  > * 간단하게 만든 프로젝트든, 컨퍼런스 내용이든 어떤 주제든 상관없으니 블로그 작성하면서 정리하는 시간 가지기 

* Rubber Duck Debugging

  > 발생한 오류를 오리에게 설명하기 
  >
  > 학습한 것에 대해 말로 설명하는 것 중요 

* 세미나, 컨퍼런스 참여해보기 





##### 1. 자바스크립트 언어의 특징

##### (1) 하이 레벨 언어 

* 로우 레벨 : 메모리를 직접 관리 (c관리)

  > 운영체제에 가까울 수록 로우 레벨, 어플리케이션에 가까울수록 하이레벨이라고 한다. 
  >
  > 로우 레벨 같은 경우에는 메모리를 직접 관리를 해줘야 한다. 이러한 점들을 개선하기 위해 나온 것이 하이 레벨 이다. 
  >
  > 하지만 자바스크립트는 메모리 자동 관리가 되어진다. 

* 메모리 자동 관리 

* 성능이 낮음



##### (2) 인터프리터 언어 

* 머신 코드 : 컴퓨터가 이해할 수 있는 0, 1 로만 이루어진 코드 
* js는 인터프리터 언어, 컴파일이 필요없음 



##### (3) 가비지 콜렉션

* 사용하지 않는 객체를 자동으로 제거 



##### (4) 멀티 패러다임 

* 절차지향 프로그래밍 
* 객체지향 프로그래밍
* 함수형 프로그래밍
* JS는 전부 가능 



##### (5) 프로토타입 기반 

* 자바스크립트에 있는 건 거의 다 객체 (원시 타입 제외)
* Array.prototype.push 



##### (6) 일급 함수 

* 함수를 변수처럼 처리 
* 함수를 다른 함수 안으로 처리 가능
* 함수에 함수로 반환 가능 



##### (7) 동적 

* 변수에 데이터타입 할당하지 않음 
* 런타임에서 타입을 알 수 없음 



##### (8) 싱글 쓰레드 

* 동시성 모델 : 자바스크립트 엔진이 여러 태스크 동시처리 
* 하나의 쓰레드는 하나의 일만 함 



##### (9) 논 블로킹 

* 이벤트 루프를 통해 오래 걸리는 작업 

  (데이터 패칭 등)은 백그라운드 실행 



---



##### 2. 컴파일러 vs 인터프리터 

> 대부분의 언어는 컴파일러로 처리를 한다. 
>
> 컴퓨터가 코드를 이해하는 것 0 과 1 머신코드
>
> 이러한 머신코드인 0과 1로 전환해주는 과정을 컴파일러 라고 한다.
>
> (소스코드 =======> 머신코드)
>
> 머신코드를 기반으로 처리를하여 프로그램을 실행한다. 

> 컴파일러와 인터프리터의 큰 차이점은 `머신코드 처리` 과정이 없는 것이다. 하지만 인터프리터에서 머신코드가 없는 것은 아니다. 다만, 
>
> 인터프리터는 소스 코드를 한줄 한줄 씩 실행을 하면서 바로 처리

##### 🔻 컴파일러 

: 전체 코드가 한 번에 머신 코드로 실행

: 바이너리 파일로 쓰여짐

: 컴파일 이후에 실행이 가능 

![image](https://github.com/oiosu/SC-HALF-FE/assets/99783474/d07e4520-2dea-48ad-9291-81bef46676c1)


##### 🔻 인터프리터 

: 한 줄씩 소스 코드를 읽으면서 실행

: 컴파일러에 비해 속도가 느림 

: 변경 사항을 빠르게 테스트 가능 

![image](https://github.com/oiosu/SC-HALF-FE/assets/99783474/967bc92b-4132-4370-921d-d1df2eb0b2ab)

---

##### Q. 자바스크립트는 인터프리터 언어인가요? 

===> 맞다 하지만, 크롬 V8 엔진이 나온 이후로는 컴파일도 같이 진행한다. 

===> 성능 최적화를 해주기 위함이다. 

---



##### 3. JIT(Just-In-Time) 컴파일러 

![image](https://github.com/oiosu/SC-HALF-FE/assets/99783474/32889d99-ecfb-4d1f-af7d-642cdac74e54)


* ##### JS엔진

![image](https://github.com/oiosu/SC-HALF-FE/assets/99783474/69b893ba-619e-4666-bfd9-4cd9da5c874d)


> 자바스크립트 엔진에서 소스코드를 작성하고 그 소스코드가 파싱이된다.
>
> > (let, const, var 기준으로) 파싱(=변환한다)  
> >
> > ====> AST 형태로 변환한다.
> >
> > AST (=추상구문트리)
>
> 변환된 AST 코드를 머신코드로 변환을 한다. 
>
> JIT 컴파일러에서는 컴파일을 한 후 머신코드를 바로 실행한다. 
>
> 그리고 실행이 되고 나서 `최적화` 과정을 거친다. 
>
> 최적화를 거칠때마다 이 엔진은 자바스크립트 코드를 향상시키는 방향으로 진화를 하게 된다. 
>
> JS 엔진 내부 
>
> ![image](https://github.com/oiosu/SC-HALF-FE/assets/99783474/846334a7-7b75-45a2-a88c-9c3d35198bbe)





> ##### ◼ 레퍼런스 참고하기 
>
> - 자바스크립트 코드 실행 동작 원리 : 엔진, 가상머신, 인터프리터, AST 기초 (https://curryyou.tistory.com/237)
> - 자바스크립트, 인터프리터 언어일까? (https://www.oowgnoj.dev/review/advanced-js-1)



---



##### ◼ Summary

> * 자바스크립트 언어의 특징 9가지 
> * 컴파일러와 인터프리터의 차이, 가장 큰 차이는 머신 코드 유무
> * JIT 컴파일러가 왜 생겼고 무엇인지
