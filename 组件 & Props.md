import logo from './logo.svg'
import './index.css'
import './css.css'
import { React, Component, useState } from 'react'
import ReactDOM from 'react-dom'

/**
 *
 * React 有十分强大的组合模式。我们推荐使用组合而非继承来实现组件间的代码重用。
 * 我们将考虑初学 React 的开发人员使用继承时经常会遇到的一些问题，
 * 并展示如何通过组合思想来解决这些问题。
 * */

// 包含关系

function FancyBorder(props) {
  return (
    <div className={'FancyBorder FancyBorder-' + props.color}>
      {props.children}
    </div>
  )
}

// function WelcomeDialog() {

//     return (

//         <FancyBorder color = "blue" >
//                 <h1 className = "Dialog-title" > Welcome</h1>
//                 <p className="Dialog-messge"> Thank you for visiting our spacecraft</p>
//        </FancyBorder>
//     )
// }

// 包含关系

function Contacts() {
  return <div className="Contacts"></div>
}

function Chat() {
  return <div className="Chat"></div>
}

function SplitPane(props) {
  return (
    <div className="SplitPane">
      <div className="SplitPane-left">{props.left}</div>
      <div className="SplitPane-right">{props.right}</div>
    </div>
  )
}

// 特例关系

function Dialog(props) {
  return (
    <FancyBorder color="blue">
      <h1 className="Dialog-title">{props.title}</h1>
      <p className="Dialog-messge">{props.messge}</p>
    </FancyBorder>
  )
}

function WelcomeDialog() {
  return (
    <Dialog
      title="Welcome4564564564"
      messge="Thank you for visiting our spacecraft play for swift"
    />
  )
}

// 组合也同样适用于以 class 形式定义的组件。

function Dialog(props) {
  return (
    <FancyBorder>
      <h1 className="Dialog-title">{props.title}</h1>
      <p className="Dialog-messge">{}</p>
    </FancyBorder>
  )
}

class SignUpDialog extends Component {}

function App() {
  return (
    <>
      <WelcomeDialog /> <SplitPane left={<Contacts />} right={<Chat />} />
    </>
  )
}
export default App

