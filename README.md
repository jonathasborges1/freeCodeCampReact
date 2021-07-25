# freeCodeCampReact
Repositório criado para armazenar as atividades https://www.freecodecamp.org/learn/front-end-libraries/react/


# Item 18 
## Contexto
> Use PropTypes to Define the Props You Expect
> React provides useful type-checking features to verify that components receive props of the correct type. For example, your application makes an API call to retrieve data that you expect to be in an array, which is then passed to a component as a prop. You can set propTypes on your component to require the data to be of type array. This will throw a useful warning when the data is of any other type. [...]

## Saida Esperada: 
~~~
⏳ The ShoppingCart component should render.
⏳ The Items component should render.
⏳ The Items component should include a propTypes check to require a value for quantity and ensure that its value is a number.
~~~

## Código Solução
~~~
const Items = (props) => {
  return <h1>Current Quantity of Items in Cart: {props.quantity}</h1>
};

// Change code below this line

// Change code above this line

Items.defaultProps = {
  quantity: 0
};
Items.propTypes = {
  quantity: PropTypes.number.isRequired
};

class ShoppingCart extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <Items />
  }
};
~~~

# Item 19 - access-props-using-this-props
## Contexto
> The last several challenges covered the basic ways to pass props to child components. But what if the child component that you're passing a prop to is an ES6 class component, rather than a stateless functional component? The ES6 class component uses a slightly different convention to access props. [...]

## Saída Espera
~~~
⏳ he ResetPassword component should return a single div element.

⏳ The fourth child of ResetPassword should be the ReturnTempPassword component.

⏳ The ReturnTempPassword component should have a prop called tempPassword.

⏳ The tempPassword prop of ReturnTempPassword should be equal to a string of at least 8 characters.

⏳ The ReturnTempPassword component should display the password you create as the tempPassword prop within strong tags.
~~~

## Código Solução
~~~
class ReturnTempPassword extends React.Component {
  constructor(props) {
    super(props);

  }
  render() {
    return (
        <div>
            { /* Change code below this line */ }
            <p>Your temporary password is: <strong>{this.props.tempPassword}</strong></p>
            { /* Change code above this line */ }
        </div>
    );
  }
};

class ResetPassword extends React.Component {
  constructor(props) {
    super(props);

  }
  render() {
    return (
        <div>
          <h2>Reset Password</h2>
          <h3>We've generated a new temporary password for you.</h3>
          <h3>Please reset this password from your account settings ASAP.</h3>
          { /* Change code below this line */ }

          { /* Change code above this line */ }
          <ReturnTempPassword tempPassword={"tempPassword"}/>
        </div>
    );
  }
};
~~~

# Item 20 - review-using-props-with-stateless-functional-components
## Contexto
>Except for the last challenge, you've been passing props to stateless functional components. These components act like pure functions. They accept props as input and return the same view every time they are passed the same props. You may be wondering what state is, and the next challenge will cover it in more detail. Before that, here's a review of the terminology for components. [...]

Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/review-using-props-with-stateless-functional-components

## Saída Espera
~~~
⏳ The CampSite component should render.

⏳ The Camper component should render.

⏳ The Camper component should include default props which assign the string CamperBot to the key name.

⏳ The Camper component should include prop types which require the name prop to be of type string.

⏳ The Camper component should contain a p element with only the text from the name prop.
~~~

## Código Solução
~~~
class CampSite extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <Camper />
      </div>
    );
  }
};
// Change code below this line
const Camper = (props) => <p>{props.name}</p>;
Camper.defaultProps = {name: "CamperBot"};
Camper.propTypes = {name:PropTypes.string.isRequired};
~~~
# Item 21 - create-a-stateful-component
## Contexto
> Except for the last challenge, you've been passing props to stateless functional components. These components act like pure functions. They accept props as input and return the same view every time they are passed the same props. You may be wondering what state is, and the next challenge will cover it in more detail. Before that, here's a review of the terminology for components. [...]

Fonte : https://www.freecodecamp.org/learn/front-end-libraries/react/create-a-stateful-component

## Saída Esperada
~~~
⏳ StatefulComponent should exist and render.

⏳ StatefulComponent should render a div and an h1 element.

⏳ The state of StatefulComponent should be initialized with a property name set to a string.

⏳ The property name in the state of StatefulComponent should render in the h1 element.
~~~

## Código Solução
~~~
class StatefulComponent extends React.Component {
  constructor(props) {
    super(props);
    // Only change code below this line
      this.state = {
        name : 'jhon'
      }
    // Only change code above this line
  }
  render() {
    return (
      <div>
        <h1>{this.state.name}</h1>
      </div>
    );
  }
};
~~~
# Item 22 - render-state-in-the-user-interface
## Contexto
> Once you define a component's initial state, you can display any part of it in the UI that is rendered. If a component is stateful, it will always have access to the data in state in its render() method. You can access the data with this.state. [...]

