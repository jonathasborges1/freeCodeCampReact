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
