**First usage of REACT**

```js
var h1 = React.createElement('h1',null,'Hello from JS');

var parent = document.querySelector('.root');

var root = ReactDOM.createRoot(parent);

root.render(h1);
```

**Creating our React folder**

Run `npm create vite ` in your bash terminal.


### The flow used in react ###
*index.html -> main.jsx -> App.jsx*

## What is JSX. ##
It is combination of javascrpt + HTML.

**Creating our first react code**
```jsx
const App = ()=>{ 
  return "hellow"
}
export default App;
```
### ***Everything you write that should be inside the App*** ###
## How to return a variable ##

Use curly braces `{varibale}` inside the string
```jsx
const a = 10;

const App = ()=>{ 
  return (
    <h1>This was the first {a}</h1>
  )
}
export default App;
```
