# react_components_introduction
Created with [CodeSandbox](https://codesandbox.io/)      
Notes from React module    
[The Complete 2021 Web Development Bootcamp](https://www.udemy.com/course/the-complete-web-development-bootcamp/)  
Instructor: Dr. Angela Yu      

## Description
This project is just a list of of foods.        
The list is repeated twice, just to show how easy is to reuse components using React.    
Our App component uses the components Heading and List (used twice)      

## Notes
React Components allow us to split up large files or a complex web structure         
into smaller components AND reuse these components.     

### Basic Componenct Creation:

React: Best Practice Documentation:     
[Airbnb React / JSX Style Guide](https://github.com/airbnb/javascript/tree/master/react)       

Eg: A Heading Component      
We will usually leave index.js as a plain JavaScript file (even if we're using some React and JSX in it).   
All of our components will be separated into individual files with the JSX extension:       
Heading.jsx (in react_components_introduction/src/components/)        
We have to use the ES6 import / export functionality into each individual component.    

```
import React from "react";

function Heading() {
  return <h1>My Favourite Foods</h1>;
}
export default Heading;
```
And now, we can import this component in our JS/JSX files.

### Components in Real projects:
Normally in the index.js of a lot of React apps we will have just a single custom component called `<App />` .      
And inside a directory called components, we can find a custom file: App.jsx .       
And in App.jsx all the import statements that would render our components:     

```
import React from "react";
import Heading from "./Heading";
import List from "./List";

function App() {
  return (
    <div>
      <Heading />
      <List />
    </div>
  );
}
export default App;

```

This way our code is modular.     
Each of these components can now be reused as and when we want to.     
And these files are a lot shorter and a lot more manageable.     

## What I have learned with this project:      
* Make my code more modular: shorter, reusable and simpler
* Conventions to separate and store React Components 
* ES6 import / export functionality
