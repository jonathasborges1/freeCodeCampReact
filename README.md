# freeCodeCampReact
Repositório criado para armazenar as atividades https://www.freecodecamp.org/learn/front-end-libraries/react/


# Item 01 - Use PropTypes to Define the Props You Expect
## Contexto
> React is an Open Source view library created and maintained by Facebook. It's a great tool to render the User Interface (UI) of modern web applications. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/create-a-simple-jsx-element

## Saida Esperada: 
~~~
⏳ The constant JSX should return an h1 element.

⏳ The h1 tag should include the text Hello JSX!
~~~

## Código Solução
~~~
const JSX =  <h1>Hello JSX!</h1>;
~~~

# Item 02 - Create a Complex JSX ElementPassed
## Contexto
> The last challenge was a simple example of JSX, but JSX can represent more complex HTML as well [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/create-a-complex-jsx-element

## Saida Esperada: 
~~~
⏳ The constant JSX should return a div element.

⏳ The div should contain an h1 tag as the first element.

⏳ The div should contain a p tag as the second element.

⏳ The div should contain a ul tag as the third element.

⏳ The ul should contain three li elements.
~~~

## Código Solução
~~~
const JSX = 
<div> 
 <h1></h1> 
 <p></p>
 <ul> <li></li> <li></li> <li></li> </ul> 
</div>
~~~

# Item 03 - Add Comments in JSXPassed
## Contexto
> SX is a syntax that gets compiled into valid JavaScript. Sometimes, for readability, you might need to add comments to your code. Like most programming languages, JSX has its own way to do this [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/add-comments-in-jsx

## Saida Esperada: 
~~~
⏳ The constant JSX should return a div element.

⏳ The div should contain an h1 tag as the first element.

⏳ The div should contain a p tag as the second element.

⏳ The existing h1 and p elements should not be modified.

⏳ The JSX should use valid comment syntax.
~~~

## Código Solução
~~~
const JSX = (
  <div>{/* Comments */}
    <h1>This is a block of JSX</h1>
    <p>Here's a subtitle</p>
  </div>
);
~~~

# Item 04 - Render HTML Elements to the DOM Passed
## Contexto
> o far, you've learned that JSX is a convenient tool to write readable HTML within JavaScript. With React, we can render this JSX directly to the HTML DOM using React's rendering API known as ReactDOM. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/render-html-elements-to-the-dom

## Saida Esperada: 
~~~
⏳ The constant JSX should return a div element.

The div should contain an h1 tag as the first element.

The div should contain a p tag as the second element.

The provided JSX element should render to the DOM node with id challenge-node.
~~~

## Código Solução
~~~
const JSX = (
  <div>
    <h1>Hello World</h1>
    <p>Lets render this to the DOM</p>
  </div>
);
// Change code below this line
ReactDOM.render(JSX,document.getElementById("challenge-node"));
~~~

# Item 05 - Render HTML Elements to the DOM Passed
## Contexto
> o far, you've learned that JSX is a convenient tool to write readable HTML within JavaScript. With React, we can render this JSX directly to the HTML DOM using React's rendering API known as ReactDOM. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/render-html-elements-to-the-dom

## Saida Esperada: 
~~~
⏳ The constant JSX should return a div element.

⏳ The div should have a class of myDiv
~~~

## Código Solução
~~~
const JSX = (
  <div className="myDiv">
    <h1>Add a class to this div</h1>
  </div>
);

~~~

# Item 06 - Learn About Self-Closing JSX Tags
## Contexto
> So far, you’ve seen how JSX differs from HTML in a key way with the use of className vs. class for defining HTML classes. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/learn-about-self-closing-jsx-tags

## Saida Esperada: 
~~~
⏳ The constant JSX should return a div element.

⏳ The div should contain a br tag.

⏳ The div should contain an hr tag.
~~~

## Código Solução
~~~
const JSX = (
  <div>
    <h2>Welcome to React!</h2>
    <p>Be sure to close all tags!</p>
    <br></br>
    <hr></hr>
  </div>
);
~~~

# Item 07 - Create a Stateless Functional Component
## Contexto
> Components are the core of React. Everything in React is a component and here you will learn how to create one [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/create-a-stateless-functional-component

## Saida Esperada: 
~~~
⏳ MyComponent should return JSX.

⏳ MyComponent should return a div element.

⏳ The div element should contain a string of text.
~~~

## Código Solução
~~~
const MyComponent = function() {
  return (
      <div>
        
        Jonathas
      </div>
  )
}

~~~

# Item 08 - Create a React Component
## Contexto
> The other way to define a React component is with the ES6 class syntax. In the following example, Kitten extends React.Component: [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/create-a-react-component

## Saida Esperada: 
~~~
⏳ The React component should return a div element.

⏳ The returned div should render an h1 header within it.

⏳ The h1 header should contain the string Hello React!.

~~~

## Código Solução
~~~
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
}
~~~

# Item 09 - Create a Component with Composition
## Contexto
> Now we will look at how we can compose multiple React components together. Imagine you are building an app and have created three components: a Navbar, Dashboard, and Footer[...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/create-a-component-with-composition

## Saida Esperada: 
~~~
⏳ The React component should return a single div element.

⏳ The component should return two nested elements.

⏳ The component should return the ChildComponent as its second child.
~~~

## Código Solução
~~~
const ChildComponent = () => {
  return (
    <div>
      <p>I am the child</p>
    </div>
  );
};

class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>I am the parent</h1>
        <ChildComponent />
      </div>
    );
  }
};
~~~

# Item 10 - Use React to Render Nested ComponentsPassed
## Contexto
> The last challenge showed a simple way to compose two components, but there are many different ways you can compose components with React. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/use-react-to-render-nested-components

## Saida Esperada: 
~~~
⏳ The TypesOfFood component should return a single div element.

⏳ The TypesOfFood component should return the Fruits component.

⏳ The Fruits component should return the TypesOfFruit component.

⏳ The TypesOfFruit component should return the h2 and ul elements
~~~

## Código Solução
~~~
const TypesOfFruit = () => {
  return (
    <div>
      <h2>Fruits:</h2>
      <ul>
        <li>Apples</li>
        <li>Blueberries</li>
        <li>Strawberries</li>
        <li>Bananas</li>
      </ul>
    </div>
  );
};

const Fruits = () => {
  return (
    <div>
    <TypesOfFruit/>
    </div>
  );
};
class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        <Fruits />
      </div>
    );
  }
};
~~~
---

