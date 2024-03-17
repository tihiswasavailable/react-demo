# **React-demo**
## **Thinking in React**
When you build a user interface with React, you will first break it apart into pieces called components. Then, you will describe the different visual states for each of your components. Finally, you will connect your components together so that the data flows through them.

![thinking-in-react](/images/react-demo.png)
- FilterableProductTable (grey) contains the entire app.
  - SearchBar (blue) receives the user input.
  - ProductTable (lavender) displays and filters the list according to the user input.
    - ProductCategoryRow (green) displays a heading for each category.
    - ProductRow (yellow) displays a row for each product.




Structure of the project:

- **App.js** - the main React component which is the entry point of the application. It renders the `HelloWorld` component.
- **index.js** - the main file which renders the `App` component in the DOM.
- **TodoList.js** - a simple component
- **index.html** - the main HTML file which is served by the server. It contains a div with the id `root` where the React application is rendered. 


## **Entry point**
In the `index.html` file, there is a div with the id `root` where the React application is rendered.
````html
 <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
  </body>
````

The entry point of the application is the `index.js` file. It renders the `App` component in the DOM.
````javascript
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';


const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
````
In the `App.js` file, the `TodoList` component is rendered.
````javascript
import React from 'react';
import TodoList from './TodoList';

function App() {
  return (
    <TodoList/>
  )
}

export default App;
````
In the `TodoList.js` file, the `TodoList` component is rendered.
````javascript
import React from "react";

function TodoList() {
    return(
    <div>
        <h1>Hello and welcome!</h1>
        <input type="text" />
        <button>Add</button>
    </div>
)}

export default TodoList;
````



