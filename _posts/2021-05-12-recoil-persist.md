 ---
title: " recoil persist"
date: 2021-08-11 16:41:28 -0400
categories: study
---
 recoil persist
      ```
      import React from 'react'
import ReactDOM from 'react-dom'
import App from './App'
import { atom, RecoilRoot, useRecoilState } from 'recoil'
import { recoilPersist } from 'recoil-persist'

const { persistAtom } = recoilPersist()

const counterState = atom({
  key: 'count',
  default: 0,
  effects_UNSTABLE: [persistAtom],
})

function App() {
  const [count, setCount] = useRecoilState(counterState)
  return (
    <div>
      <h3>Counter: {count}</h3>
      <button onClick={() => setCount(count + 1)}>Increase</button>
      <button onClick={() => setCount(count - 1)}>Decrease</button>
    </div>
  )
}

ReactDOM.render(
  <React.StrictMode>
    <RecoilRoot>
      <App />
    </RecoilRoot>
  </React.StrictMode>,
  document.getElementById('root'),
)
      ```
