# ReactTutorial

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
In JavaScript classes, you need to always call super when defining the constructor of a subclass. All React component classes that have a constructor should start it with a super(props) call.

