---
title: "Reactjs UseEffect"
date: 2022-12-06T20:41:35+07:00
draft: false
---

useEffect is a hook that is used to perform side effects in function components. It is a combination of componentDidMount, componentDidUpdate, and componentWillUnmount. It is used to fetch data from the server, subscribe to events, and perform other side effects.

in my case i will use useEffect to fetch data from the server

first, you need to know lifecycle in reactjs

secondly, you need to know how to use useEffect

thirdly, you need to know how to fetch data from the server


here my code

```js   
import React, { useState, useEffect } from 'react'
import axios from 'axios'


const App = () => {
  const [data, setData] = useState([])

  useEffect(() => {
    axios.get('https://jsonplaceholder.typicode.com/users')
      .then(res => {
        setData(res.data)
      })
  }, [])

  return (
    <div>
      <h1>Reactjs UseEffect</h1>
      <ul>
        {data.map(item => (
          <li key={item.id}>{item.name}</li>
        ))}
      </ul>
    </div>
  )
}

export default App
```