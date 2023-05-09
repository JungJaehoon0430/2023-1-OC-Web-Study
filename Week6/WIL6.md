복습

CSS
서열 관계 존재(우선순위)
1. 상속
2. 우선순위
1) 사용자 스타일 (컴퓨터 사용자)
2) 제작자 스타일 (개발자)
3) 브라우저 기본 스타일

select
id 선택자
클래스 선택자
타입 선택자
전체 선택자

서열
인라인 스타일 -> 아이디 선택자 -> 클랙스 선택자 -> 타입 선택자

본수업

box model

dev 보이지 않는 박스 안에
body tag 얘도 박스

1. 블록 레벨 요소
한 줄을 차지하는 박스(body, div, p, h5 등)
부모 요소 전체 공간 차지
2. 인라인 레벨 요소
자신만을 감싸는 요소(span, strong 등)

margine : 요소간의 여백(content간의 여백)
border : 테두리(종류 여러개)
padding : content와 border 사이의 간격, 넓게 하면 사이 간격 늘어남
content : strong같은거 안에 있는 거

top -> right -> bottom -> left
margin: 10px 30px 0 20px
margine: 10px 30px <!--위 아래 10px, 오른쪽 왼쪽 30px-->

개발자 도구에서 요소 볼 수 있음
스타일에 맨 밑에 박스 스타일에서 볼 수 있음
디버깅에도 유용

FLEX Box Layout
Flexible Layout
아이템이 배열된 방향인 '주축'을 정할 수 있다
주축과 수직한 축을 across axis라 부름
가로 row
세로 column
.flex-box {
    display: flex
    flex-direction: row
}<!--가로로 배열-->

justify-content: flex-end 끝에 배열 외울 필요 X

저주 콘서트
크로스-라인

저스티파이 : 주축
얼라인 : 크로스축

column이랑 row로 주축 계속 바꿔가면서 

더 알면 좋은 것 - 프론트엔드 할거면
1. css grid rayouts
2. can i use? 어느 브라우저 몇번째 버전부터 쓸 수 있는지 알 수 있음