# Back-End related study

## node.js

### Express.js

- Express.js는 Node.js를 위한 빠르고 간편한 웹 프레임워크다.
- 다양한 프레임워크가 존재하고 있지만 Express engine를 가장
  많이 사용한다.
- MVC 패턴의 적용을 쉽게 해주는 3rd-party 모듈중 한가지다.

#### Mocha

- Mocah는 러너를 포함하고 있는 테스트 프레임워크다.
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