# Item 11 - Compose React ComponentsPassed
## Contexto
> As the challenges continue to use more complex compositions with React components and JSX, there is one important point to note. Rendering ES6 style class components within other components is no different than rendering the simple components you used in the last few challenges. You can render JSX elements, stateless functional components, and ES6 class components within other components. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/compose-react-components

## Saida Esperada: 
~~~
⏳ The TypesOfFood component should return a single div element.

⏳ The TypesOfFood component should return the Fruits component.

⏳ The Fruits component should return the NonCitrus component and the Citrus component.

⏳ The TypesOfFood component should return the Vegetables component below the Fruits component.
~~~

## Código Solução
~~~
const NonCitrus = () =>{
  return(
      <div></div>
  );
}

const Citrus = () =>{
  return(
      <div></div>
  );
}

class Fruits extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h2>Fruits:</h2>
        <NonCitrus/>
        <Citrus/>
      </div>
    );
  }
};
class TypesOfFood extends React.Component {
  constructor(props) {
     super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        <Fruits/>
        <Vegetables />
      </div>
    );
  }
};
~~~

# Item 12 - Render a Class Component to the DOM
## Contexto
> You may remember using the ReactDOM API in an earlier challenge to render JSX elements to the DOM. The process for rendering React components will look very similar. The past few challenges focused on components and composition, so the rendering was done for you behind the scenes. However, none of the React code you write will render to the DOM without making a call to the ReactDOM API. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/render-a-class-component-to-the-dom

## Saida Esperada: 
~~~
⏳ The TypesOfFood component should return a single div element.

⏳ The TypesOfFood component should render the Fruits component after the h1 element.

⏳ The TypesOfFood component should render the Vegetables component after Fruits.

⏳ The TypesOfFood component should render to the DOM within the div with the id challenge-node.
~~~

## Código Solução
~~~
class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        <Fruits />
        <Vegetables />
      </div>
    );
  }
};
ReactDOM.render(
  <TypesOfFood/>,
  document.getElementById('challenge-node')
);
const Fruits = () => {
  return (
   <div>
      <h2>Fruits:</h2>
      <h4>Non-Citrus:</h4>
        <ul>
          <li>Apples</li>
          <li>Blueberries</li>
          <li>Strawberries</li>
          <li>Bananas</li>
        </ul>
      <h4>Citrus:</h4>
        <ul>
          <li>Lemon</li>
          <li>Lime</li>
          <li>Orange</li>
          <li>Grapefruit</li>
        </ul>
    </div>
  )
}
const Vegetables = () => {
  return (
    <div>
      <h2>Vegetables:</h2>
      <ul>
        <li>Brussel Sprouts</li>
        <li>Broccoli</li>
        <li>Squash</li>
      </ul>
    </div>
  )
}
~~~

# Item 13 - Write a React Component from Scratch
## Contexto
> Now that you've learned the basics of JSX and React components, it's time to write a component on your own. React components are the core building blocks of React applications so it's important to become very familiar with writing them. Remember, a typical React component is an ES6 class which extends React.Component. It has a render method that returns HTML (from JSX) or null. This is the basic form of a React component. Once you understand this well, you will be prepared to start building more complex React projects [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/write-a-react-component-from-scratch

