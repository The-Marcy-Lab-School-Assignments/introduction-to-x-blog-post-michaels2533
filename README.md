# Learning React as a JavaScript Developer in 2025! 

By Michael Stawowski

## Introduction

## Why should I use React? 
React is a popular Javascript library used by developers for building user interfaces. Originally, developed by Facebook and is used among 
companies like Instagram, AirBnb and Netflix to create dynamic and fast web applications. React make building interactive UIs 
easier and seamless with is component-based architecture and virtual DOM. 

If you're totally new to React, don't fret!. In this tutorial, I will walkthrough the core concepts/features of React,
how to setup a React project and compare and contrast between using React and plain VanillaJS to build 
interactive user websites. 


## Core syntax/features. 

* For programming languages: data types, variables, code blocks, functions, conditionals, arrays and objects, and iteration. Include code snippets with explanations.

* For frameworks (including React and Express): setup/installation/configurations, core concepts, key methods or approaches. Include code snippets with explanations.

## Configuring your React Development Environment. 
Before we can dive into learning about React, you'll need to setup your development environment to get started with React. Here's a brief rundown.


## Step 1: Install Node.js
Before we begin, make sure NodeJs is installed on your machine. NodeJs will come bundled with npm, the package manager that we will be using throughout this process.

Afterwards, check if it's properly installed by running the following commands in your terminal.

```bash
node --version
npm --version
```

## Step 2: Install Create React App
Create React App is a tool that setups up a new React Project with sensible defaults, so you don't need to manually configure anything.

Install Create React App with the npm package manager. 
```bash
npm install -g create-react-app
```
---
Disclaimer: It's strongly recommended you use modern build tools like Vite to build React applications. The React team no longer supports the create-react-app tool for newer projects.However, this article focuses on the bare minimum you need to get started with React 

## Step 3: Create a Fresh React Project
Finally, now you're ready to create your first React app, run the following commands.

```bash
npx create-react-app my-first-react-app
cd my-first-react-app
npm start
```
Congratulations, you have successfully configured your React application! This will start your React development server, and you can open your browser and visit http://localhost:3000 to see your app running.

## Understanding The Core Concepts of React 
Now, let's breakdown the core concepts/features of React.

## Components: The Building Blocks of React
The React Framework are built using components. A component is a reusable, self-contained piece of code that dictates how a UI element is rendered.
There are two types of components in React: functional components and class components. 

Here's a simple examples of both a functional and class components.

 A simple functional component
```js
function message() {
    return <h1>Hello World!</h1>>
}

export default message; 
```

A simple class component
```js
import React from "react"; 

class Counter extends React.Component {
    // Initialize the internal state.
    constructor(props) {
        super(props)
        this.state = {count : 0};
    }
    // A custom method to update the counter.
    function increment() {
        this.setState(prevState=>({count:prevState.count + 1}));
    }

    // This method is required in class components.
    render() {
        return (
            <button onClick={this.increment}>
            Clicked {this.state.count} time{this.state.count !== 1 && "s"}
            </button>
        )
    }
}
 export default Counter;
```

As you can see, a component can simply return an h1 element or be as complex as a counter system. This is why components in React are such 
a powerful and important concept. 

## JSX(Javascript XML)
React uses JSX, a syntax extension that allows you to write HTML-like code within Javascript. While it looks like HTML, it's actually
syntactic sugar for React.createElement() calls.

Here is simple example of JSX: 

```jsx
const elm = <h1> Hello World! </h1>
```

## State and Props Systems: Enables dynamic components 
React components utilize states and props to manage and store data. Here is a quick rundown of their definitions.

States: Data that can be changed within a component.

Props: Data passed to the child component from the parent.


## Using State 
States are used to manage data that can be changed over time. Here's an example using the useState hook.

```js
import React, { useState } from 'react'; 

function Counter() {
    const [count, setCount] = useState(0);
    
    return (
        <div>
            <p>You clicked {count} times</p>
            <button onClick={() => setCount(count + 1)}>Click me</button>
        </div>
    );
}
```
Here useState is used to create a state variable **count** and a function **setCount** that updates the count state. The component rerenders whenever the state changes.

## Using Props
Props are used to pass data to child components. Here is an example.

```js
function Greeting({name}) {
    return <h1>Hey there! ,{name}</h1>
}

// In the parent component.
<Greeting name="John"/>
```

Here I passed down the name prop to the **Greeting** component. After that, I destructured the name prop from the object and called it within the component.
## Compare and Contrast

* For programming languages: What are the key differences between the new language and JavaScript? What are the commonalities?
* For frameworks (including React and Express): What are the alternatives to this framework? Can you compare this framework to anything we've learned in the Core Curriculum? What are the tradeoffs when choosing this framework compared to the alternatives?


## Compare and Contrast: Why use ReactJs instead of VanillaJS? 


## Conclusion & Tips for learning this language/framework.

* Wrap things up
* Provide links to resources that you used to help you learn the language.

