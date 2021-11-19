Redux
====

어플리케이션의 state를 관리하고 업데이트 해주는 상태관리 라이브러리.

Redux가 필요한 이유
----
state를 부모에서 만들면 자식에게 계속 props로 계속 전송 전송해줘야 한다.(계속 중첩되면 복잡해짐 )

리덕스는 일일히 prop로 전달해주지 않아도 된다. 
리덕스는 'state 보관함'(store.js)-> state를 직접 꺼내 쓸 수 있다. 

Redux 사용방법
----
컴포넌트에서 state 수정요청(reducer에서 만든)을 하려면 dispatch를 쓴다. 