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
