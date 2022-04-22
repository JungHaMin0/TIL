### 화살표 함수


    const double = function (x) {
        return x*2
    }
    cosole.log('double: ', double(7))


함수를 double에 저장하는 방식
일반적인 함수 사용 방식.  


    const doubleArrow = (x) => {
        return x*2
    }
    console.log('doubleArrow', doubleArrow(7))

function 대신 ' => '

일반함수와 화살표 함수 차이
1. 축약형으로 코딩 가능.  
    const doubleArrow = (x) => return x*2   
    const doubleArrow = x => x*2 (괄호도 생략 가능)  

2. 축약형 - {} 

    const doubleArrow = x => {
        name: 'hamin'
    }  
이렇게하면 undefined가 나옴  
*솔루션: 괄호안에 대괄호를 넣어준다.
    const doubleArrow = x => ({
        name: 'hamin'
    })  
이 부분만 조금 주의하면서 작성하자.

