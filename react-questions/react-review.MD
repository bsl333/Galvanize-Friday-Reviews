## React Questions 8-16-2016

##### Explain the difference between a class component and a functional component.
<details>
  <summary>Answer:</summary>
  class components maintain state and must have a render function.
</details>



##### Why should forms be class components?
<details>
  <summary>Answer:</summary>
  Form elements naturally keep some internal state (i.e. input fields in the form).
</details>


##### Describe the difference between a programming language and a framework such as React.
<details>
  <summary>Answer:</summary>
  A programming language is the dialect in which code is written, requiring the specific use and placement of 
  characters and keywords. A framework like React is a collection of libraries and methods, written in a particular 
  language (Javascript in this case) and is used with that language to provide extra functionality.
</details>



##### What is the `props` property, and how do you access it when passing information from a parent to child class component? How about for a functional component
<details>
  <summary>Answer:</summary>
  The props property are the inputs passed down from a parent to a child component - they can be of any data type. 
  Class component: `this.props.property`
  functuonal component: destructure in function`({property1, property2})` declaration, or `props.propery`
</details>


##### Name at least 3 React Lifecycle methods.
<details>
  <summary>Answer:</summary>
  componentWillMount, render, componentDidMount
</details>



##### Why should you manage state with setState() rather than manually editing this.state?
<details>
  <summary>Answer:</summary>
  setState() re-renders its component (unless shouldComponentUpdate() returns false)
</details>


##### Why would you lift state up to a parent component?

<details>
  <summary>Answer:</summary>
  When several components require (and change with) the same changing data.
</details>
