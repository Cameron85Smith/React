# React

## Definition

**TypeScript** is a language that is a super set of Javascript. It adds static typing to the language where It helps us catch errors early in the development process.

**Statically-Typed** is a programming language characteristic in which variable types are explicitly declared and thus are determined at compile time. This lets the compiler decide whether a given variable can perform the actions requested from it or not. Static typing associates types with variables, not with values.

**React** is a Javascript library for building dynamic and interactive user interfaces. With ReactJS, we don’t need to worry about updating and querying DOM elements. Instead, we describe a webpage as using small, reusable components where ReactJS will take care of efficiently updating and querying DOM elements.

#### React Behind the Scenes

When the application starts, React takes the component tree and builds a Javascript data structure called the Virtual DOM. The Virtual DOM is different from the actual DOM in the browser as it is a lightweight, in-memory representation of our component tree where each node represents a component and its properties. When the state or the data of a component changes, React updates the corresponding node in the Virtual Dom to reflect the new state. It then proceeds to compare this current Virtual DOM with the previous virtual DOM to check which components need to be updated and then it proceeds to update those nodes in the actual DOM. Technically, updating the DOM is done by a companion library called React DOM. React DOM is one of the dependencies that we find in the package.json file.

#### React Ecosystem

We often need libraries that address concerns like:
- Routing (Going from one page to another)
- HTTP (Making HTTP calls)
- Managing the application state
- Internatialisation
- Form Validation
- Animation

The beauty of React is that it does not have an opinion on which library to use for the aforementioned concerns. We can use the right tool for the job.

## JavaScript Refresher

#### The Script Tag
###### <u>JavaScriptRefresher Project</u>

By convention, we add JavaScript to our website by using the **\<script></script>** import tag. The import is a navigation to a folder that holds the scripts. We create this separate scripts folder because as Software Engineers, this helps us to maintain complex JavaScript apps that make the code base easier to navigate, maintain, and understand.

We can also add extra attributes to the scripts tag like the **defer** attribute which implies that the script will only run after the rest of the HTML document has been read and passed. This ensures that if your script needs to run with HTML elements, the **defer** keyword will load the script once all the HTML elements are loaded.

Alternatively, we can move the **\<script></script>** tag to the end of the **\<body></body>** section.

In modern JavaScript projects we use the **\<type></type>** attribute tag which is set to **module** where this attribute makes sure that the script is treated like a JavaScript module. This allows us to use the import syntax in our script where we can import code from script A into script B.

This script will now be part of the web page when the web page is loaded.

```
<script src="assets/scripts/app.js"></script>
```

###### <u>ReactVSVanilla Project</u>

In comparison to the JavaScriptRefresher project, if we inspect the <b>index.html</b> file, we will notice that we are not using any script tags at all. If we open Developer Tools in the browser and inspect the <b>index.html</b>, you will see that now, there are script tags in the file. This is explained in the next section, <b>The Reaact Build Process</b>.

#### The React Build Process

It is important to note that in the context of React, we will never add **\<script></script>** tags to our HTML files on our own because React projects always use a build process which, as part of the process, injects the **\<script></script>** tags into the HTML code for us. React transforms our code before it is handed over to the browser. This transformation is done with the help of the **react-scripts** library that runs in the background. This library is referenced in the **package.json** file that holds a list of all of the dependencies for the project.

#### The Import/Export Syntax