## Saida Esperada: 
~~~
⏳ There should be a React component called MyComponent.

⏳ MyComponent should contain an h1 tag with text My First React Component! Case and punctuation matter.

⏳ MyComponent should render to the DOM.

⏳ MyComponent should have a constructor calling super with props.
~~~

## Código Solução
~~~
// Change code below this line
class MyComponent extends React.Component {
  constructor(props){
    super(props);
  }
  render (){
    return (
      <div>
        <h1>My First React Component!</h1>
      </div>
   )
  }
};
ReactDOM.render(<MyComponent/>, document.getElementById('challenge-node'));
~~~


# Item 14 - Pass Props to a Stateless Functional Component
## Contexto
>  The previous challenges covered a lot about creating and composing JSX elements, functional components, and ES6 style class components in React. With this foundation, it's time to look at another feature very common in React: props. In React, you can pass props, or properties, to child components. Say you have an App component which renders a child component called Welcome which is a stateless functional component. You can pass Welcome a user property by writing [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/pass-props-to-a-stateless-functional-component

## Saida Esperada: 
~~~
⏳ The Calendar component should return a single div element.

⏳ The second child of the Calendar component should be the CurrentDate component.

⏳ The CurrentDate component should have a prop called date.

⏳ The date prop of the CurrentDate should contain a string of text.

⏳ The date prop should be generated by calling Date()

⏳ The CurrentDate component should render the value from the date prop in the p tag.
~~~

## Código Solução
~~~
const CurrentDate = (props) => {
  return (
    <div>
      <p>The current date is: {props.date} </p>
    </div>
  );
};

class Calendar extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h3>What date is it?</h3>
        <CurrentDate date={Date()} />
      </div>
    );
  }
};
~~~

# Item 15 - Pass an Array as PropsPassed
## Contexto
>  The last challenge demonstrated how to pass information from a parent component to a child component as props or properties. This challenge looks at how arrays can be passed as props. To pass an array to a JSX element, it must be treated as JavaScript and wrapped in curly braces.[...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/pass-an-array-as-props

## Saida Esperada: 
~~~
⏳ The ToDo component should return a single outer div.

⏳ The third child of the ToDo component should be an instance of the List component.

⏳ The fifth child of the ToDo component should be an instance of the List component.

⏳ Both instances of the List component should have a property called tasks and tasks should be of type array.

⏳ The first List component representing the tasks for today should have 2 or more items.

⏳ The second List component representing the tasks for tomorrow should have 3 or more items.

⏳ The List component should render the value from the tasks prop in the p tag.
~~~

## Código Solução
~~~
const List = (props) => {
  return <p>{props.tasks.join(', ')}</p>
};
class ToDo extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>To Do Lists</h1>
        <h2>Today</h2>
        <List tasks = {['Melao','Cocada']}/>
        <h2>Tomorrow</h2>
        <List tasks = {['Melao','Cocada','Lasanha']}/>
      </div>
    );
  }
};
~~~

# Item 16 - Use Default Props
## Contexto
>  React also has an option to set default props. You can assign default props to a component as a property on the component itself and React assigns the default prop if necessary. This allows you to specify what a prop value should be if no value is explicitly provided. For example, if you declare MyComponent.defaultProps = { location: 'San Francisco' }, you have defined a location prop that's set to the string San Francisco, unless you specify otherwise. React assigns default props if props are undefined, but if you pass null as the value for a prop, it will remain null. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/use-default-props

## Saida Esperada: 
~~~
⏳ The ShoppingCart component should render.

⏳ The ShoppingCart component should have a default prop of { items: 0 }.
~~~

## Código Solução
~~~
class MyComponent extends React.Component{
  constructor(props){
    super(props);
  }
  render(){
    return ( <ShoppingCart items={10} />)
  }
};
const ShoppingCart = (props) => {
 ShoppingCart.defaultProps = { items:0 }
  return (
    <div>
      <h1>Shopping Cart Component {props.items} </h1>
    </div>
  )
};
~~~

# Item 17 - Override Default Props
## Contexto
>  The ability to set default props is a useful feature in React. The way to override the default props is to explicitly set the prop values for a component [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/override-default-props

## Saida Esperada: 
~~~
⏳ The component ShoppingCart should render.

⏳ The component Items should render.

⏳ The Items component should have a prop of { quantity: 10 } passed from the ShoppingCart component.
~~~

## Código Solução
~~~
const Items = (props) => {
  return <h1>Current Quantity of Items in Cart: {props.quantity}</h1>
}
Items.defaultProps = {
  quantity: 0
}
class ShoppingCart extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <Items quantity={10} />
  }
};
~~~

# Item 18 - Use PropTypes to Define the Props You Expect
## Contexto
> Use PropTypes to Define the Props You Expect
> React provides useful type-checking features to verify that components receive props of the correct type. For example, your application makes an API call to retrieve data that you expect to be in an array, which is then passed to a component as a prop. You can set propTypes on your component to require the data to be of type array. This will throw a useful warning when the data is of any other type. [...]