## Saída Esperada
~~~
⏳ MyComponent should have a key name with value freeCodeCamp stored in its state.

⏳ MyComponent should render an h1 header enclosed in a single div.

⏳ The rendered h1 header should only contain text rendered from the component's state.
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'freeCodeCamp'
    }
  }
  render() {
    return (
      <div>
        { /* Change code below this line */ }
        <h1> {this.state.name} </h1>
        { /* Change code above this line */ }
      </div>
    );
  }
};
~~~

# Item 23 - render-state-in-the-user-interface-another-way
## Contexto
> There is another way to access state in a component. In the render() method, before the return statement, you can write JavaScript directly. For example, you could declare functions, access data from state or props, perform computations on this data, and so on. Then, you can assign any data to variables, which you have access to in the return statement. [...]

Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/render-state-in-the-user-interface-another-way

## Saída Esperada
~~~
⏳ MyComponent should have a key name with value freeCodeCamp stored in its state.

⏳ MyComponent should render an h1 header enclosed in a single div.

⏳ The rendered h1 tag should include a reference to {name}.

⏳ The rendered h1 header should contain text rendered from the component's state.
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'freeCodeCamp'
    }
  }
  render() {
    // Change code below this line
    const name = this.state.name
    // Change code above this line
    return (
      <div>
        { /* Change code below this line */ }
          <h1>{name}</h1>
        { /* Change code above this line */ }
      </div>
    );
  }
};
~~~

Ítem 24 - set-state-with-this-setstate
## Contexto
> The previous challenges covered component state and how to initialize state in the constructor. There is also a way to change the component's state. React provides a method for updating component state called setState. You call the setState method within your component class like so: this.setState(), passing in an object with key-value pairs. The keys are your state properties and the values are the updated state data. For instance, if we were storing a username in state and wanted to update it, it would look like this: [...]

Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/set-state-with-this-setstate

## Saída Esperada
~~~
⏳ The state of MyComponent should initialize with the key value pair { name: Initial State }.

⏳ MyComponent should render an h1 header.

⏳ The rendered h1 header should contain text rendered from the component's state.

⏳ Calling the handleClick method on MyComponent should set the name property in state to equal React Rocks!.
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'Initial State'
    };
    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    // Change code below this line
      this.state.name = "React Rocks!" 
    // Change code above this line
  }
  render() {
    return (
      <div>
        <button onClick={this.handleClick}>Click Me</button>
        <h1>{this.state.name}</h1>
      </div>
    );
  }
};
~~~

#Item 25 - bind-this-to-a-class-method
## Contexto 
> In addition to setting and updating state, you can also define methods for your component class. A class method typically needs to use the this keyword so it can access properties on the class (such as state and props) inside the scope of the method. There are a few ways to allow your class methods to access this. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/bind-this-to-a-class-method

Saída Experada
~~~
⏳ MyComponent should return a div element which wraps two elements, a button and an h1 element, in that order.

⏳ The state of MyComponent should initialize with the key value pair { text: "Hello" }.

⏳ Clicking the button element should run the handleClick method and set the state text to You clicked!.
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      text: "Hello"
    };
    // Change code below this line

    // Change code above this line
  }
  handleClick() {
    this.setState({
      text: "You clicked!"
    });
  }
  render() {
    return (
      <div>
        { /* Change code below this line */ }
        <button onClick={this.handleClick.bind(this)}>Click Me</button>
        { /* Change code above this line */ }
        <h1>{this.state.text}</h1>
      </div>
    );
  }
};
~~~

# Iten 26 - use-state-to-toggle-an-element
## Contexto
> Sometimes you might need to know the previous state when updating the state. However, state updates may be asynchronous - this means React may batch multiple setState() calls into a single update. This means you can't rely on the previous value of this.state or this.props when calculating the next value. So, you should not use code like this: [...]

##### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/use-state-to-toggle-an-element

## Saída Esperada
~~~
⏳ MyComponent should return a div element which contains a button.

⏳ The state of MyComponent should initialize with a visibility property set to false.

⏳ Clicking the button element should toggle the visibility property in state between true and false.

⏳ An anonymous function should be passed to setState.

⏳ this should not be used inside setState
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      visibility: false
    };
    // Change code above this line
    this.toggleVisibility = this.toggleVisibility.bind(this);
  }
  // Change code below this line
  toggleVisibility () {
    this.setState(state => ({visibility : !state.visibility}))
  }
  render() {
    if (this.state.visibility) {
      return (
        <div>
          <button onClick={this.toggleVisibility}>Click Me</button>
          <h1>Now you see me!</h1>
        </div>
      );
    } else {
      return (
        <div>
          <button onClick={this.toggleVisibility}>Click Me</button>
        </div>
      );
    }
  }
}
~~~

# Item 27 - Write-a-simple-counter.
## Contexto
>You can design a more complex stateful component by combining the concepts covered so far. These include initializing state, writing methods that set state, and assigning click handlers to trigger these methods. [...]

##### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/write-a-simple-counter

## Saída Esperada
~~~
⏳ Counter should return a div element which contains three buttons with text content in this order Increment!, Decrement!, Reset.

⏳ The state of Counter should initialize with a count property set to 0.

⏳ Clicking the increment button should increment the count by 1.

⏳ Clicking the decrement button should decrement the count by 1.

⏳ Clicking the reset button should reset the count to 0
~~~

## Código Solução
~~~
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
    // Change code below this line
    this.increment = this.increment.bind(this);
    // Change code above this line
    this.decrement = this.decrement.bind(this);
    // Change code above this line
    this.reset = this.reset.bind(this);
  }
  increment (){
    this.setState (
      (state) => {return {count: state.count + 1}}
    )
  }
  // Change code below this line
  decrement (){
    this.setState (state => ({count: state.count - 1})
    )
  }
  // Change code above this line
  reset (){
    this.setState(
      (state) => {return {count: 0}}
    )
  }
  render() {
    return (
      <div>
        <button className='inc' onClick={this.increment}>Increment!</button>
        <button className='dec' onClick={this.decrement}>Decrement!</button>
        <button className='reset' onClick={this.reset}>Reset</button>
        <h1>Current Count: {this.state.count}</h1>
      </div>
    );
  }
};
~~~

# Item 28 - create-a-controlled-input
## Contexto - Create a Controlled Input
> Your application may have more complex interactions between state and the rendered UI. For example, form control elements for text input, such as input and textarea, maintain their own state in the DOM as the user types. With React, you can move this mutable state into a React component's state. The user's input becomes part of the application state, so React controls the value of that input field. Typically, if you have React components with input fields the user can type into, it will be a controlled input form.

##### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/create-a-controlled-input

## Saída Esperada
~~~
⏳ ControlledInput should return a div element which contains an input and a p tag.

⏳ The state of ControlledInput should initialize with an input property set to an empty string.

⏳ Typing in the input element should update the state and the value of the input, and the p element should render this state as you type.
~~~

## Código Solução
~~~
class ControlledInput extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: ''
    };
    // Change code below this line
    this.atualize = this.atualize.bind(this);
  }
  // Change code below this line
  atualize (e){
    this.setState({
      input: e.target.value
      })
  }
  render() {
    return (
      <div>
        <input 
        type="text" 
        onChange={this.atualize} 
        value={this.state.input}
        />
        <h4>Controlled Input:</h4>
        <p>{this.state.input}</p>
      </div>
    );
  }
};
~~~
# Item 29 - Create a Controlled Form
## Contexto - Create a Controlled Form
> The last challenge showed that React can control the internal state for certain elements like input and textarea, which makes them controlled components. This applies to other form elements as well, including the regular HTML form element. [...]

##### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/create-a-controlled-form

## Saída Esperada
~~~
⏳ MyForm should return a div element which contains a form and an h1 tag. The form should include an input and a button.

⏳ The state of MyForm should initialize with input and submit properties, both set to empty strings.

⏳ Typing in the input element should update the input property of the component's state.

⏳ Submitting the form should run handleSubmit which should set the submit property in state equal to the current input.

⏳ handleSubmit should call event.preventDefault

⏳ The h1 header should render the value of the submit field from the component's state.
~~~

## Código Solução
~~~
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: '',
      submit: ''
    };
    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }
  handleChange(event) {
    this.setState({
      input: event.target.value
    });
  }
  handleSubmit(event) {
    this.setState({
      submit: this.state.input
    });
    event.preventDefault()
  }
  
  render() {
    return (
      <div>
        <form onSubmit={this.handleSubmit}>
          
          <input 
          type="text" 
          value={this.state.input} 
          onChange={this.handleChange}
          />

          <button type='submit'>Submit!</button>
            
        </form>
        <h1>{this.state.submit}</h1>
      </div>
    );
  }
}
~~~

# Item 30 -
## Contexto - Pass State as Props to Child Components
> You saw a lot of examples that passed props to child JSX elements and child React components in previous challenges. You may be wondering where those props come from. A common pattern is to have a stateful component containing the state important to your app, that then renders child components. You want these components to have access to some pieces of that state, which are passed in as props

## Fonte : https://www.freecodecamp.org/learn/front-end-libraries/react/pass-state-as-props-to-child-components

## Saída Esperada
~~~
⏳ The MyApp component should render with a Navbar component inside.

⏳ The Navbar component should receive the MyApp state property name as props.

⏳ The h1 element in Navbar should render the name prop.
~~~

## Código Solução
~~~
class MyApp extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'CamperBot'
    }
  }
  render() {
    return (
       <div>
         <Navbar name = {this.state.name}/>
       </div>
    );
  }
};

class Navbar extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <h1>Hello, my name is:{this.props.name}</h1>
    );
  }
};
~~~
