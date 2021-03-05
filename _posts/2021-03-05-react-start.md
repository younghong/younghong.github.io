---
date: 2020-12-21 07:26:40
layout: post
title: React 시작하기
subtitle: React 시작하기
description: React 시작하기
image: https://younghong.github.io/img/react_logo.png
optimized_image: https://younghong.github.io/img/react_logo.png
comments: true
category: React
tags:
  - React
  - Dev
author: yh.kim
---



## React 시작하기

#### 1.nodejs 설치

Node.js가 없다면 설치한다. 
설치 링크를 아래에 연결해 놓았다.
[node.js](https://nodejs.org/en/ "node js")

#### 2.react project 생성
npm install 단계 없이 'create-react-app my-app' 명령어를 실행해도 되지만
version이 맞지 않다는 오류가 발생하면 'npm install -g create-react-app' 명령어를 실행해야 한다.
```shell
$ npm install -g create-react-app
$ create-react-app my-app
```

#### 3.JSX 문법
javascript와 xml이 결합된 표현식
기본적인 사용 방법은 html tag를 return해 주면된다.

```js
function App() {
  return (
    <div>
      <h1>1</h1>
      <h2>2</h2>
    </div>
  );
}

export default App;
```


#### 4.hello world
코딩의 시작 hello world를 찍어보자.
```js
function App() {
  return (
    <h1>Hello World</h1>
  );
}

export default App;
```


#### 5.Component 생성
class로 컴포넌트를 생성하고,
생성된 컴포넌트를 호출한다.
```js
import React from 'react';
import ReactDOM from 'react-dom';
import './App.css';


class Hello extends React.Component {
  render() {
    return (
      <div>
        Hello World
      </div>
    );
  }
}

function App() {
  return (
    <Hello />
  );
}

export default App;
```

#### 6.속성 넘기기
```js
import React from 'react';
import './App.css';

class Hello extends React.Component {

  constructor(props){
    super(props);
    this.state={age:10,name:'hi'};
  }


  render() {
    return (
      <div>
        Hello {this.props.name}  - 
        age: {this.props.age}
      </div>
    );
  }
}

function App() {
  return (
    <Hello name="UBISTORM" age='1110' />
  );
}

export default App;
```

![placeholder](https://younghong.github.io/img/react_logo.png "install file")
























