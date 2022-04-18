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

npm install -y
package.json이 생성됨.
해당 파일 안에서  main: "index.js"는 지워도 됨

npm install parcel-bundler -D

major버전 : 기존 버전과 호환되지 않는 버전
minor버전 : 기존 버전과 호환되고 새로운 기능 추가된 버전
patch버전 : 기존 버전과 호환되고, 버그 및 오타 등이 수정된 버전

Major.Minor.Patch
12   .14   .1
이런 식으로 현재 프로그램이 어떤 식인지 확인이 가능
이런걸 배우는 이유가 버전관리 즉 협업에서 버전을 맞춰야하기에 이런 것을 알아야한다.

^12.14.1
'^' 캐롯 : Major 버전 안에서 가장 최신 버전으로 업데이트 가능
즉 Minor, Patch들만 업데이트가 된다

npm install lodash@4.17.20 : lodash를 4.17.20버전으로 다운

npm update lodash : lodash를 업데이트

*하지만 앞에 캐롯(^) 기호가 없으면 해당 명령어를 입력해도 최신 버전으로 업데이트x 

즉 원하지 않는 최신 버전 업데이트가 싫을 때 캐롯 기호를 지우면 된다.

~유의적버전










