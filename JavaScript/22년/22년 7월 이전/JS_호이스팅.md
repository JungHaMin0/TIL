### 호이스팅(Hoisting)
### 함수 선언부가 유효범위(Scope) 최상단으로 끌어올려지는 현상

호이스팅이란?  

    const a = 7

    double()

    const double = function() {
        console.log(a*2)
    }  
=> 오류  

함수 표현을 사용했을 때 double()을 위에서 사용 불가

    const a = 7

    double()

    function double() {
        console.log(a*2)
    }  
=> 14  

이러한 경우는 호이스팅이 발생해서 실행이 가능하다.  
호이스팅이 필요한 이유는 함수 안에 많은 로직들이 있을텐데 그 아래 호출을 하면 로직들을 지나야 호출을 볼 수 있기에 그 위에 호출을 정의 해서 쉽게 찾을 수 있게 하는 용도

