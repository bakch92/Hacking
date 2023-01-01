# 반복되는 HTML 코드를 반복문으로 줄이고 싶을 때
## Array의 map 함수를 이용하여 반복문으로 축약 가능
아래와 코드처럼 map 함수를 사용하며 콜백 함수 내 a 파라미터는 실제 글제목 state 내 각 elemnt 요소의 값이고
i는 index 값

    function App (){
    let [글제목, 글제목변경] = useState(['남자 코트 추천', '강남 우동 맛집', '파이썬독학']);
    return (
        <div>
        (생략)
        { 
            글제목.map(function(a,i){
                return (
                    <div className="list" key={i}>
                        <h4>{a}</h4>
                        <p>2월 18일 발행</p>
                    </div> )
            }) 
        }
        </div>
        )
    }