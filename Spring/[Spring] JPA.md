## Spring JPA, ORM, 영속성

### JPA란? 
JPA는 persistence이다. => Java Persistence API
persistence(영속성): 데이터를 실행한 프로그램이 종료되어도 사라지지 않는 것
즉 Persistence는 영구의 기록이 될 수 있도록 해주는 것

![image](https://user-images.githubusercontent.com/80952596/147633206-113cd177-ff75-4708-b931-078fff4a4b19.png)


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


### JPA의 영속성
* 컨텍스트-> 그 대상의 모든 정보
영속성 컨텍스트(Context): 데이터를 영구적으로 저장
[자바 - 영속성 컨텍스트 - DB] (영속성 컨텍스트는 자바 Object)
자바에서 변경된 데이터는 영속성 컨텍스트에도 변경이 된다 하지만 DB의 데이터 타입은 다르기에
변경이 되지 않는다. 여기서 JPA의 특징이 나오는데 자바에서 변경된 데이터가 영속성 컨텍스트로 가서
자동으로 JPA로 Update, Delete가 된다.

걍 편리한 영속성 컨텍스트다. 한줄 정리.

### JPA는 DB와 OOP 불일치성을 해결하기 위한 방법론을 제공한다.
DB의 Team: int id, int name | User: int id, String name, int team_id가 있다고하면 
자바에서 저 기준으로 작성하면 DB에서 컨트롤을 가지게되고, DB에서 관계를 설정해줘야한다 하지만 
우리가 원하는 것은 JAVA에서 컨트롤을 가지는 것이다. 그에 따른 OOP, ORM 방법이 
int team_id를 => Team team_id로 바꿔서 오브젝트화 시켜준다 그러면 관계가 성립이 되고 JAVA에서 컨트롤 권한을 가진다.

* OOP: 객체지향 프로그래밍

JPA는 Spring에서 필요한 방법론이다.
내가 이제 해야할 것은 이런 것을 이용하고 애자일 방법론과 아키텍처 그리고 시큐리티를 사용하여
보다 더 완벽한 프로젝트를 만드는 것에 집중하자

### JPA OOP
JAVA에서 객체지향은 필드가 담긴 DB를 생성하면 VO로 만든다.
여기서 다른 VO를 위에 배운 오브젝트 형식대로 만들고 extends로 필드가 담긴 DB의 VO에 상속을 해주면
그 오브젝트들이 DB 아래 필드형태로 들어가게 된다. 

!! JPA는 OOP 관점에서 모델링을 할 수 있게 해준다. (상속, 콤포지션, 연관관계)

### 방언 처리 용이 -> Migration용이. 유지보수 용이.
SPRING -> JPA -> DB 형태로 돌아가서 JPA가 큰 역활을 해주는 것인데
여기서 방언 처리용이라는 것은 우리가 DB를 사용할 때  Oracle, Maria, MsSql, Mysql 등등 사용하는데
이것을 변경해줄려면 긴 코드를 수정해야하는데 Spring의 JPA는 그런 필요 없이 몇 줄이면 된다.

### JPA는 쉽고 어렵다.
적응을 하면 쉬움 근데 또 쉽다가 방대한 데이터 처리를 하면 다시 어려워짐


