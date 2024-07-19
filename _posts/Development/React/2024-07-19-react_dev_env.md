---
title: React 개발환경 설정
date: 2024-07-19 +0800
categories: [Development, React]
tags: [dev, react, env] # TAG는 소문자
---
### React란? 
---
웹 프로그래밍의 장점은 인터넷만 연결돼 있다면 자신이 개발한 웹 사이트를 다른 사람과 공유할 수 있고 웹 페이지를 만드는 과정에서 시각적인 결과물이 계속 생성되기 때문에 비교적 재미있게 개발할 수 있다는 것이다. 

<br/>

리액트는 웹 페이지에서 눈에 보이는 영역인 프런트엔드에 특화된 언어이다. 리액트의 장점은 코드 이식성과 재활용성이 높고 화면 출력 속도가 빠르다는 것이다. 화면을 구성하는 코드를 컴포넌트 단위로 나누고 필요한 부분에 이식해 사용할 수 있다. 그리고 자바스크립트(Javascript) 기반의 언어이기 때문에 리액트를 잘하면 자바스크립트 실력도 자연스럽게 향상된다.

<br/><br/><br/><br/>

### 개발 환경 준비
---
- 자바스크립트 패키지 관리 도구
	- npm
		- node package manager
		- node.js와 react.js에서 사용하는 대부분의 패키지를 설치할 수 있다.
		- npm은 node.js와 함께 설치된다.
	- yarn
		- 페이스북에서 만든 패키지 도구
		- npm에 비해 캐싱, 보안, 신뢰성 등이 개선됐다.

<br/>

#### 1. node.js 다운로드
- https://nodejs.org/en/download/release에 접속해 14.4.0 버전 다운로드

<br/>

#### 2. node.js 설치
[Automatically install the neccesary tools. Note that this will also install Boxstarter and Chocolatey. The script will pop-up in a new window after the installation completes]에 체크 표시를 하지 않고 [Next]를 클릭한다. [Finish]를 눌러 설치를 완료한다.

<br/>

#### 3. node.js 및 npm 설치 확인
`win` + `R`을 누른 후 'cmd'를 입력해 명령 프롬프트를 실행한다. node -v, npm -v 명령어로 설치된 node.js와 npm의 버전을 확인한다.

<br/>

#### 4. react 프로젝트의 워크스페이스로 사용할 폴더 생성
cmd 창에서 cd 명령어를 이용해 생성한 폴더 경로로 이동한다. 

<br/>

#### 5. yarn 설치
npm install 명령어로 yarn을 설치한다. yarn -v 명령어로 설치된 yarn 버전을 확인한다.

<br/>

#### 6. create-react-app 설치
- ~~npm install -g create-react-app 명령어로 create-react-app를 설치한다. create-react-app client 명령어로 'client'라는 프로젝트를 생성한다. 프로젝트를 생성한 후 client 경로를 보면 package.json, node_modules 등의 파일과 폴더가 생성된 것을 확인할 수 있다.~~
- **npx create-react-app my-app 으로 실행해야 한다.**

<br/>

#### 7. react 서버 실행
- client 경로에서 yarn start 명령어로 react 서버를 실행한다. 크롬 웹 브라우저에서 http://localhost:3000 url을 열면 웹 화면을 확인할 수 있다.
- src 폴더의 index.js 파일을 열어 <React.StrictMode>, </React.StrictMode> 태그를 삭제한다. Strict 모드는 애플리케이션 내의 잠재적 문제를 알아내기 위한 도구로, 생명 주기 함수를 여러 번 실행하는 원인이 되므로 사용하지 않는다. 

<br/>

```js
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  // <React.StrictMode>
    <App />
  // </React.StrictMode>
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```

<br/>

#### 8. 실행 방법 
react 프로젝트인 경우, react 경로에서 [npm install] 명령어를 실행한다. 같은 경로에서 [npm start] 명령어로 react 서버를 구동한다. react, node 프로젝트인 경우, react와 node 경로에서 각각 [npm install] 명령어를 실행한 후 [yarn dev] 명령어로 react, node 서버를 동시에 구동한다. react, node 폴더 경로에는 각각 package.json 파일이 있는데, 프로젝트에서 사용하는 npm 패키지 리스트가 작성돼 있다. [npm install] 또는 [yarn install]을 실행하면 package.json 파일에 있는 패키지 리스트가 설치된다.

<br/><br/>

✔ Create React App (2024 기준)

```
npx create-react-app my-app
cd my-app
npm start
```