###### Fonte: 

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

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/access-props-using-this-props

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

##### Fonte : https://www.freecodecamp.org/learn/front-end-libraries/react/pass-state-as-props-to-child-components

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
# Item 31 - pass-a-callback-as-props
## Contexto - 
> You can pass state as props to child components, but you're not limited to passing data. You can also pass handler functions or any method that's defined on a React component to a child component. This is how you allow child components to interact with their parent components. You pass methods to a child just like a regular prop. It's assigned a name and you have access to that method name under this.props in the child component. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/pass-a-callback-as-props

## Saída Esoerada
~~~
⏳ The MyApp component should render.

⏳ The GetInput component should render.

⏳ The RenderInput component should render.

⏳ The GetInput component should receive the MyApp state property inputValue as props and contain an input element which modifies MyApp state.

⏳ The RenderInput component should receive the MyApp state property inputValue as props.
~~~

## Código Solução
~~~
class MyApp extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      inputValue: ''
    }
    this.handleChange = this.handleChange.bind(this);
  }
  handleChange(event) {
    this.setState({
      inputValue: event.target.value
    });
  }
  render() {
    return (
       <div>
          <GetInput input = {this.state.inputValue} handleChange = {this.handleChange}/>
          <RenderInput input = {this.state.inputValue} />
       </div>
    );
  }
};

class GetInput extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h3>Get Input:</h3>
        <input
          value={this.props.input}
          onChange={this.props.handleChange}/>
      </div>
    );
  }
};

class RenderInput extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h3>Input Render:</h3>
        <p>{this.props.input}</p>
      </div>
    );
  }
};
~~~

# Item 32 - Use the Lifecycle Method componentWillMount
## Contexto - 
> React components have several special methods that provide opportunities to perform actions at specific points in the lifecycle of a component. These are called lifecycle methods, or lifecycle hooks, and allow you to catch components at certain points in time. This can be before they are rendered, before they update, before they receive props, before they unmount, and so on. Here is a list of some of the main lifecycle methods:  [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/use-the-lifecycle-method-componentwillmount

## Saída Esperada
~~~
⏳ MyComponent should render a div element.

⏳ console.log should be called in componentWillMount
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  componentWillMount() {
    console.log();
  }
  render() {
    return <div />
  }
};
~~~

# Item 33 - Use the Lifecycle Method componentDidMount
## Contexto  
> Most web developers, at some point, need to call an API endpoint to retrieve data. If you're working with React, it's important to know where to perform this action.[...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/use-the-lifecycle-method-componentdidmount

## Saída Esperada
~~~
⏳ MyComponent should render a div element which wraps an h1 tag.

⏳ Component state should be updated with a timeout function in componentDidMount.

⏳ The h1 tag should render the activeUsers value from MyComponent's state.
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      activeUsers: null
    };
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({
        activeUsers: 1273
      });
    }, 2500);
  }
  render() {
    return (
      <div>
        {/* Change code below this line */}
        <h1>Active Users: {this.state.activeUsers} </h1>
        {/* Change code above this line */}
      </div>
    );
  }
}
~~~

# Item 34 - Add Event Listeners
## Contexto  
> The componentDidMount() method is also the best place to attach any event listeners you need to add for specific functionality. React provides a synthetic event system which wraps the native event system present in browsers. This means that the synthetic event system behaves exactly the same regardless of the user's browser - even if the native events may behave differently between different browsers.  [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/add-event-listeners

## Saída Esperada
~~~
⏳ MyComponent should render a div element which wraps an h1 tag.

⏳ A keydown listener should be attached to the document in componentDidMount.

⏳ The keydown listener should be removed from the document in componentWillUnmount.

⏳ Once the component has mounted, pressing enter should update its state and the rendered h1 tag
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      message: ''
    };
    this.handleEnter = this.handleEnter.bind(this);
    this.handleKeyPress = this.handleKeyPress.bind(this);
  }
  // Change code below this line
  componentDidMount() {
      document.addEventListener('keydown', this.handleKeyPress);
  }
  componentWillUnmount() {
    document.removeEventListener('keydown', this.handleKeyPress);
  }
  handleEnter() {
    this.setState((state) => ({
      message: state.message + 'You pressed the enter key! '
    }));
  }
  handleKeyPress(event) {
    if (event.keyCode === 13) {
      this.handleEnter();
    }
  }
  render() {
    return (
      <div>
        <h1>{this.state.message}</h1>
      </div>
    );
  }
};
~~~

# Item 35 - Optimize Re-Renders with shouldComponentUpdate
## Contexto  
> So far, if any component receives new state or new props, it re-renders itself and all its children. This is usually okay. But React provides a lifecycle method you can call when child components receive new state or props, and declare specifically if the components should update or not. The method is shouldComponentUpdate(), and it takes nextProps and nextState as parameters. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/optimize-re-renders-with-shouldcomponentupdate

