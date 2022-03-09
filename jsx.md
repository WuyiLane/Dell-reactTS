import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
// /**
//  *  实例1
//  * */
// const name = 'Josh Perez';
// const element = <h1>Hello, {name}</h1>;
/**
 *  实例2 在 JSX 中嵌入表达式
 * */

// function formatName(user) {
//     return user.firstName + '' + user.lastName;
// }

// const user = {
//     firstName: 'Harper',
//     lastName: 'Perez'
// }

// const element = (
//     <h1>
//     Hello，{formatName(user)}
//   </h1>
// )
/**
 * 实例3 JSX 也是一个表达式
 * */

// function formatName(user) {
//     return user.firstName + '' + user.lastName;
// }
const user = {
    firstName: 'Harper',
    lastName: 'Perez',
    avatarUrl: 'https://t7.baidu.com/it/u=4158772482,569675020&fm=193&f=GIF'
}

// function getGreeting(user) {
//     if (user) {
//         return <h1> Hello, { formatName(user)}</h1>
//     }
//     return <h1> Hello,Stranger.</h1>

// }
// const element = (
//     <h1>
//     Hello，{getGreeting(user)}
//   </h1>
// )

/**
 * jsx 特定属性
 * */

const element = <div tabIndex="0">Hello,react</div>
const img = <img src={user.avatarUrl}></img>
/**
 * 使用 JSX 指定子元素
 * */

const elementImg = <img src={user.avatarUrl}/>
/**
 *jsx 标签里能够包含很多子元素 
 * 
 * */

// const elementText = (
//     <div>
//     <h1>
//       Hello!
//     </h1>
//     <h2>Good to see you here</h2>
//   </div>
// )

// const title = response.potentiallyMaliciousInput
// // 直接这样是安全的
// const elementTitle = <h1>{title}</h1>

/**
 * 
 * jsx 表示对象：
 * Babel 会把 JSX 转译成一个名为 React.createElement() 函数调用
 * */


const elementgreet = (
    <h1 className="getGreetingr">
      Hello,react
    </h1>
)

/**
 *  简化过的结构
 * 
 * */

/**
 * “React 元素”。它们描述了你希望在屏幕上看到的内容。React 通过读取这些对象，然后使用它们来构建 DOM 以及保持随时更新。
 * */
// const element = {

//     type: 'h1',
//     props: {
//         className: 'getGreeting',
//         children: 'Hello,world!'
//     }
// }

ReactDOM.render(
    elementgreet,
    document.getElementById('root')
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals

