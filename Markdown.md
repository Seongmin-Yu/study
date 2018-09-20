# Back-End related study

## node.js

### <u>**Express.js**</u>

- Express.js는 Node.js를 위한 빠르고 간편한 웹 프레임워크다.
- 다양한 프레임워크가 존재하고 있지만 Express engine를 가장
  많이 사용한다.
- MVC 패턴의 적용을 쉽게 해주는 3rd-party 모듈중 한가지다.

### <u>**Mocha**</u>

- **Mocah**는 러너를 포함하고 있는 테스트 프레임워크다.
- Mocha는 assertion을 지원하지 않기때문에 다른 라이브러리와 
  함께 사용해야 하며 Node에서 기본으로 제공하는 assert 
  라이브러리가 존재한다.
- 요즘은 주로 chio와 함께 사용한다고 한다.
- 설치방법에 대해서도 정리해보자.

<pre><code>
$ sudo npm install mocha
</code></pre>

- package.json에 스크립트를 추가해두면 편하다.
- -w옵션을 주면 파일이 변경되는 것을 감지하여 자동으로 테스트 러너가 실행된다.

<pre><code>
"scripts": {
    "test":"node_module/.bin/mocah $(find ./ -name '*.js') -recursive -w
},
</code></pre>

- 사용법은 나중에 정리!

### <u>**npm**</u>

- npm이란 Node Package Manager의 약자다.
- npm은 Javascript의 패키지 관리자다.
- Node의 기본 패키지 관리자다.
- 모아진 패키지들을 개발자는 편리하게 이용할 수 있다.

<pre><code>
$ npm install 모듈명
//-g 옵션 : 전역모드로 설치

$ npm uninstall 모듈명
//-g 옵션 : 전역모드로 삭제

$ npm undate 모듈명
//-g 옵션 : 전역모드로 업데이트

$ npm init //package.js파일 생성(기본적으로 프로젝트에 포함되지만 수동으로 생성가능)

$ npm ls //설치된 모듈 확인(지역)
$ npm ls -g --depth=0 //설치된 모듈 확인(전역)
</code></pre>

### <u>**nginx**</u>

- 비동기 이벤트 기반 구조의 웹서버 소프트웨어다.
- **Apache**는 하나의 이벤트에 하나의 쓰레드를 할당하는 방식을 사용하는 반면에
  **nginx**는 **Event=Driven**구조를 사용한다.
- **Event-Driven**구조는 여러개의 커넥션을 Event Handler를 통해 비동기 방식으로
  진행하여 먼저 처리되는 이벤트부터 로직을 실행시킨다.
- 더 작은 쓰레드로 클라이언트의 요청이 처리 가능하며, **Apache**보다 적은 리소스로
  더 빠른 처리가 가능하다.

![Alt text](https://mblogthumb-phinf.pstatic.net/MjAxNzAzMjZfMTM3/MDAxNDkwNDk1NjMxNzgy.OHZ33nerX_6Hc92Mg_xjr51acwwi1P_mq3SIl7Cuhisg.niRsQQVM5CwGpXKcdOxl3bkNsmfBkqGV1ajcBpV6CvQg.GIF.jhc9639/mighttpd_e02.gif.gif?type=w800)
**Event-Driven 구조**