## Saída Esperada
~~~
⏳ The Controller component should render the OnlyEvens component as a child.

⏳ The shouldComponentUpdate method should be defined on the OnlyEvens component.

⏳ The OnlyEvens component should return an h1 tag which renders the value of this.props.value.

⏳ OnlyEvens should re-render only when nextProps.value is even.
~~~

## Código Solução
~~~
class OnlyEvens extends React.Component {
  constructor(props) {
    super(props);
  }
  shouldComponentUpdate(nextProps, nextState) {
    console.log('Should I update?');
    if (nextProps.value % 2 === 0){
      return true;
     }
    // Change code above this line
  }
  componentDidUpdate() {
    console.log('Component re-rendered.');
  }
  render() {
    return <h1>{this.props.value}</h1>;
  }
}

class Controller extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      value: 0
    };
    this.addValue = this.addValue.bind(this);
  }
  addValue() {
    this.setState(state => ({
      value: state.value + 1
    }));
  }
  render() {
    return (
      <div>
        <button onClick={this.addValue}>Add</button>
        <OnlyEvens value={this.state.value} />
      </div>
    );
  }
}
~~~
---

# Item 36 - Introducing Inline Styles
## Contexto  
> There are other complex concepts that add powerful capabilities to your React code. But you may be wondering about the more simple problem of how to style those JSX elements you create in React. You likely know that it won't be exactly the same as working with HTML because of the way you apply classes to JSX elements. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/introducing-inline-styles

## Saída Esperada
~~~
⏳ The component should render a div element.

⏳ The div element should have a color of red.

⏳ The div element should have a font size of 72px.
~~~

## Código Solução
~~~
class Colorful extends React.Component {
  render() {
    return (
      <div style={meuEstilo}>Big Red</div>
    );
  }
};
const meuEstilo = {
  color: "red",
  fontSize: "72px"
}
~~~
# Item 37 - Add Inline Styles in React
## Contexto 
> You may have noticed in the last challenge that there were several other syntax differences from HTML inline styles in addition to the style attribute set to a JavaScript object. First, the names of certain CSS style properties use camel case. For example, the last challenge set the size of the font with fontSize instead of font-size. Hyphenated words like font-size are invalid syntax for JavaScript object properties, so React uses camel case. As a rule, any hyphenated style properties are written using camel case in JSX. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/add-inline-styles-in-react

## Saída Esperada
~~~
⏳ The styles variable should be an object with three properties.

⏳ The styles variable should have a color property set to a value of purple.

⏳ The styles variable should have a fontSize property set to a value of 40.

⏳ The styles variable should have a border property set to a value of 2px solid purple.

⏳ The component should render a div element.

⏳ The div element should have its styles defined by the styles object.
~~~

## Código Solução
~~~
// Change code above this line
class Colorful extends React.Component {

  render() {
    return (
      <div style={styles}>Style Me!</div>
    );
    // Change code above this line
  }
};

const styles = {
  color: "purple", 
  fontSize: 40,
  border: "2px solid purple"
}
~~~

# Item 38 - Use Advanced JavaScript in React Render Method
## Contexto 
> In previous challenges, you learned how to inject JavaScript code into JSX code using curly braces, { }, for tasks like accessing props, passing props, accessing state, inserting comments into your code, and most recently, styling your components. These are all common use cases to put JavaScript in JSX, but they aren't the only way that you can utilize JavaScript code in your React components.  [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/use-advanced-javascript-in-react-render-method

## Saída Esperada
~~~
⏳ The MagicEightBall component should exist and should render to the page.

⏳ MagicEightBall's first child should be an input element.

⏳ MagicEightBall's third child should be a button element.

⏳ MagicEightBall's state should be initialized with a property of userInput and a property of randomIndex both set to a value of an empty string.

⏳ When MagicEightBall is first mounted to the DOM, it should return an empty p element.

⏳ When text is entered into the input element and the button is clicked, the MagicEightBall component should return a p element that contains a random element from the possibleAnswers array.
~~~

## Código Solução
~~~
const inputStyle = {
  width: 235,
  margin: 5
};

