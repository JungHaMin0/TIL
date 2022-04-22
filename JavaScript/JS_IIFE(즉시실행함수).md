### 즉시실행 함수
### IIFE, Immediately-invoked Function Expession

    const a=7
    function double() {
        console.log(a*2)
    }
    double()  
우리가 함수를 실행하고 그 이후에는 쓸 일이 없다할 때 쓰는 IIFE  
즉 함수를 만들자마자 바로 실행하는 방법

1. ()()
    const a=7
    (function () {
        console.log(a*2)
    })()  

2. (()) 
    const a=7
    (function () {
        console.log(a*2)
    }())  

즉시실행 함수에 2가지 방법이 있고 2번 방법으로 자주 작성하자