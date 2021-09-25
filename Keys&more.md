#List and Keys

The example below uses a map() function (HHF) to take an 
array of numbers and double thier values. We assign the new array returned by map() to the variable doubled and log it.

const numbers = [1,2,3,4,5];
const doubled = numbers.map((number) => number * 2);
console.log(doubled);

this code logs [2,4,6,8,10] to the console

**This is how to do it with React**

## Rendering Multiple Components

you can build **COLLECTIONS** of elements and include them in JSX using curly braces {}.

const numbers=[1,2,3,4,5,6,7,8,9];
const listItems = numbers.map((number) => 
    <li>{numbers}</li>
);

above we have a const array of numbers.
we set another const which holds the map funciton to go through the array and create a list item for each of them.

We include the entire listItems array inside a <ul> element, and render it to the DOM:

ReactDOM.render(
  <ul>{listItems}</ul>,
  document.getElementById('root')
);

**A key is a special string attribute you need to include when creating lists of elements.**

*Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity!!*

const numbers = [1,2,3,4,5];
const listItems = numbers.map((number) => 
<li key={number.toString()}>
{number}
</li>
);

Most often, you would use IDs from your data as keys!!!
const todoItems = todos.map((todo) => <li key={todo.id}>
{todo.text}
</li>
);

RECAP:

1. What does .map() return?
*Map returns a new array that is produced from the expression inside of the function return!*

If I want to loop through an array and display each value in JSX, how do I do that in React?
EX.
const numbers = [1,2,3,4,5];
const items = numbers.map((number) => <h1>{numbers}</h1>);

Each list item needs a unique __Key__.

What is the purpose of a key?

*Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity!!*


The Spread Operator

**A spread operator is used to expand an iterable object into the list of argument**

**The spread syntax “spreads” the array into separate arguments**


Math.max(1,3,5) // 5
Math.max([1,3,5]) // NaN
use ... instead!!!
it sprads the array into seperate arguments. 



1.What is the spread operator?


List 4 things that the spread operator can do.
- The spread operator "spreads" the array into seperate arguments. 
- The spread operator can copy an array!
- The spread operator can concatenate or combinng arrays.
- The spread operator can add items to a list. 

Give an example of using the spread operator to combine two arrays.
const hello = {hello: "😋😛😜🤪😝"}
const world = {world: "🙂🙃😉😊😇🥰😍🤩!"}

const helloWorld = {...hello,...world}
console.log(helloWorld) // Object { hello: "😋😛😜🤪😝", world: "🙂🙃😉😊😇🥰😍🤩!" }

Above, we define to const variables with two seperate objects. The first object 'hello' has a value of emjois, as does 'world'. the two arrays are assign into another variable 'helloWorld' and the spread operator is used to put the two arrays together!

Give an example of using the spread operator to add a new item to an array.

const fruits = ['🍏','🍊','🍌','🍉','🍍']
const moreFruits = [...fruits];
console.log(moreFruits) // Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]
fruits[0] = '🍑'
console.log(...[...fruits,'...',...moreFruits]) //  🍑 🍊 🍌 🍉 🍍 ... 🍏 🍊 🍌 🍉 🍍

a variable 'fruits' is defined with 5 items in the array.
this array of fruits is assigned to a new variable called 'morefruits' with the spread operator in the beginning. '[...fruits];'
the variable fruits adds another item to the array and the end result is a copy of the previous array with a new fruit!



Give an example of using the spread operator to combine two objects into one.
const myArray = [`🤪`,`🐻`,`🎌`]
const yourArray = [`🙂`,`🤗`,`🤩`]
const ourArray = [...myArray,...yourArray]
console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩

in this example, we have two different arrays with different assigned variables. to combine them, we set another variable using our two array names and the spread operator. ['...myArray,...yourArray']


In the video, what is the first step that the developer does to pass functions between components?
He creates the mthod that will be used to set the state in the parent component!
In your own words, what does the increment function do?
the increment funciton goes through the array and matches the name passing in to the name in the specific data. if they match up the count stared at 0 adds by 1.
How can you pass a method from a parent component into a child component?
After the method is created, it is then added as an attribute to the child component called in the render method of the parent. The child can then access the method by using 'this.props.[insert method here].' 

How does the child component invoke a method that was passed to it from a parent component?
the child would call the method either in the render or inside of its own method(s) and the function would be called back up to the parent! 