class MagicEightBall extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      userInput: '',
      randomIndex: ''
    };
    this.ask = this.ask.bind(this);
    this.handleChange = this.handleChange.bind(this);
  }
  ask() {
    if (this.state.userInput) {
      this.setState({
        randomIndex: Math.floor(Math.random() * 20),
        userInput: ''
      });
    }
  }
  handleChange(event) {
    this.setState({
      userInput: event.target.value
    });
  }
  render() {
    const possibleAnswers = [
      'It is certain',
      'It is decidedly so',
      'Without a doubt',
      'Yes, definitely',
      'You may rely on it',
      'As I see it, yes',
      'Outlook good',
      'Yes',
      'Signs point to yes',
      'Reply hazy try again',
      'Ask again later',
      'Better not tell you now',
      'Cannot predict now',
      'Concentrate and ask again',
      "Don't count on it",
      'My reply is no',
      'My sources say no',
      'Most likely',
      'Outlook not so good',
      'Very doubtful'
    ];
    const answer = possibleAnswers[this.state.randomIndex];
    return (
      <div>
        <input
          type='text'
          value={this.state.userInput}
          onChange={this.handleChange}
          style={inputStyle}
        />
        <br />
        <button onClick={this.ask}>Ask the Magic Eight Ball!</button>
        <br />
        <h3>Answer:</h3>
        <p>
          {answer}
        </p>
      </div>
    );
  }
}
~~~

# Item 39 - Render with an If-Else Condition
## Contexto 
> Another application of using JavaScript to control your rendered view is to tie the elements that are rendered to a condition. When the condition is true, one view renders. When it's false, it's a different view. You can do this with a standard if/else statement in the render() method of a React component.  [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/render-with-an-if-else-condition

## Saída Esperada
~~~
⏳ MyComponent should exist and render.

⏳ When display is set to true, a div, button, and h1 should render.

⏳ When display is set to false, only a div and button should render.

⏳ The render method should use an if/else statement to check the condition of this.state.display.
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      display: true
    }
    this.toggleDisplay = this.toggleDisplay.bind(this);
  }
  toggleDisplay() {
    this.setState((state) => ({
      display: !state.display
    }));
  }
  render() {
    const display = this.state.display
    if(display){
      return (
        <div>
          <button onClick={this.toggleDisplay}>Toggle Display</button>
          <h1>Displayed!</h1>
       </div>
      )
    }else{
      return (
        <div>
          <button onClick={this.toggleDisplay}>Toggle Display</button>
       </div>
      )
    }
  }
};
~~~

# Item 40 - Use && for a More Concise Conditional
## Contexto 
> The if/else statements worked in the last challenge, but there's a more concise way to achieve the same result. Imagine that you are tracking several conditions in a component and you want different elements to render depending on each of these conditions. If you write a lot of else if statements to return slightly different UIs, you may repeat code which leaves room for error. Instead, you can use the && logical operator to perform conditional logic in a more concise way. This is possible because you want to check if a condition is true, and if it is, return some markup. Here's an example:  [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/use--for-a-more-concise-conditional

## Saída Esperada
~~~
⏳ MyComponent should exist and render.

⏳ When display is set to true, a div, button, and h1 should render.

⏳ When display is set to false, only a div and button should render.

⏳ The render method should use the && logical operator to check the condition of this.state.display.
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      display: true
    }
    this.toggleDisplay = this.toggleDisplay.bind(this);
  }
  toggleDisplay() {
    this.setState(state => ({
      display: !state.display
    }));
  }
  render() {
    return (
       <div>
         <button onClick={this.toggleDisplay}>Toggle Display</button>
         {this.state.display && <h1>Displayed!</h1>}
       </div>
    );
  }
};
~~~
# Item 41 - Use a Ternary Expression for Conditional Rendering
## Contexto 
> Before moving on to dynamic rendering techniques, there's one last way to use built-in JavaScript conditionals to render what you want: the ternary operator. The ternary operator is often utilized as a shortcut for if/else statements in JavaScript. They're not quite as robust as traditional if/else statements, but they are very popular among React developers. One reason for this is because of how JSX is compiled, if/else statements can't be inserted directly into JSX code. You might have noticed this a couple challenges ago — when an if/else statement was required, it was always outside the return statement. Ternary expressions can be an excellent alternative if you want to implement conditional logic within your JSX. Recall that a ternary operator has three parts, but you can combine several ternary expressions together. Here's the basic syntax: [...]

###### Fonte:https://www.freecodecamp.org/learn/front-end-libraries/react/use-a-ternary-expression-for-conditional-rendering

## Saída Esperada
~~~
⏳ The CheckUserAge component should render with a single input element and a single button element.

⏳ The CheckUserAge component's state should be initialized with a property of userAge and a property of input, both set to a value of an empty string.

⏳ When the CheckUserAge component is first rendered to the DOM, the button's inner text should be Submit.

⏳ When a number of less than 18 is entered into the input element and the button is clicked, the button's inner text should read You Shall Not Pass.

⏳ When a number greater than or equal to 18 is entered into the input element and the button is clicked, the button's inner text should read You May Enter.

⏳ Once a number has been submitted, and the value of the input is once again changed, the button should return to reading Submit.

⏳ Your code should not contain any if/else statements.
~~~

## Código Solução
~~~
const inputStyle = {
  width: 235,
  margin: 5
};

