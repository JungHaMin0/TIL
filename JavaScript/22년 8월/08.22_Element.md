## 2022년 8월 22일 TIL(다시시작)
### 메모 저장 기능이 있는 캘린더 토이 프로젝트 중..

- 1. 캘린더 for문
캘린더를 작성 시 이 중 for문을 사용 했는데  
i=0; i<30; i++;  
j=0; j<5; j++; 로 했음.  

근데 다시 생각해보고 정리를 해보니 해당 방식은
완성 후에도 몇번이나 낭비가 됨.  

그래서  
i=0; i<6; i++;  
j=0; j<5; j++; 방식으로 해결.

- 2. Element
처음으로 직접 Element라는 것을 사용해 봄.  
for문까지는 그냥 숫자로 출력 했지만, 이번에는 table, tr, td를 이용하여 출력

- 3. append vs appendChild
Child가 붙은거는 css와 동일하게 1가지만 넣을 때
Child 없이 append는 여러가지 넣을 때

1가지를 넣을 때 append를 사용하면 자원 낭비.

- 4. Code Review

```  
    let now = new Date();
    let month = now.getMonth() + 1;
    let year = now.getFullYear();
    const pText1 = document.createTextNode(year + "년 ");
    const pText2 = document.createTextNode(month + "월");
```   
now로 현재 날짜 데이터를 가져와서  
getMonth(), getFullYear()로 년도와 월 분리.  
createTextNode를 사용하여 Text 삽입.  

  > td.innerHTML = idx++;

  현재 8월 22일자 작성한 코드에서는 해당 코드 라인이 아직 이해가 가지 않음. -> 더 공부

