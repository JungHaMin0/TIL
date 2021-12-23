## Spring Message Convert, BufferedReader & BufferedWriteer

### Message Converter (스프링 라이브러리로 존재)
"메시지 변환" 중간데이터, JSON
한국 [안녕] ---> 미국 (받지를 못함, 번역이 필요)
미국 [Hello] ---> 한국 (받지를 못함, 번역이 필요)
+ 한국어를 Direct로 영어로 번역이 어려움
✔️여기서 중간 데이터라는 것을 만듦. 즉 한국과 미국의 중간 언어를 만듦. => XML, JSON(요즘추세)

ex) Java Object를 C에게 보낼 때, C Object를 Java로 보낼 때
Java --> Json --> C 이런 식으로 하면 편함

![image](https://user-images.githubusercontent.com/80952596/147228523-da710d80-2a97-4650-8f32-940ef972d915.png)


### BufferedReader & BufferedWriteer
"BufferedReader" 가변 길이의 문자를 받을 수 있다 [request.getReader()]
즉 Java의 InputStreamReader에서 메모리 낭비를 하던 것을 보안한 것

"BufferedWriteer" 내려쓰기 때 printWriter를 자주 씀 --> println(), print()
즉 둘다 통신 시 문자열의 가변길이로 전송

@ResponseBody --> BufferedWriteer 실행됨
@RequestBody --> BufferedReader 실행됨

+ 스프링은 버전 업그레이드 되고, Boot도 나오고 계속 발전중이다. 이 언어를 꼭 계속 써야한다.
