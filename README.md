## Front

### HTTP란 무언인가?
- HyperText Transfer Protocol의 약자로 웹에서 데이터를 주고 받을 수 있는 프로토콜, 즉 하나의 규칙이다. 브라우저 Request <-> 서버 Response </br>
#### ※ https란 통신 보안이 더 강화된 hhtp라 볼 수 있다.

### Get과 Post란?
- Get은 url에 데이터를 붙혀서 서버에 전송하는 반면에 Post는 body안에서 전송되기에 보안쪽으로는 post가 낫다. 용도로는 Get은 서버로부터 데이터를 불러오는 용도(읽기)로 사용되고 Post는 게시판 글 작성, 회원 가입 등 서버에 데이터를 전송/수정 용도 (쓰기)로 사용된다. 

### CORS란?
- Cross-Origin Resource Sharing의 약자로 출처가 다른 곳에서 데이터를 주고 받을 수 있도록 허용해주는 정책이다. 기존에는 보안상 서로 다른 출처에서 리소를 주고 받는 것이 제한되었지만, 지금은 서로 다른 출처에서도 통신이 필요하기에 이러한 문제를 해결하기 위해서 나온 정책이다. 여기에서 출처란, URL에서 프로토콜, 도메인, 포트번호가 같은것을 의미한다.

### DOM이란?
- document object modal의 약자로 문서객체모델, 즉 웹 페이지의 태그들을 자바스크립트가 읽을 수 있도록 브라우저가 트리구조로 만든 객체 모델이다.

### SPA란?
- Single Page Application의 약자로 하나에 페이지에서 스크립트로 컨텐츠를 동적으로 변경하여 보여주는 어플리케이션 ( 반대로는 MPA - Multi Page Appcation 웹 페이지 화면 마다 html 문서를 각 각 보여주는 어플리케이션 ) 장점으로는 서버가 해야할 일을 클라이언트가 부담하므로 서버 부담이 덜하나 단점으로는 초기에 모든 리소스를 한번에 다 내려받아야 하기에 초기 구동 속도가 느릴 수 있다. 그치만 이 문제는 Webpack의 code splitting으로 해결 가능 )

### 만약 주소창에 google.com을 검색하였을 경우 렌더링이 일어나는 과정은?
- 브라우저는 웹에서 google.com이라는 도메인으로 해당 페이지를 찾아와서 HTML과 CSS파일을 받아와서 해석 즉 파싱(parsing)하여 각각 Tree를 만든다. 파싱 단계는 Html 파일을 해석하여 DOM Tree를 구성하는 단계이다. 만약 CSS가 포함되어 있다면 CSSOM(CSS Object Modal) Tree 구성 작업도 함께 진행한다. 그리고 그 두 트리(Dom Tree + CSSOM Tree)를 결합하여 랜더링 트리를 만든다(style). 렌더링 트리는 실제로 화면에 그려질 트리. 그리고 랜더링 트리에서 각 노드위 위치와 크기를 계산(레이아웃), 계산된 값을 이용해 각 노드를 화면 상의 실제 픽셀로 변환하고 레이어를 만든다 (페인트). 마지막으로 레이어를 합성하여 실제 화면에 나타낸다 (Composite)

### 브라우저 저장소 ( 로컬스토리지, 세션스토리지, 쿠키 ) 각 차이점은?
-

### 명령형 / 선언형 프로그래밍의 차이점은?
- 명령형 프로그래밍(객체 지향 프로그래밍)은 어떻게(how) 할 것인가에 가깝고 선언형 프로그래밍(함수형 프로그래밍)은 무엇을(what) 할 것인가에 가깝다. 선언형 프로그래밍은 과정 보다는 결과가 중요하다. React는 선언형 프로그래밍

## JavaScript

### 호이스팅이란?
- 함수 선언문 

### 클로저란?
- 함수를 호출하는 위치가 아닌 정의하는 위치에서 해당 함수에 부모 함수에서 정의
된 변수에 접근할 수 있는 내부 함수를 뜻함. 클로저는 3가지 스코프를 갖는다. 본인(로컬)에서 정의된 변수, 부모 함수(클로저)에서 정의된 변수, 전역(글로벌)에서 정의된 변수

### This란?
- 기본적으로는 window 를 가리키지만 객체에서 this란 해당 메서드를 참조하는 객체 그 자체를 가리킨다 

### 이벤트 버블링이란?
-

### strict 모드란 ?
- 

### Promise의 3가지 상태
- Pending(대기) : 비동기 처리 로직이 완료되지 않은 상태 Fulfilled(이행) : 비동기 처리가 완료되어 Promise가 결과 값을 반환해준 상태 Rejected실패) : 비동기 처리 실패

## React

### state 원리는?
-리액트에서 동적으로 데이터 변화가 필요할 때 일반적인 자바스크립트 방법( 컴포넌트 내부에서 함수로 데이터 값을 재 할당 )으로는 변화가 일어나지 않다. 리액트가 해당 코드를 평가하고 화면에 랜더링을 하면 그 이후에 특정 이벤트로 변수의 값이 변화가 되어도 해당 컴포넌트는 다시 호출 되지 않는다. 그 이유는 클릭 이벤트 또는 변수의 값이 바뀌었을 때 해당 컴포넌트 함수를 다시 실행하라고 트리거 하지 않기 때문이다. 그래서 그런 상황이 필요할 경우 리액트 라이브러리중 useState를 사용해야한다. state의 값이 useState로 인하여 변경이 되면 리액트는 해당 컴포너를 재 평가하도록 하여 바뀐 데이터 값을 화면에 재 랜더링 한다. 이 때 useState는 반드시 컴포넌트 함수 안에서 호출되어야 한다
