# 🚀React Projects with Vite.js <img height=50px src="https://skillicons.dev/icons?i=react"> <img height=50px src="https://skillicons.dev/icons?i=vite">

<img height="170px" align="right" src="https://github.com/shanibider/Vite.js-With-React/assets/72359805/e3c6ac19-7d0b-4b57-9473-613b5203e5b3">

This repository aims to provide a comprehensive guide to understanding the core concepts of `React.js`, a popular JavaScript library for building user interfaces. Contains practice projects aimed at improving skills in 
### React.js, utilizing the Vite.js build tool <img height=20px src="https://skillicons.dev/icons?i=react"> <img height=20px src="https://skillicons.dev/icons?i=vite"> <img height=20px src="https://skillicons.dev/icons?i=js">,
for a seamless development experience.


## Overview 💻
  - [x] 🎯 Learn front-end development with React.
  - [x] 🎯 Understand when and how to use **React Components**.
  - [x] 🎯 Learn to **pass Prop**s and work with them.
  - [x] 🎯 Learn to write **JSX** and understand JSX syntax.
  - [x] 🎯 Learn about the **React DOM**.
  - [x] 🎯 Learn **State Management** in React.
  - [x] 🎯 Learn about **React Hooks**.
  - [x] 🎯 Learn about **conditional rendering** in React.
  - [x] 🎯 Understand the difference between **class and functional components**.






# React Fundamentals <img height=40px src="https://skillicons.dev/icons?i=react">
React is a JavaScript library developed by Facebook for building user interfaces. It allows developers to create reusable UI components and efficiently manage the state of their applications.

## Covering -

  - [x] 🚀Introduction to React
  - [x] 🚀 Getting Started
  - [x] 🚀 Components
  - [x] 🚀 Props and State
  - [x] 🚀 Lifecycle Methods
  - [x] 🚀 Event Handling
  - [x] 🚀 Conditional Rendering
  - [x] 🚀 Lists and Keys
  - [x] 🚀 Forms
  - [x] 🚀 Hooks
  - [x] 🚀 Context API
  - [x] 🚀 Refs
  - [x] 🚀 Virtual DOM
  - [x] 🚀 React Router




## Introduction to React -
```jsx
import React from 'react';

const App = () => {
  return (
    <div>
      <h1>Hello, React!</h1>
      <p>Welcome to the world of React.</p>
    </div>
  );
}

export default App;
```


## 🏆 Getting Started
To get started with React, you'll need to have Node.js and npm installed on your machine. You can create a new React project using Create React App, a toolchain for setting up React projects quickly.

```bash
npx create-react-app my-app
cd my-app
npm start
```
<br>

## 🏆 Components
Components are the building blocks of React applications. They are reusable UI elements that encapsulate logic and markup. React components can be either functional components or class components.
- [ ] Class components have a render() method that returns React elements.
- [ ] Function components are JavaScript functions that return React elements. They are simpler and easier to read compared to class components.

**Example:**