class CheckUserAge extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: '',
      userAge: ''
    }
    this.submit = this.submit.bind(this);
    this.handleChange = this.handleChange.bind(this);
  }
  handleChange(e) {
    this.setState({
      input: e.target.value,
      userAge: ''
    });
  }
  submit() {
    this.setState(
      (state) => {return { userAge: state.input}}
    );
  }
  render() {
    const buttonOne = <button onClick={this.submit}>Submit</button>;
    const buttonTwo = <button>You May Enter</button>;
    const buttonThree = <button>You Shall Not Pass</button>;
    return (
        <div>
          <h3>Enter Your Age to Continue</h3>
          <input
            style={inputStyle}
            type='number'
            value={this.state.input}
            onChange={this.handleChange}
          />

          <br />
          {this.state.userAge >= 18 ? buttonTwo 
          :this.state.userAge === "" ? buttonOne : buttonThree}

        </div>
    )}
}
~~~

# Item 42 - render-conditionally-from-props
## Contexto 
> So far, you've seen how to use if/else, &&, and the ternary operator (condition ? expressionIfTrue : expressionIfFalse) to make conditional decisions about what to render and when. However, there's one important topic left to discuss that lets you combine any or all of these concepts with another powerful React feature: props. Using props to conditionally render code is very common with React developers — that is, they use the value of a given prop to automatically make decisions about what to render. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/use-a-ternary-expression-for-conditional-rendering

## Saída Esperada
~~~
⏳ The GameOfChance component should exist and render to the page.

⏳ GameOfChance should return a single button element.

⏳ GameOfChance should return a single instance of the Results component, which has a prop called fiftyFifty.

⏳ GameOfChance state should be initialized with a property of counter set to a value of 1.

⏳ When the GameOfChance component is first rendered to the DOM, a p element should be returned with the inner text of Turn: 1.

⏳ Each time the button is clicked, the counter state should be incremented by a value of 1, and a single p element should be rendered to the DOM that contains the text Turn: N, where N is the value of the counter state.

⏳ When the GameOfChance component is first mounted to the DOM and each time the button is clicked thereafter, a single h1 element should be returned that randomly renders either You Win! or You Lose!.
~~~

## Código Solução
~~~
class Results extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <h1>
          {this.props.fiftyFifty >= 0.5 ? 'You Win!' : 'You Lose!' }
      </h1>
    )
  }
}

class GameOfChance extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      counter: 1
    };
    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState(
      (state) => {return {counter: state.counter + 1}});
  }
  render() {
    const expression = Math.random() ; // retorna um valor aleatorio entre maior que zero e menor que 1
    return (
      <div>
        <button onClick={this.handleClick}>Play Again</button>
        <Results fiftyFifty={expression}/>
        <p>{'Turn: ' + this.state.counter}</p>
      </div>
    );
  }
}
~~~
# Item 43 - Change Inline CSS Conditionally Based on Component State
## Contexto 
> At this point, you've seen several applications of conditional rendering and the use of inline styles. Here's one more example that combines both of these topics. You can also render CSS conditionally based on the state of a React component. To do this, you check for a condition, and if that condition is met, you modify the styles object that's assigned to the JSX elements in the render method. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/change-inline-css-conditionally-based-on-component-state

## Saída Esperada
~~~
⏳ The GateKeeper component should render a div element.

⏳ The GateKeeper component should be initialized with a state key input set to an empty string.

⏳ The GateKeeper component should render an h3 tag and an input tag.

⏳ The input tag should initially have a style of 1px solid black for the border property.

⏳ The input tag should be styled with a border of 3px solid red if the input value in state is longer than 15 characters.
~~~

## Código Solução
~~~
class GateKeeper extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: ''
    };
    this.handleChange = this.handleChange.bind(this);
  }
  handleChange(event) {
    this.setState({ input: event.target.value })
  }
  render() {
    let inputStyle = {
      border: '1px solid black'
    };
    // Change code below this line
    if(this.state.input.length > 15){
      inputStyle = {
        border: '3px solid red'
      };
    }
    return (
      <div>
        <h3>Don't Type Too Much:</h3>
        <input
          type="text"
          style={inputStyle}
          value={this.state.input}
          onChange={this.handleChange} />
      </div>
    );
  }
};
~~~

# Item 44 - Use Array.map() to Dynamically Render Elements
## Contexto 
> Conditional rendering is useful, but you may need your components to render an unknown number of elements. Often in reactive programming, a programmer has no way to know what the state of an application is until runtime, because so much depends on a user's interaction with that program. Programmers need to write their code to correctly handle that unknown state ahead of time. Using Array.map() in React illustrates this concept. [...]

###### Fonte:https://www.freecodecamp.org/learn/front-end-libraries/react/use-array-map-to-dynamically-render-elements

## Saída Esperada
~~~
⏳ The MyToDoList component should exist and render to the page.

⏳ The first child of MyToDoList should be a textarea element.

⏳ The second child of MyToDoList should be a br element.

⏳ The third child of MyToDoList should be a button element.

