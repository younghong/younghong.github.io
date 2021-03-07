---
date: 2021-03-05 07:26:40
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

<ins>*VSCode의 터미널을 Shell로 설정해뒀다면 ShellScript 오류가 발생할 수 있다
윈도우 사용자라면 cmd로 바꿔놓는게 편할꺼다.*</ins>
```shell
$ npm install -g create-react-app
$ create-react-app my-app
```

#### 3.JSX 문법
javascript와 xml이 결합된 표현식이다.
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

#### 4.ES6 문법
리액트는 js 라이브러리이며, es6문법이 종종 등장한다.
```js

//전통적인 문법
function bob (a){
  return a + 100;
}

// Arrow Function
let bob = a => a + 100;



//전통적인 문법
function sum(a,b){
  return a+b;
}

// Arrow Function
sum = (a,b) => {
        return a+b;
}

```


#### 5.hello world
코딩의 시작 hello world를 찍어보자.
```js
function App() {
  return (
    <h1>Hello World</h1>
  );
}

export default App;
```


#### 6.Component 생성
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

#### 7.속성 넘기기
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


#### 8.리액트 Hooks
리액트를 functional programming style로 만들어주는 기능.

아래 코드는 단순 카운트를 늘려주는 코드지만
해야할 것들이 많다.

##### 8-1 일반적인 코드
```js
import React from 'react';

class App2 extends React.Component {

    state = {
        count:0
    }

    modify = (n) => {
        this.setState({
            count:n
        });
    };

    render() {
        const { count } = this.state;
      return (
        <div className="game">
            <div>{count}</div>
            <button onClick={ () => this.modify(count+1)}>Incremnt</button>
        </div>
      );
    }
  }

export default App2;
  
```
##### 8-2 Hooks을 사용한 코드
훅을 사용하니 위 코드보다 훨씬 더 간결해졌다.
```js
import React, {useState} from 'react';

const App = () => {
    const [count, setCount] = useState(0);

    return (
        <div className="game">
            <div>Hook</div>
            <div>{count}</div>
            <button onClick={ () => setCount(count+1)}>Incremnt</button>
        </div>
    )
}

export default App;
```

#### 9 React Redux
Redux는 angular,Vue,바닐라 등에서도 사용하는 javascript library.

Redux 설명 이미지-1
![placeholder](https://younghong.github.io/img/blog_2021-03-07(2).png "Object Tree")

Redux 설명 이미지-2
![placeholder](https://younghong.github.io/img/blog_2021-03-07.png "Object Tree")


dispatch (action) => hadle (reducer) => update store

npm init -y
npm install redux
npm install redux react-redux


>effect , Higher Order Hook등 배워야할게 많다

![placeholder](https://younghong.github.io/img/react_logo.png "install file")
























