# React Comment Box

The tutorial from React JS official site to create a comment box and show how good React is.

## React Documentation at a High Level

### React Component

React Component is a modular in React where a single part of the application is created it renders to the screen. The render uses uses a XMLish type of tags called JSX. Which simple precompilers than translates the syntactic sugar to plain JavaScript. So in actually it would look like this with use of hashes and function createElement in order for JavaScript to use it.

```
var CommentBox = React.createClass({
displayName: 'CommentBox',
  render: function() {
    return (
      React.createElement('div', {className: "commentBox"},
        "Hello, world! I am a CommentBox."
      )
    );
  }
});
React.render(
  React.createElement(CommentBox, null),
  document.getElementById('content')
);
```

You can also add in additional other React components into render
allowing for nesting of components and isolated components to keep code
easy to maintain.

### Props

Props, they are like public valuables where the developer can access them and set the valuables for them.  In order to do this add them to the React Component tag as a attribute
with the name of the prop and the value you would like to set. In this
cast `<Comment author="Jason">This comment</comment>`. Furthermore, by
using `this.props.children` you can access the text or other tags between
the opening and closing tags.

### State

State is like a private valuable for a component it can only be access from that
component. 

 - To set a state you will need to add `getInitialState()` to that component and declare that state valuables.
 - To set a state outside of a `getInitialState()` it is `this.setState({stateName: value})`
this will course the component to re-render in order to keep it up to
data with the latest data from the state. 
 - To access those state it is similar to props `this.state.stateName`

### Other

 - **dangerouslySetInnerHTML**
  - React protect its developers from XSS attacks by default it turns any HTML into harmless strings. This can be override and as long you know that the source of the HTML is secure. By adding dangerouslySetInnerHTML attribute to a HTML tag you can set the inter HTML to render as HTML in the browser.

 - **findDOMNode**
  - To get the properties and functions for those tags

 - **this.refs**
  - this.refs Reacts way of find tags in the render

