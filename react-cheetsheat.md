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

{/* Comment */}

## Any HTML emelent inside JSX can be self closing
### But self closing elements can't contain any content

```html
<div />
<br />
```

## JavaScript code inside JSX

{ let a =5 }

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

