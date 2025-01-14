React is a component-based platform.

The root of the hierarchy is the App component

        App
         |
        / \
Haading    Greeting

Each component must import React and at the root ReactDOM to use JSX.

The line of action is then 

ReactDOM.render(<App />, document.getElementAt("root"));

Import/Export

Using ES6 terminology, it is not required to use the Node 'require()'. 

    import React from 'react'

This statement will import the default-declared variable or method which is added at the end of the file. A default value does not need to have the same name as the variable which is exported, but if there are multiple exports, the names must match. Also these elements must be surrounded with {}.

    const pi = 3.141;

    function add(a,b) {
        return a+b;
    }

    export default pi;
    export {add};

TO import all functions use *. THIs can be prefixed with an alias.

Object destructuring is done with {}. E.g

    const {name, target} = event.target;

Array destucturing is done with [].

    const [name, setName] = useState();

Using an Object in state requires knowing the previous value of any To get the previous value, use prevValue and pass a funtion to the set function of the state.

Spread operator

- to merge arrays

const citrus = ['oranges', 'lemons', 'kiwis']
const fruits =['apples', 'bananas', 'apples', ...citrus];

