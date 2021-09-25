## Forms!!!

Controlled components..
In HTML, form elements such as < input >,
< textarea >, and < select > typically amntain thier own state and update it based on user input. In React mutable state is typically kept in the state property of components, and only updated with setState().

We can combine the two by making the React state be the 'single source of truth'. Then the React component that renders a form ALSO controls what happens in that form on subsequent user input. An input form element whoes value in controlled by React in this way is called a controlled component.

2. '< textarea >'
In HTML, a textarea tag element defines its text by its children. 
In React, a textarea uses a value attribute instead. 
HTML:
< textarea >
Hello there, this is some text in a text area 
< /textarea >

This way, a form using a textaarea can be written very similarly to a form that uses a single-line input:

REACT:

this.state = {
    value:'Please write an essay about your favorite DOM element'
};

this will be in the text field box to start out!
< textaarea value= {this.state.value}>

================================================================
3. the select tag

this.state = {value: 'coconut'};

< select value={this.state.value}>
....

These elements in React make it so that they all accept a value attribute that you can use to implement a controlled component!


## What is a ‘Controlled Component’?

An input form whose value is controlled by the React state. We can pass the value to other UI elements or reset it from other event handlers

Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
We should update the state with thier responses as soon as they enter them. It is possible to do so with react and make it accessible to the user to change.

How do we target what the user is entering if we have an event handler on an input field?

We can use 'event.target.value' to retrieve the value of whatever input in called on, or your input's element. 

## The Ternary Operator!!


Consider the following code: ``if (person.age >= 16) {
  `` person.driver = 'Yes';
} else {
  person.driver = 'No';
} ``


**We can rewrite it to this**:

person.driver = person.age >=16 ? 'yes' : 'no';

if( condition ) {
    value if true
} else {
    value if false
}

condition ? value if true : value if false

The condition is what you are actually testing. the result of your condiiton should be true or false or at least coerce to either boolean value.

2. A ? seperates our conditional from our *TRUE* value. Anything between the ? and the : is what is executd if the condition is true.

3. Finally, a : colon. If your condition is false, any code AFTER THE COLON is executed.

We can test ternary operators to test multiple conditions!

let isStudent = false;
let isSenior = true;

let price = isStudent ? 8 : isSenior ? 6 : 10;

Why would we use a ternary operator?
It lessens the amount of Code we need to write!

Rewrite the following statement using a ternary statement:
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }

  let equals = x===y ? 'true' : 'false';

Happy Coding!!