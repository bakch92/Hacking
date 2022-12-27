# 리액트 Prpos 문법

## 부모 컴포넌트(App) 의 state를 자식 Component 가 가져다 쓰려면?
리액트에서는 일반 JS 문법처럼 정의된 변수를 바로 가져다 쓸수 없어 props 문법을 이용하여 부모 컴포넌트에서 자식 컴포넌트로 state를 넘겨줘야 한다.

## 사용법
사용법은 아래 코드처럼 부모 컴포넌트의 html 내 자식 컴포넌트 부분에 작명을 하여 state를 넘겨준 후, 자식 컴포넌트에서 props를 파라미터에 정의하여 html 코드 내 중괄호{} 이용하여 state를 사용한다.

    function App (){
        let [글제목, 글제목변경] = useState(['남자코트 추천', '강남 우동맛집', '파이썬독학']);
        return (
            <div>
                <Modal 글제목={글제목}></Modal>
            </div>
        )
    }

    function Modal(props){
        return (
            <div className="modal">
                <h4>{ props.글제목[0] }</h4>
                <p>날짜</p>
                <p>상세내용</p>
            </div>
        )
    }