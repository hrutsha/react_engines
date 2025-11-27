```
import React, { useState } from 'react'

const Form = () => {

    let [data,setData] = useState({
        name:" ",
        email:" ",
    })

    let nameHandler = (e)=>{
        setData({...data,name:e.target.value })
    }

    let emailHandler = (e)=>{
        setData({...data,email:e.target.value })
    }
    console.log(data)

    let clearHandler = ()=>{
        setData({
            name:" ",
            email:" "
        })
    }
  return (
    <div>
        <h3>registration form</h3>

        <input type="text" placeholder='enter your name' onChange={nameHandler} value={data.name} /> <br />
        <input type="text" placeholder='enter your email' onChange={emailHandler} value={data.email} />

        <button onClick={clearHandler}>clear</button>

        <p> {data.name} </p>
        <p> {data.email} </p>


    </div>
  )
}

export default Form
```

```
import React, { useState } from 'react'

const Form = () => {
    let [data,setData] = useState({
        name:"",
        email:""
    })
    
    let inputHandler = (e)=>{
        setData({...data,[e.target.name]:e.target.value })
    }

    let clearHandler = ()=>{
        setData({
            name:"",
            email:""
        })
    }

  return (
    <div>
        <h3>Registration Form</h3>
        <input type="text" name='name' placeholder='enter name' onChange={inputHandler} value={data.name} /> <br />
        <input type="text" name='email' placeholder='email' onChange={inputHandler} value={data.email} /> <br />

        <button onClick={clearHandler}>clear</button>

        <p> {data.name} </p>
        <p> {data.email} </p>
    </div>
  )
}

export default Form
```
