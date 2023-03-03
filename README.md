### HTTP란 무언인가?
- HyperText Transfer Protocol의 약자로 웹에서 데이터를 주고 받을 수 있는 프로토콜, 즉 하나의 규칙이다. Request <-> Response </br>
#### ※ https란 통신 보안이 더 강화된 hhtp라 볼 수 있다.

### Get과 Post란?
- Get은 url에 데이터를 붙혀서 서버에 전송하는 반면에 Post는 body안에서 전송되기에 보안쪽으로는 post가 낫다. 용도로는 Get은 서버로부터 데이터를 불러오는 용도(읽기)로 사용되고 Post는 게시판 글 작성, 회원 가입 등 서버에 데이터를 전송/수정 용도 (쓰기)로 사용된다. 

### CORS란?
- Cross-Origin Resource Sharing의 약자로 출처가 다른 곳에서 데이터를 주고 받을 수 있도록 허용해주는 정책이다. 기존에는 보안상 서로 다른 출처에서 리소를 주고 받는 것이 제한되었지만, 지금은 서로 다른 출처에서도 통신이 필요하기에 이러한 문제를 해결하기 위해서 나온 정책이다. 여기에서 출처란, URL에서 프로토콜, 도메인, 포트번호가 같은것을 의미한다.
