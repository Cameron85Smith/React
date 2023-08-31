# React

## Definition

**TypeScript** is a language that is a super set of Javascript. It adds static typing to the language where It helps us catch errors early in the development process.

**Statically-Typed** is a programming language characteristic in which variable types are explicitly declared and thus are determined at compile time. This lets the compiler decide whether a given variable can perform the actions requested from it or not. Static typing associates types with variables, not with values.

**React** is a Javascript library for building dynamic and interactive user interfaces. With ReactJS, we don’t need to worry about updating and querying DOM elements. Instead, we describe a webpage as using small, reusable components where ReactJS will take care of efficiently updating and querying DOM elements.

### React Behind the Scenes
When the application starts, React takes the component tree and builds a Javascript data structure called the Virtual DOM. The Virtual DOM is different from the actual DOM in the browser as it is a lightweight, in-memory representation of our component tree where each node represents a component and its properties. When the state or the data of a component changes, React updates the corresponding node in the Virtual Dom to reflect the new state. It then proceeds to compare this current Virtual DOM with the previous virtual DOM to check which components need to be updated and then it proceeds to update those nodes in the actual DOM. Technically, updating the DOM is done by a companion library called React DOM. React DOM is one of the dependencies that we find in the package.json file.

### React Ecosystem
We often need libraries that address concerns like:
- Routing (Going from one page to another)
- HTTP (Making HTTP calls)
- Managing the application state
- Internatialisation
- Form Validation
- Animation

The beauty of React is that it does not have an opinion on which library to use for the aforementioned concerns. We can use the right tool for the job.