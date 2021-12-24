## Spring JPA, ORM

### JPA란? 
JPA는 persistence이다. => Java Persistence API
persistence(영속성): 데이터를 실행한 프로그램이 종료되어도 사라지지 않는 것
즉 Persistence는 영구의 기록이 될 수 있도록 해주는 것

*API란?
애플리케이션(A)
프로그래밍 (P)
인터페이스 (I)
JPA란 즉 자바 프로그래밍을 할 때 영구적으로 데이터 저장을 하기위해 필요한 인터페이스 => JPA

(아직까진 이해가 안간다. 코드로 이해를 하자)


### JPA는 ORM이다.
Object Relational Mapping
오프젝트를 데이터베이스에 연결하는 방법론
모델링 -> 추상적인 개념을 현실로 꺼내는 것

## 핵심
자바와 파이썬이 통신할 때 서로의 말을 못 알아먹어서 JSON을 쓴다.
자바와 DB도 DB의 오브젝트를 자바가 못 알아먹어서 자바가 OBJECT를 직접 VO처럼 생성한다
그리고 하나하나 Connection을 해줘야하고, 쿼리문도 해야하는데 여기서!! JPA는 함수 하나로
모든 것을 해준다. 끗. 즉 이런 반복적인 CRUD를 함수 하나로 줄여준다. 즉 이런 것들을 JPA의 ORM이 해결해줌.
