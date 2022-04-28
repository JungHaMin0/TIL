### 타이머함수
### setTimeout(함수, 시간): 일정 시간 후 함수 실행
### setInterval(함수, 시간): 시간 간격마다 함수 실행
### clearTimeout(): 설정된 TimeOut 함수를 종료
### clearInterval(): 설정된 Interval 함수를 종료

    setTimeout(function () {}, 3000)
    //3000 = 3초

    setTimeout(function () {
        console.log('hamin!')
    }, 3000)
    => 3초후 hamin! 출력

    setTimeout(() => {
        console.log('hamin!')
    }, 3000)
    => 3초후 hamin! 출력

    const timer = setTimeout(() => {
        console.log('hamin!')
    }, 3000);

    const btnEl = document.querySelector('button')
    btnEl.addEventListener('click', () => {
        clearTimeout(timer)
    })

button클릭 시 타이머 종료.

3초마다 hamin! 실행  
    const timer = setInterval(() => {
        console.log('hamin!')
    }, 3000);

    const btnEl = document.querySelector('button')
    btnEl.addEventListener('click', () => {
        clearInterval(timer)
    })  
버튼 클릭 시 3초마다 출력되던 것이 멈춰짐.
이러한 타이머함수가 실제로 많이 쓰인다.