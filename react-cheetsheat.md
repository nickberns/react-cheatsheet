## JSX must return a single element. 
### This means that you need to create one root HTML element, e.g. <div>

<div>
  <p>Paragraph One</p>
  <p>Paragraph Two</p>
  <p>Paragraph Three</p>
</div>

## Comments inside JSX

{/* Comment */}

## JavaScript code inside JSX

{ let a =5 }

## Render JSX to DOM

`const JSX = (
  <div>
    <h1>Hello World</h1>
    <p>Lets render this to the DOM</p>
  </div>
);`

ReactDOM.render(JSX,document.getElementById('example-node'));

## JSX Elements can't use reserved Javascript words
### all HTML attributes and event references have to be written in CamelCase

class -> className
onclick -> onClick
onchange -> onChange
