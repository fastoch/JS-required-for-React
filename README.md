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
Props in React (short for **properties**) are a fundamental concept used for passing data from one component to another, 
specifically from a parent component to its child components.  

## The spread operator

If we want to create an object similar to the person object right above, except for the name value, we can do that:
```js
const person2 = {...person, name: "Filip"}
```

The spread operator is also very useful when working with arrays:
```js
const names = ["Pedro", "Jack", "Rose"]
const names2 = [...names, "Jessica"]  // this adds a name to the previous array
```

This operator is really important in React, because this is how we're going to manipulate arrays that are inside of **states**.  

# 3 important Functions for Arrays

- .map()
- .filter()
- .reduce()

## .map()

For each element in the array, apply a specific callback function.  

For example, add a string to each element and log the result to the console:
```js
let names = ["Pedro", "Jessica", "John"]
names.map((name) => {
  console.log(name + " is awesome!")
})
```

We can use `.map()` to render a React component:
```jsx
names.map((name) => {
  return <h1>{name}</h1>
})
```

## .filter()

Remove "Pedro" from the list: 
```jsx
let names = ["Pedro", "Jessica", "John"]
names.filter((name) => {
  return name !== "Pedro"
})
```

## .reduce()

- .reduce() takes two arguments: a callback function and, optionally, an initial value.
- The callback is called once for each element in the array, and it receives:
  - The accumulator (the running total or result from the previous iteration)
  - The current value (the current element in the array)
  - The current index (optional)
  - The array itself (optional)

If you provide an initial value, the accumulator starts with that.  
Otherwise, it's set to the first element in the array, and iteration begins at the second element.  

If no initial value is provided and the array is empty, .reduce() will throw an error.  

Example: 
```js
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue);
// sum is 10
```


@24/28
