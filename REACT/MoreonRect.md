## Experimenting ##
**Let's create a project in which button increment a variable value when clicked.**

```jsx
const App = ()=>{
  let count = "Zero"
  const incrementCount = ()=>{
    console.log(count)
  }
  return (
    <div>
      <button onClick={incrementCount}>Click to add</button>
    </div>
    )
}
export default App;
```
## Use of useState ##
Code without useState: The value will not change in the frontend..
with this code:
```jsx
import { useState } from "react"

const App = ()=>{
  let count = 0;
  const incrementCount = ()=>{
    count+=1
    console.log(count)
  }
  return (
    <div>
      <h1>
        The value of the count is= {count}
      </h1>
      <button onClick={incrementCount}>Click to add</button>
    </div>
    )
}
export default App;
```
The problem with the above code is that in the console value of count is incremented but int the frontend it doesn't get updated..

### But with the use of useState we can do that ###
React is more optmized that's why we have to tell to react to change the value of count in the frontend.
```jsx
import { useState } from "react"

const App = ()=>{
  const [count,setCount] = useState(10)
  const incrementCount = ()=>{
    setCount(count+1);
  }
  return (
    <div>
      <h1>
        The value of the count is= {count}
      </h1>
      <button onClick={incrementCount}>Click to add</button>
    </div>
    )
}
export default App;
```

## Some more codes: ##
Incrementing and Decrementing the value using useState

```jsx
import { useState } from "react"

const App = ()=>{
  const [count,setCount] = useState(10)
  return (
    <div>
      <h1>
        The value of the count is= {count}
      </h1>
      <button onClick={() =>{
        setCount(count+1)
      }}>Increment</button>
      <button onClick={()=>{
        setCount(count-1)
      }}>Decrement</button>
    </div>
    )
}
export default App;
```