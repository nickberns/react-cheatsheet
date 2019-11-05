## JSX must return a single element. 
### This means that you need to create one root HTML element, e.g. <div>
```html
<div>
  <p>Paragraph One</p>
  <p>Paragraph Two</p>
  <p>Paragraph Three</p>
</div>
```
## Comments inside JSX
```html
{/* Comment */}
```
## Any HTML emelent inside JSX can be self closing
### But self closing elements can't contain any content

```html
<div />
<br />
```

## JavaScript code inside JSX
```html
{ let a =5 }
```
## Render JSX to DOM

```html
const JSX = (
<div>
  <h1>Hello World</h1>
  <p>Lets render this to the DOM</p>
</div>
);
```

ReactDOM.render(JSX,document.getElementById('example-node'));

## JSX Elements can't use reserved Javascript words
### all HTML attributes and event references have to be written in CamelCase

```html
class -> className
onclick -> onClick
onchange -> onChange
```

## Stateless React Component
### Can be created via a function
### Function name must begin with a Capital

```html
const MyComponent = function() {
  return(
      <div>Hello</div>
  );
 };
```
## Stateful React Component
### Create via class ES6 method
```html
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return(
    <div>
      <h1>Hello React!</h1>
    </div>
    );
  }
};
```
## JSX Parent Component with Child Components
### The Children are nested within the Parent
```html
return (
 <App>
  <Navbar />
  <Dashboard />
  <Footer />
 </App>
);
```
## Render React component to DOM
```html
ReactDOM.render(<TypesOfFood />,document.getElementById('challenge-node'));
```
## Default props
```html
MyComponent.defaultProps = { location: 'San Francisco' }
```
## Pass integer as props
```html
<Items quantity={10} />
```
## Pass string as props
```html
<Items quantity='ten' />
```
## PropTypes
### Here's an example to require the type function for a prop called handleClick:
```html
MyComponent.propTypes = { handleClick: PropTypes.func.isRequired }
```
1. Spell the type as full name except for 2 exceptions: bool & func
2. It needs to be imported 
```html
import React, { PropTypes } from 'react';
```
## Always start component names with a capital letter.
React treats components starting with lowercase letters as DOM tags. For example, <div /> represents an HTML div tag, but <Welcome /> represents a component and requires Welcome to be in scope.

## All React components must act like pure functions with respect to their props.

Converting a Function to a Class

You can convert a function component like Clock to a class in five steps:

1. Create an ES6 class, with the same name, that extends React.Component.
2. Add a single empty method to it called render().
3. Move the body of the function into the render() method.
4. Replace props with this.props in the render() body.
5. Delete the remaining empty function declaration.

```html
class Clock extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.props.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}
```
