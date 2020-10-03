@page learn-react/controlled-vs-uncontrolled-components Controlled vs Uncontrolled Components
@parent learn-react 5

@description Learn how to handle inputs in React and the difference between controlled and uncontrolled components.

@body

## Introduction 

One of the biggest mindset shifts for new developers learning React is the concept of a controlled vs uncontrolled component. This is something that is particularly important when building input components (text, checkbox, radio, etc).

There are two types of input components we can create in React, controlled inputs and uncontrolled inputs.

An uncontrolled input is one where we're not explicitly setting the value attribute. When a value attribute is not explicitly set, the input is ultimately controlled by the browser, and thus, out of the control of the React developer:

```html
<div id="root"></div><script crossorigin src="//unpkg.com/react@16/umd/react.development.js"></script><script crossorigin src="//unpkg.com/react-dom@16/umd/react-dom.development.js"></script><script type="jsx">ReactDOM.render(<SearchBar />,document.getElementById('root'));

// Uncontrolled
function SearchBar() {
  return <input type="text" />;
}

</script>
```
@codepen

The `SearchBar` above is considered uncontrolled because we're not explicitly giving it a value. The value of the input is now entirely determined by the browser & the user, we as developers have no say.

While this isn't necessarily a bad thing, it does make our lives as React developers more difficult. The reason being, at any given point in the lifecycle of this component, we don't know what the value of the input is. Assuming we'll want to use the value at some point, this becomes a problem. How do we access the input's value?

We can solve this problem by explicitly controlling the input (giving it a value).

```html  title="When we provide a value, we're controlling the input" subtitle="In this case, the user can't type anything"
<div id="root"></div><script crossorigin src="//unpkg.com/react@16/umd/react.development.js"></script><script crossorigin src="//unpkg.com/react-dom@16/umd/react-dom.development.js"></script><script type="jsx">ReactDOM.render(<SearchBar />,document.getElementById('root'));

// Controlled (sort of)
function SearchBar() {
  return <input type="text" value="hello" />;
}

</script>
```
@codepen

The component above is now considered to be "controlled", at any given point we always know what the value is (`hello`), and we've taken control away from the browser.

Obviously this isn't a great solution though because the value will always be "hello". We can remedy this by involving state:

```html
<div id="root"></div><script crossorigin src="//unpkg.com/react@16/umd/react.development.js"></script><script crossorigin src="//unpkg.com/react-dom@16/umd/react-dom.development.js"></script><script type="jsx">ReactDOM.render(<SearchBar />,document.getElementById('root'));

// Controlled (with state)
function SearchBar() {
  const [inputValue, setInputValue] = React.useState("")
  return (
    <input
      type="text"
      value={inputValue}
      onChange={e => setInputValue(e.target.value)}
    />
  )
}

</script>
```
@codepen

We'll create a piece of state called `inputValue`, use that as the value of the input, and update it whenever the input changes.

The process outlined above is how most controlled inputs are structured. Whether it's a textbox, a color picker or a checkbox, we can use this same stateful strategy to construct it. By storing the value in state, we always have access to it, and we can even control what the value ends up being.

We can take this a step further, by controlling the component with props:

```html 1:21 title="It's common to let a smart 'parent' component control the values"
<div id="root"></div><script crossorigin src="//unpkg.com/react@16/umd/react.development.js"></script><script crossorigin src="//unpkg.com/react-dom@16/umd/react-dom.development.js"></script><script type="jsx">ReactDOM.render(<SmartParentComponent />,document.getElementById('root'));

// Controlled (with props)
function SearchBar({inputValue, onInputValueChange}){
  return (
    <input
      type="text"
      value={inputValue}
      onChange={e => onInputValueChange(e.target.value)}
    />
  )
}

function SmartParentComponent(){
  const [inputValue, setInputValue] = React.useState("")

  return (
    <SearchBar
      inputValue={inputValue}
      onInputValueChange={newValue => setInputValue(newValue)}
    />
  )
}

</script>
```
@codepen

Above we've defined 2 component, `SmartParentComponent` and `SearchBar`. The `SearchBar` component accepts two props, one for the value of the input, and another for updating the value of the input. Notice that there is no state here, this is a dumb, stateless component.

The `SmartParentComponent` does have state however, it is keeping track of the input value and how to set the input value. These are then passed down into the dumb `SearchBar` component, and used to control it. 

This is another very common pattern. The idea is that we have a very simple, lightweight `SearchBar` component, which has no concept of state, instead it is entirely controlled by props passed down from a smart, stateful parent.


## Exercise

Let's use our knowledge of controlled vs uncontrolled components to build an input component! (note this will not be apart of the tic-tac-toe game)

Run the app locally with `npm start` and choose the `Controlled vs Uncontrolled` exercise. Now head over to `src/exercises/a - Controlled vs Uncontrolled/components`. These are the files you'll be editing.

### The problem

✏️ You'll be modifying the `Search` component so that it is a controlled input. Specifically, try your hand at the following:

- Modify the `Search` component below so that it's value is controlled by state. 
- Modify the clear button so that, when clicked, it clears out the value of the input. 
- Make it so that the clear button is only visible when there is text in the input.

### The solution

#### Search

```jsx
import React, { useState } from 'react';

function Search() {
  const [value, setValue] = useState('');

  return (
    <div className="search-container">
      <input
        className="search"
        value={value}
        onChange={(e) => setValue(e.target.value)}
      />
      {value && (
        <div className="clear" onClick={() => setValue('')}>
          X
        </div>
      )}
    </div>
  );
}

export default Search;
```
@highlight 4,10,11,13,14,only