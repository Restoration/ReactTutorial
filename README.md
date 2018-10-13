# ReactTutorial

## Overview
Important points in the React tutorial.  
[Tutorial: Intro to React](https://reactjs.org/tutorial/tutorial.html)

React tutorial is four section.
- Setup
- Basic writing style
- Implement system
- Past reference

## What is React?
React is a declarative, efficient, and flexible JavaScript library for building user interfaces. 
It lets you compose complex UIs from small and isolated pieces of code called “components”. 

### Prerequistes
You have some familiarity with HTML and JavaScript or you know a different programming language. 
And also you’re familiar with programming concepts like functions, objects, arrays, and to a lesser extent, classes. 

## What is props?
A component takes in parameters, called props (short for “properties”), and returns a hierarchy of views to display via the render method.

## Function
```
<button className="square" onClick={function() { alert('click'); }}>
<button className="square" onClick={() => alert('click')}>
```
Notice how with `onClick={() => alert('click')}`, we’re passing a function as the onClick prop. 
It only fires after a click. Forgetting `() =>` and writing `onClick={alert('click')}` is a common mistake, and would fire the alert every time the component re-renders. 

## Constructor
In JavaScript classes, you need to always call super when defining the constructor of a subclass. 
All React component classes that have a constructor should start it with a super(props) call. 

## immutability
Why immutability is important? Becaouse, immutability makes complex features much easier to implement. 
In application, an ability to undo and redo certain actions is a common requirement. 
Avoiding direct data mutation lets us keep previous versions history intact, and reuse them later. 

### About detecting changes
Detecting changes in mutable objects is difficult because they are modified directly. 
This detection requires the mutable object to be compared to previous copies of itself and the entire object tree to be traversed. 
Detecting changes in immutable objects is considerably easier. If the immutable object that is being referenced is different than the previous one, then the object has changed. 

### Re-render in React
The main benefit of immutability is that it helps you build pure components in React. 
Immutable data can easily determine if changes have been made which helps to determine when a component requires re-rendering. 

## Function component
In React, function components are a simpler way to write components that only contain a render method and don’t have their own state. 
Instead of defining a class which extends React.Component, we can write a function that takes props as input and returns what should be rendered. 
Function components are less tedious to write than classes, and many components can be expressed this way.

## key
key is a special and reserved property in React (along with ref, a more advanced feature). 
When an element is created, React extracts the key property and stores the key directly on the returned element. 
Even though key may look like it belongs in props, key cannot be referenced using this.props.key. React automatically uses key to decide which components to update. 
A component cannot inquire about its key. 
Keys do not need to be globally unique. Keys only need to be unique between components and their siblings.