⏳ The state of MyToDoList should be initialized with toDoList as an empty array.

⏳ The state of MyToDoList should be initialized with userInput as an empty string.

⏳ When the Create List button is clicked, the MyToDoList component should dynamically return an unordered list that contains a list item element for every item of a comma-separated list entered into the textarea element.
~~~

## Código Solução
~~~
const textAreaStyles = {
  width: 235,
  margin: 5
};

class MyToDoList extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      userInput: '',
      toDoList: []
    }
    this.handleSubmit = this.handleSubmit.bind(this);
    this.handleChange = this.handleChange.bind(this);
  }
  handleSubmit() {
    const itemsArray = this.state.userInput.split(',');
    this.setState({
      toDoList: itemsArray
    });
  }
  handleChange(e) {
    this.setState({
      userInput: e.target.value
    });
  }
  render() {
    const items = this.state.toDoList.map( 
      (element) => {return <li>{element}</li>}
    );  
    return (
      <div>
        <textarea
          onChange={this.handleChange}
          value={this.state.userInput}
          style={textAreaStyles}
          placeholder='Separate Items With Commas'
        />
        <br />
        <button onClick={this.handleSubmit}>Create List</button>
        <h1>My "To Do" List:</h1>
        <ul>{items}</ul>
      </div>
    );
  }
}
~~~

# Item 45 - Give Sibling Elements a Unique Key Attribute
## Contexto 
> The last challenge showed how the map method is used to dynamically render a number of elements based on user input. However, there was an important piece missing from that example. When you create an array of elements, each one needs a key attribute set to a unique value. React uses these keys to keep track of which items are added, changed, or removed. This helps make the re-rendering process more efficient when the list is modified in any way [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/give-sibling-elements-a-unique-key-attribute

## Saída Esperada
~~~
⏳ The Frameworks component should exist and render to the page.

⏳ Frameworks should render an h1 element.

⏳ Frameworks should render a ul element.

⏳ The ul tag should render 6 child li elements.

⏳ Each list item element should have a unique key attribute.

⏳ Each list item element should contain text from frontEndFrameworks.
~~~

## Código Solução
~~~
const frontEndFrameworks = [
  'React',
  'Angular',
  'Ember',
  'Knockout',
  'Backbone',
  'Vue'
];

class Frameworks extends React.Component{
  constructor(props){
    super(props)
  }
  render(){
    const renderFrameworks = frontEndFrameworks.map(
      (key) => {return <li key={key}>{key}</li>}
    );
    return (
      <div>
        <h1>Popular Front End JavaScript Frameworks</h1>
        <ul>{renderFrameworks}</ul>
      </div>
    );
  }
};
~~~

# Item 46 - Use Array.filter() to Dynamically Filter an Array
## Contexto 
> The map array method is a powerful tool that you will use often when working with React. Another method related to map is filter, which filters the contents of an array based on a condition, then returns a new array. For example, if you have an array of users that all have a property online which can be set to true or false, you can filter only those users that are online by writing: [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/use-array-filter-to-dynamically-filter-an-array

## Saída Esperada
~~~
⏳ MyComponent should exist and render to the page.

⏳ MyComponent's state should be initialized to an array of six users.

⏳ MyComponent should return a div, an h1, and then an unordered list containing li elements for every user whose online status is set to true.

⏳ MyComponent should render li elements that contain the username of each online user.

⏳ Each list item element should have a unique key attribute.
~~~

## Código Solução
~~~
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      users: [
        {
          username: 'Jeff',
          online: true
        },
        {
          username: 'Alan',
          online: false
        },
        {
          username: 'Mary',
          online: true
        },
        {
          username: 'Jim',
          online: false
        },
        {
          username: 'Sara',
          online: true
        },
        {
          username: 'Laura',
          online: true
        }
      ]
    }
  }
  render() {
    const usersOnline = this.state.users.filter(
      (user) => {return user.online === true}
    );
    const renderOnline = usersOnline.map(
      (user) =>  {return <li key={user.username}>{user.username}</li>}
    );
    return (
       <div>
         <h1>Current Online Users:</h1>
         <ul>
           {renderOnline}
         </ul>
       </div>
    );
  }
};
~~~

# Item 47 - Render React on the Server with renderToString
## Contexto 
> So far, you have been rendering React components on the client. Normally, this is what you will always do. However, there are some use cases where it makes sense to render a React component on the server. Since React is a JavaScript view library and you can run JavaScript on the server with Node, this is possible. In fact, React provides a renderToString() method you can use for this purpose. [...]

###### Fonte: https://www.freecodecamp.org/learn/front-end-libraries/react/render-react-on-the-server-with-rendertostring

## Saída Esperada
~~~
⏳ The App component should render to a string using ReactDOMServer.renderToString.
~~~

## Código Solução
~~~
class App extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <div/>
  }
};
ReactDOMServer.renderToString(<App />)
// Change code below this line
~~~
