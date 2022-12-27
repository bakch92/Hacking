# 리액트 Component

## Component란?
긴 HTML을 한 단어로 깔끔하게 치환하여 넣을수 있는 문법으로 모듈 형식으로 HTML을 가져다 쓸수 있음

## 사용법
1. function을 이용하여 함수를 하나 만듬
2. 함수 안에 return( HTML 코드) 담음
3. 메인 HTML 코드 원하는 곳에 <함수명/> 사용하여 축약한 HTML 삽입


    function App (){
        return (
        <div>
          (생략)
          <Modal></Modal>
        </div>
        )
    }
    function Modal(){
        return (
          <div className="modal">
          <h4>제목</h4>
          <p>날짜</p>
          <p>상세내용</p>
        </div>
        )
    }


## Component 만들때 주의점
1. Component 첫 글자는 대문자로 작명하는 것이 규칙
2. return () 안에 html 태그를 평행하게 여러개 들어가게 할 수 없음
3. function App(){} 내부에서 만들면 안됨(이유는 App(){} 함수도 Component 생성 문법이기 때문)