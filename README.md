src = https://youtu.be/m55PTVUrlnA?si=DP2WCaVrUm-mKiiY  

# Arrow Functions

When working with React, we use a lot of arrow functions.  
- Classic function syntax:
```js
function DoSomething() {
  // the logic goes here 
}
```
- Arrow function:
```js
const DoSomething = () => {
  // the logic goes here 
}
```

In React, we define components, and components are just functions.  
```js
const MyComponent = (props) => {
  // some hooks
  // some helper functions
  // a return statement containing our JSX 
}
```

## Anonymous functions

They allow us to execute a piece of logic without having to declare a function:
```jsx
<button>
  onClick={() => { some logic }}
</button>
```

# Ternary Operators

They are very handy to minimize the amount of code we write in React.  

An if...else statement takes too many lines:
```js
if (age > 20) {
  let category = "adult"
} else {
  let category = "kid"
}
```

With a ternary operator:
```js
let category = age > 20 ? "adult" : "kid"
```

Another way to do that is by usinga syntax called "**short circuiting**":
```js
let category = (age > 20 && "adult") || "kid"
```

Example with a React component:
```jsx
const Component = () => {
  ...
  return age > 20 ? <div>Adult</div> : <div>Kid</div>
}
```

# Objects

Also known as dictionaries in Python, objects are very important in React.  

## Object destructuring

```js
const person = {
  name: "Peter",
  age: 32,
  isMarried: false
}

const name = person.name
const age = person.age
const isMarried = person.isMarried

// The 3 variables above can actually be declared in one line:
const { name, age, isMarried } = person
```

We use object destructuring a lot when working with **props**.  
Props in React (short for **properties**) are a fundamental concept used for passing data from one component to another, specifically from a parent component to its child components.  



@16/28
