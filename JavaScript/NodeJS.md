### Node JS

개발자라면 Node.js만 다운 받는게 아니라 버전을 자유롭게 바꿀 수 있는 nvm을 설치!
https://github.com/coreybutler/nvm-windows/releases
에서 nvm-setup다운로드 - 터미널에서 - nvm --version을 통해 버전 확인

nvm 사용법
nvm ls: 설치 확인 명령어
nvm install 12.14.1: 12.14.1버전을 유의적 설치(버전 최대치는 nvm current로 확인)
*nvm으로 프로젝트에 맞는 node.js 버전을 설정.

NPM(Node Package Manager)
NPM 약 100만 개의 패키지들이 있다. 이것은 오픈패키지나 회사에서 만들어진 패키지를 npm install로 설치 후 사용이 가능하다.

보통 npm 패키지는 우린 모듈이라고 부른다.
예를들면 슬라이드 플러그인이다. 누군가 만들어 놓은 것을 우리가 가져다 씀.

->npm install -y
package.json이 생성됨.
해당 파일 안에서  main: "index.js"는 지워도 됨

->npm install parcel-bundler -D
모듈 안에 parcel-bundler라는 폴더가 생김.

->npm install lodash
모듈 안에 lodash라는 것이 생김

npm install한 것을 package.json에서 볼 수 있다.

package-lock.json는 자동으로 관리하는 개념.
package.json는 직접적으로 관리하는 개념

예를 들어 패키지A 안에 여러가지 패키지가 있는데 이것을 우리가 직접 관리하기 어렵다 그래서 자동으로 관리해주는게 package-lock

node_modules는 지워져도 됨
npm i로 다시하면 됨 그러나 package~~는 지워지면 안됨.

```
->npm install parcel-bundler -D
->npm install lodash

```

-D의 차이는 package에서 dependencies 앞에 'dev'가 붙는다 => devDependencies 이것의 차이는 


개발용 의존성 vs 일반 의존성

[개발용 의존성]
개발할 때만 필요하고 웹 브라우저에선 필요하지 않을 경우 (직접적 동작x)

[일반 의존성]
실제 웹 브라우저에서도 동작할 수 있는 개념

-D는 --save-dev의 약어


요즘은 Live Server는 잘 안쓰고 parcel를 씀
패키지.json - script 부분에 "dev": "parcel index.html" 명렁 추가
이럴 경우 프로젝트 내부에서만 명렁어가 동작.
-> npm run dev

나오는 주소를 팔로우 링크.

<script>
import _ from 'lodash'
</script>

빌드화
script 부분에
"build": "parcel build index.html"
-> npm run build 진행 시
dist라는 폴더 생성 -> dist에 index.html에 난독화가 진행되어 있음.
즉 패키지를 번들을 해서 용량을 축소 시킨 것 빌드 시 정말 유용.

지금 이 시간에 배우는 것은 패키지를 관리하고 유용하게 쓰며, 그 많은 패키지를 빌드시킬 때도 유용하게 용량 축소를 통하여 더욱 효과적으로 할 수 있는 
parcel-bundler, lodash를 배움

그리고 라이브서버말고 이젠 lodash로 서버를 열어서 개발하자.


