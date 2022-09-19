Number.isNaN(1);
NaN 함수는 여부 검사를 보다 직관적인 방식.

isFinite(NaN)
isFinite()함수는 NaN 값을 테스트 가능.

for-of
for(let value of array){
    //value로 작업을 실행
}

for-in
for(let property in object) {
    //object의 항목(property)으로 작업 실행
}

스코프(즉 함수의 범위)
global(전역)
local(지역)

1)
var name = 'abc'
function log() {
    console.log(name);
}

function wrapper() {
    name = 'cba'
    log();
}

wrapper();

=> cba

2)
var name = 'abc'
function log() {
    console.log(name);
}

function wrapper() {
    var name = 'cba'
    log();
}

wrapper();

=> abc

[lexcial scoping]
내부에서 선언한 것이 외부로 나갈 시 초기화 됨
즉 정적인 스코프. 

1번 예제를 보면 블록 안에서 'var' 이렇게 선언이 아닌 값을 cba로 바꿔주는 것이기에 정상적인 스코프.

2번 예제를 보면 블록 안에서 'var' 선언이 된다.
스포프는 호출이 아닌 선언 기점으로서, 블록 밖으로 값이 나가면 적용이 안된다.

### [콜백함수]
> 파라미터로 함수를 전달받아, 함수 내부에서 실행하는 함수.

```
let number = [1, 2, 3, 4, 5];

number.forEach(function(x) {
    console.log(x * 2);
});

```

콜백을 쓰는 이유가 A의 작동이 될 때 B의 작동을 비동기로 즉시 처리할 때를 위함이다.

number가 작동 됨과 동시에 함수가 실행시켜져 number가 작동 시 비동기로 console.log가 찍히게 된다.