```jsx
import React from 'react';

const Button = () => {
  return <button>Click me</button>;
}

export default Button;
```
### ✅ Function Based Components:
![Capture](https://github.com/shanibider/React-Vite.js/assets/72359805/bd0b5a77-851d-46c6-aa6e-efe7f69e3e2c)

<br>


## 🏆 Props and State
`Props` (short for properties) and `state` are core concepts in React for managing data and passing data between components.
- [ ] `Props` are inputs to components. They are immutable and are passed from parent components to child components. Props allow components to be customizable and reusable.
- [ ]`state` represents the internal data of a component. It is mutable and can be changed using setState(). State is managed within a component and is used to maintain and update data.

**Example:**

```jsx
import React, { useState } from 'react';

const Counter = () => {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}

export default Counter;
```

### ✅ State vs Props:  
![2](https://github.com/shanibider/React-Vite.js/assets/72359805/f36f7fc2-52b1-4048-b75b-54d85354d015)

<br>

## 🏆 Component Lifecycle: 
React components have a lifecycle that includes various stages such as mounting, updating, and unmounting. Developers can hook into these lifecycle events to perform actions like initializing `state`, **fetching data**, or cleaning up resources.
<br>

## 🏆 Lifecycle Methods
Lifecycle methods allow developers to hook into specific points in the lifecycle of a component, such as when it is mounted, updated, or unmounted. These methods enable developers to perform actions like fetching data, updating the DOM, or cleaning up resources.

**Example:**

```jsx
// LifecycleExample.js
import React, { Component } from 'react';

class LifecycleExample extends Component {
  constructor(props) {
    super(props);
    console.log('Component is initialized');
  }

  componentDidMount() {
    console.log('Component is mounted');
  }

  componentDidUpdate() {
    console.log('Component is updated');
  }

  componentWillUnmount() {
    console.log('Component is unmounted');
  }

  render() {
    return <div>Lifecycle Example</div>;
  }
}

export default LifecycleExample;
```

### ✅ Lifecycle Hooks + Fetching Data from APIs:
- [ ] Lifecycle hooks are special methods that allow you to perform actions at specific points in a component's lifecycle. Some common lifecycle hooks in class components include componentDidMount, componentDidUpdate, and componentWillUnmount. In function components, you can achieve similar behavior using `useEffect` hook.
- [ ] In React, you can fetch data from APIs using methods like fetch() or libraries like Axios. Typically, you perform API calls in lifecycle hooks or `useEffect` hook to fetch data when the component mounts or updates.
![3](https://github.com/shanibider/React-Vite.js/assets/72359805/3fa503e2-2429-4d63-8dee-7a754e976259)

<br>



## 🏆 Event Handling
In React, event handling is similar to handling events in HTML, but with a few syntactic differences. Event handlers are specified as camelCase properties in JSX and passed as props to components.

**Example:**

```jsx
// ClickCounter.js
import React, { useState } from 'react';

const ClickCounter = () => {
  const [count, setCount] = useState(0);

  const handleClick = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={handleClick}>Click me</button>
    </div>
  );
}

export default ClickCounter;
```
<br>



## 🏆 Hooks
Hooks are a new addition in React 16.8 that allow developers to use state and other React features without writing class components. Hooks provide a more functional approach to working with React components.

**Example:**

```jsx
// CounterWithHooks.js
import React, { useState } from 'react';

const CounterWithHooks = () => {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}

export default CounterWithHooks;
```
<br>


## 🏆 Context API
The Context API is a feature introduced in React 16.3 for managing `global state` in React applications. It allows data to be passed through the component tree without having to pass props down manually at every level.

**Example:**

```jsx
// ThemeContext.js
import React, { createContext, useState } from 'react';

export const ThemeContext = createContext();

export const ThemeProvider = ({ children }) => {
  const [theme, setTheme] = useState('light');

  const toggleTheme = () => {
    setTheme(theme === 'light' ? 'dark' : 'light');
  };

  return (
    <ThemeContext.Provider value={{ theme, toggleTheme }}>
      {children}
    </ThemeContext.Provider>
  );
};
```

### ✅ Context API and React Hooks:
![6](https://github.com/shanibider/React-Vite.js/assets/72359805/abdef6e0-8960-4a24-aefb-aa68e8f97712)

<br>




## 🏆 Conditional Rendering
Conditional rendering in React allows developers to show or hide elements based on certain conditions. This can be achieved using JavaScript expressions or ternary operators within JSX.

**Example:**

```jsx
// ConditionalRendering.js
import React, { useState } from 'react';

const ConditionalRendering = () => {
  const [isLoggedIn, setIsLoggedIn] = useState(false);

  return (
    <div>
      {isLoggedIn ? (
        <p>Welcome, user!</p>
      ) : (
        <button onClick={() => setIsLoggedIn(true)}>Log in</button>
      )}
    </div>
  );
}

export default ConditionalRendering;
```
<br>


## 🏆 Lists and Keys
Rendering lists of items in React is a common task. Keys are special attributes that help React identify which items have changed, are added, or are removed from a list.

**Example:**

```jsx
// ListExample.js
import React from 'react';

const ListExample = () => {
  const items = ['Apple', 'Banana', 'Orange'];

  return (
    <ul>
      {items.map((item, index) => (
        <li key={index}>{item}</li>
      ))}
    </ul>
  );
}

export default ListExample;
```
<br>



## 🏆 Forms
React provides a way to manage form inputs and their state using controlled components. Controlled components tie the form elements' values to the component's state, allowing React to control the form's behavior.

**Example:**

```jsx
// FormExample.js
import React, { useState } from 'react';

const FormExample = () => {
  const [formData, setFormData] = useState({ email: '', password: '' });

  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData({ ...formData, [name]: value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    console.log('Form submitted:', formData);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="email"
        name="email"
        value={formData.email}
        onChange={handleChange}
        placeholder="Email"
      />
      <input
        type="password"
        name="password"
        value={formData.password}
        onChange={handleChange}
        placeholder="Password"
      />
      <button type="submit">Submit</button>
    </form>
  );
}

export default FormExample;
```
<br>


## 🏆 Refs
Refs provide a way to access DOM nodes or React elements created in the render method. They are useful for accessing form elements, triggering imperative animations, or integrating third-party DOM libraries.

**Example:**

```jsx
// TextInputWithFocusButton.js
import React, { useRef } from 'react';

const TextInputWithFocusButton = () => {
  const inputRef = useRef(null);

  const focusInput = () => {
    inputRef.current.focus();
  };

  return (
    <div>
      <input ref={inputRef} type="text" />
      <button onClick={focusInput}>Focus Input</button>
    </div>
  );
}

export default TextInputWithFocusButton;
```
<br>


## 🏆 React Router

React Router is a popular library for adding routing to React applications. It allows developers to create single-page applications with multiple views, each mapped to a unique URL.

**Example:**

```jsx
// AppRouter.js
import React from 'react';
import { BrowserRouter as Router, Route, Switch } from 'react-router-dom';
import Home from './Home';
import About from './About';
import Contact from './Contact';

const AppRouter = () => {
  return (
    <Router>
      <Switch>
        <Route exact path="/" component={Home} />
        <Route path="/about" component={About} />
        <Route path="/contact" component={Contact} />
      </Switch>
    </Router>
  );
}

export default AppRouter;
```


### ✅ Controlled Components: 
These are components whose value is controlled by React state. The value of the component is set by the state and changes are handled by event handlers.

![4](https://github.com/shanibider/React-Vite.js/assets/72359805/389ad64f-78c9-44ac-bfed-8fe814aecb68)

<br>


## 🏆 Virtual DOM
React uses a virtual DOM to optimize the performance of rendering updates. Instead of directly updating the DOM on every state change, React updates a virtual DOM tree and then calculates the most efficient way to update the actual DOM.
This concept is more theoretical and doesn't have a specific example code to demonstrate.
<br>

## 🏆 JSX (JavaScript XML):
JSX is a syntax extension for JavaScript that allows developers to write HTML-like code within JavaScript. JSX makes it easier to write and understand React components by combining HTML and JavaScript syntax.

<br>




<br>
<br>


# Important React Examples from my code 💻 - 

<img align="center" height="300px" src="https://github.com/shanibider/React-Vite.js/assets/72359805/0251929c-296f-467a-9cdb-88708003a4d2">

# 1. 🎯Arrow functions -
![react arrow functions](https://github.com/shanibider/React-Vite.js/assets/72359805/f42200d9-d43b-4ee1-87d3-ac53b3c726cd)



# 2. 🎯useState -
### 🖊 Syntax:
<img height="280px" src="https://github.com/shanibider/React-Vite.js/assets/72359805/9e40f176-214c-4640-ae1d-be89b211e250">

### 🔎Example 1  - 
![useState1](https://github.com/shanibider/React-Vite.js/assets/72359805/1bb6a7ac-88e0-40af-ad21-421e2d0be0d7)


## 🖥React useState Example - 
![react-useState](https://github.com/shanibider/React-Vite.js/assets/72359805/d0b36f31-1f12-4a64-82e6-ffc4aa233ae3)


### 🔎Example 2  - 
![useStateexample-2](https://github.com/shanibider/React-Vite.js/assets/72359805/b1f96e70-14b0-4d97-ba67-d0c806eabe35)



# 3. 🎯Event Handling -
![eventHandling](https://github.com/shanibider/React-Vite.js/assets/72359805/2f1fe253-a7c3-4bef-b4a2-652399b09b90)

# 4. 🎯 Event Handling using Form -
![eventHandling+forms](https://github.com/shanibider/React-Vite.js/assets/72359805/6692d7fd-8cca-4449-9170-a5c10808a254)

## 🖥 React Form Example - 
![forms](https://github.com/shanibider/React-Vite.js/assets/72359805/1dbbbecc-07af-4682-8521-e9131524246b)


# 5. 🎯 Changing Complex State -
![complex state](https://github.com/shanibider/React-Vite.js/assets/72359805/95cda713-1fc6-4e4e-abcc-ed67c6ba60bb)

# 6. Spread Operator 🎯
Using spread operator (...prevValue) to copy (shallow copy of objects or arrays) all properties from the previous state.
![spread operator](https://github.com/shanibider/React-Vite.js/assets/72359805/db1a4009-914b-49ff-a052-0b4bc3602087)




<br>

## Example 🔎
Here's a simple example of a React component using JSX:

```jsx
import React from 'react';

// Functional component using JSX
const Greeting = ({ name }) => {
  return (
    <div>
      <h1>Hello, {name}!</h1>
      <p>Welcome to my React practice project.</p>
    </div>
  );
};
export default Greeting;


In this example:
We import the React module from the 'react' package.
We define a functional component named Greeting that takes a name prop.
Inside the component, we use JSX syntax to define the structure of the UI.
JSX allows us to write HTML-like code directly within JavaScript, making our components more expressive and readable.
We interpolate JavaScript expressions inside curly braces {} to dynamically insert values, such as the name prop.
To use this component in your application, simply import it and render it within another component or the main application:

import React from 'react';
import ReactDOM from 'react-dom';
import Greeting from './Greeting';

const App = () => {
  return (
    <div>
      <Greeting name="John" />
    </div>
  );
};
ReactDOM.render(<App />, document.getElementById('root'));

This will render the Greeting component with the name "John" inside the root element of your HTML document.
```




## About Vite.js <img height=30px src="https://skillicons.dev/icons?i=vite">

Vite is a modern build tool that aims to provide a fast development experience for web development. Developed by Evan You, the creator of Vue.js, Vite (French for "fast") leverages native ES Module (ESM) support in modern browsers to deliver near-instant cold server start times and blazing-fast hot module replacement (HMR) during development. Here are some key features and concepts of Vite.js:

- [x] 🥇 **ESM-Based Development**: Vite uses native ES Module (ESM) support in modern browsers to serve JavaScript modules directly without bundling. This eliminates the need for bundling during development, resulting in faster startup times and improved developer productivity.

- [x] 🥇 **Built-in Development Server**: Vite includes a built-in development server that serves your project with HMR enabled out of the box. Changes to your code are reflected instantly in the browser without requiring a full page reload, making the development experience extremely fast and efficient.

- [x] 🥇 **Optimized Production Builds**: When building for production, Vite leverages Rollup under the hood to generate optimized production builds. It automatically applies code splitting, tree shaking, and other optimizations to ensure small bundle sizes and optimal performance.

- [x] 🥇 **Plugin-Based Architecture**: Vite's architecture is designed to be highly extensible through plugins. You can enhance and customize Vite's behavior by adding plugins for features like CSS preprocessing, TypeScript support, and more.

- [x] 🥇 **Modern JavaScript Stack**: Vite embraces modern JavaScript features and tools, such as ES6/ESNext syntax, TypeScript, JSX, and CSS Modules. It provides first-class support for these technologies out of the box, enabling developers to build modern web applications with ease.

- [x] 🥇 **Framework Agnostic**: While Vite was initially developed with Vue.js in mind, it is not tied to any specific framework. You can use Vite to build projects with React, Preact, Svelte, or even plain HTML/CSS/JavaScript. Vite's flexibility makes it suitable for a wide range of web development projects.

- [x] 🥇 **Rich Developer Experience**: Vite prioritizes developer experience by focusing on fast feedback loops and seamless integration with modern tools like VS Code and browsers. It provides features like built-in CSS auto-prefixing, JSX support, and fast refresh to streamline the development process.

Vite's combination of speed, simplicity, and extensibility makes it an excellent choice for modern web development projects. Whether you're building a small prototype or a large-scale application, Vite can help you achieve fast and efficient development workflows.




# Useful Links 🖇️
[Babel: JavaScript compiler](https://babeljs.io/)


## Getting Started 🎯

To get started with these projects, follow these steps:

1. Clone this repository to your local machine:

   ```bash
   git clone <repository_url>
   ```

2. Navigate to the project directory:

   ```bash
   cd react-projects
   ```

3. Install dependencies using npm or yarn:

   ```bash
   npm install
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```


5. Open your browser and navigate to the development server's URL (usually http://localhost:3000).




## 📫 Connect with me 😊
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shani-bider/)
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://shanibider.github.io/Portfolio/)
[![gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shanibider@gmail.com)

<footer>
<p style="float:left; width: 20%;">
Copyright © Shani Bider, 2024
</p>
</footer>

## License📄

This project is licensed under the MIT License.
