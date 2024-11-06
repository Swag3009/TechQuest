# Basics
## Hoisting 
Hoisting is a Javascript mechanism where variables and function declarations are moved to the top of their scope befoer code execution.

## Let and Const 
**let :** 
1. It is block scoped.
2. Let can be updated but not re-declared. 
```js
// Updated
let name = "Swagatika";
name = "Swagatika Mohapatra";

//Re-declaration will throw error
let name = "Swagatika";
let name = "Swagatika Mohapatra";
```
3. Same variable can be declared in different blocks without throwing error, because both instances are treated as different variables due to their different scope. 
4. *let* declarations are hoisted to the top. 
5. Unlike *var*, the *let* keyword is not initialized. If we try to use it before initializing it, it will throw *Reference Error*. 
**cosnt :**
1. It is block scoped.
2. *const* declarations are hoisted to the top but are not initialized. 
3. It can not be updated or re-declared. Therefore it must be initialized at the time of declaration. 
4. *const* object can not be updated, but the properties of the objects can be updated. 
```js
const time = {
	min: 34,
	sec: 12
}
// Can't
time = {
	minutes: "thirty four",
	seconds: "five"
}
// Can 
time.min = "thirty four"
```
## Template Literal 
- Denoted with ``
- It allows multi line strings

```js
let text = 
`The quick
brown fox 
jumps over
the lazy dog.`
```
- It allows interpolate variables and expressions into string. *${}* is used to embed variable and expresion inside string. Within the placeholder it must be an expression, if you provide something like function delcaration, it will be stringified. 
```js
let name = `Swagatika`;
let fullName = `${name} Mohapatra`
```
#### Usage 
- *Generating HTML Markup* - It allows to embed Javascript expressions directly into HTML string, which makes it easy to create dynamic content.
- *Creating Dynamic SQL Queries* - It can be done by embedding variables or expressions directly into the query strings. You can create queries based on runtime value. 
- *Taged template literal* - A tagged template literal is a function call whose argument come from template literal. 
  - When the tag function gets called, the first argument it receives is an array of strings, which resulted from splitting the template literal on the interpolated parts. 
  - Each interpolated value is passed to the function as additional arguments, which can be accessed using rest parameter. 
```js
function tagfunc(string, ...substitution) {
  console.log(string);
  console.log(substitution);
}
let name = `Swagatika`;
let beverage = `Coffee`;
tagfunc`Hello ${name}! Would you like to have ${beverage}`;

//Output
/*
['Hello', '! Would you like to have', '']
['Swagatika', 'Coffee']
*/
```
## Function
Function is a block of code designed to perform a perticular task. Function is used for reusability, readability, easy testing, abstraction, collaboration, extensibility and modularisation. 
- In js, functions are first-class citizens, means they can be treated as values and passed around like any other variable.
- *Parameter* - Parameters are the references to values that will be used in a function. 
- *Arguments* - Arguments are the actual values passed to the functions when it is called in the programe. 
```js
function add(num1, num2){
	return num1+num2;
}
// here num1 and num2 are parameters
add(2, 3);
// here 2 and 3 are arguments
```

### Anonymous Function
Anonymous function is function that does not have a name. It is usually created for specific tasks and are often assigned to variables or used as arguments  for other functions. It is often used in situations where you don't need to reuse the function outside its immediate context. 
- Anonymous function is not accessible after it's initial creation. Therefore often you need to assign it to a variable. 
- () parantheses make the anonymous function an expression that returns a function object, without it, it will show syntax error. 
- It can be passed as arguments to other functions. 
- It can be stored in a variable and functions stored in variables do not need function names. They are always invoked (called) using the variable name. 
```js
// Anonymous function with function keyword
(function () {
	//statements
})
// Anonymous arrow function
() => {
	//statements
}
```
### Immediately Invoked Function Expression (IIFE)
It is a function that is called immediately after it is defined. It is used to create local scope for variables to prevent them from polluting the global scope. 
```js
(function () {
	//statement
})();
(()=>{
	//statement
})();
```
### Arrow function
It allows to write shorter function syntax.
- Arrow functions don't have their own binding to **this**, **argumens** or **super** and should not be used as **methods**. 
- Arrow functions cannot be used as contructors. Calling them with new throws TypeError. They also don't have access to the **new.target** keyword. 
- Arrow fucntions cannot use **yeild** within thier body and cannot be created as generator functions. 
```js
() => expression

param => expression

(param) => expression

(param1, paramN) => expression

(param1, paramN) => (expression)

//returning object 
(param1, paramN) => ({obj: 'obj'})

() => {
	statements
}

param => {
	statments
}

(param1, paramN) => {
	statements
}
```
- Rest parameters, default parameters, and destructureing within params are supported and alsways require parnetheses. 
```js
(a, b, ...r) => expression
(a = 400, b = 20, c) => expression
([a, b] = [10, 20]) => expression
({ a, b } = { a: 10, b: 20 }) => expression
```
- Arrow functions can be async by prefixing the expression with the async keyword. 
```js
async param => expression
async (param1, param2, ...paramN) => {
  statements
}
```
### 'this' in arrow function 
- Arrow functions do not bind their own this, instead they inherit the one from the parent scope, which is called "lexical scoping". 

### Higher Order Function
Higher order functions are fucntions that take one or more functions as arguments  or return a function as their result. 
#### map() 
- It takes an array of values and applies a tranformation to each value in the array. 
- It does not mutate the original array. 
- It creates a new array. 
```js
const arr = [1, 2, 3, 4, 5];
const output = arr.map((num) => num += 10)
console.log(arr); // [1, 2, 3, 4, 5]
console.log(output); // [11, 12, 13, 14, 15]
```
#### filter() 
- It takes an array and returns a new array with only the values that meet certain cirtera. 
- It does not mutate the original array.
- It select a subset of data from an array based on certain critera.
```js
const arr = [1, 2, 3, 4, 5];
const output = arr.filter((num) => num % 2) // filter out odd numbers
console.log(arr); // [1, 2, 3, 4, 5]
console.log(output); // [1, 3, 5]
```
#### reduce()
- This method iterate the array and reduces array's values into one value. 
- Accumulator parameter is the single value that will be returned by the method. 
- currentValue parameter is the item from the array which will change in each iteration.
- It iterates over each element in the array, and each iteration returns a single value, which is the accumulator. When the iteration is finished, the accumulator value will be returned from the method. 
- If we don't add the initial accumulator value explicitly, then the method will take the first item in the array as the initial accumulator value. 
- It is used for
  - Summarizing values into a single value
  - Grouping sililar items together
  - Removing duplicates from an array
```js
// Syntax
Array.reduce((accumulator, item, index, array) => {
  // TODO: Define the process for each iteration here
}, initialAccumulatorValue)
```
## Destructuring 
Destructureing assignment is a js expression that allows to upack values of array, properties of objects into distinct variable data.
### Object Destructuring
Object destructuing is the syntax for extracting values from an object prperty and assigning them to a variable. 
```js
const user = {
  first_name: "swagatika",
  last_name: "mohapatra",
};
const {
  first_name,
  last_name,
  full_name = `${first_name} ${last_name}`,
} = user;
```
#### Add Aliases
An alias name can be given to destructured variables.
```js
const user = {
  name: "Swagatika",
  address: "Forest Colony",
  age: 21,
};
const { address: permanentAddress } = user;
console.log(permanentAddress); // output -> Forest Colony
```
Attempt to access the varible address will result in error. 
#### Nested Object Destructuring 
The rule of thumb is to start with the top level and go down in the hierarchy until you reach the value you want to extract. 
```js 
const user = {
  name: "Alex",
  address: "15th Park Avenue",
  age: 43,
  department: {
    name: "Sales",
    Shift: "Morning",
    address: {
      city: "Bangalore",
      street: "7th Residency Rd",
      zip: 560001,
    },
  },
};
const {department: {address: {city}}} = user;
console.log(city); \\Output -> Bangalore
```
#### Dynamic Name Property
Many times we don't use the key name of an object while destructuring. 
```js
const user = {
  name: "Swagatika",
  address: "Forest Colony",
  age: 21,
};
getValue = (key) => {
  const { [key]: returnValue } = user;
  return returnValue;
};
console.log(getValue("name")); //Output -> Swagatika
```

#### Destructure to the Function Parameter
We use this when we don't need the entire object in a function but only some properties. Using destructure we don't need to pass the entire object and then extract the values from it one by one. 
```js
const user = { 
    'name': 'Alex',
    'address': '15th Park Avenue',
    'age': 43
}
function logDetails({name, age}) {
    console.log(`${name} is ${age} year(s) old!`)
}
logDetails(user);
```

#### Destructure Function return value
When an function returns and object but we need only specific property values, use destructuring.
```js
const getUser = () => {
    return{ 
        'name': 'Alex',
        'address': '15th Park Avenue',
        'age': 43
    }
}
const { name, age } = getUser();
console.log(name, age); 
```

#### Destructure in loops
Using for-of loop, object destructuring can be used. 
```js
const users = [
    { 
        'name': 'Alex',
        'address': '15th Park Avenue',
        'age': 43
    },
    { 
        'name': 'Bob',
        'address': 'Canada',
        'age': 53
    },
    { 
        'name': 'Carl',
        'address': 'Bangalore',
        'age': 26
    }
];
for(let { name, age } of users) {
    console.log(`${name} is ${age} years old!`);
}
```
#### Console Object
Console is a built-in object in js supported by all browsers. The properties of console can be used destructuring. 
```js
const { log, warn, error } = console;

log('I log into the browser console');
warn('I am a warning');
error('I am an error');
```
### Spread Operator
It takes an iterable and expands it into individual elements.
Objects can also be expanded and copy its enumerable properties to a new object.
With spread syntax we can clone, update, and merge objects in an immutable way. 

#### Create Clone of an Object
The spread syntax performs a shallow copy of the object. This means that none of the netsted object instances are cloned. 
```js
const user = { 
    'name': 'Alex',
    'address': '15th Park Avenue',
    'age': 43
}

const clone = {...user} // Output, {name: "Alex", address: "15th Park Avenue", age: 43}

clone === user; // Output, false
```

#### Add Properties to Objects
The new property gets added to the cloned object. 
```js
const user = { 
    'name': 'Alex',
    'address': '15th Park Avenue',
    'age': 43
}

// Add a new property salary
const updatedUser = {...user, salary:12345}; // {name: "Alex", address: "15th Park Avenue", age: 43, salary: 12345}

// Original object is unchanged
console.log(user); // {name: "Alex", address: "15th Park Avenue", age: 43}
```
#### Update Nested Objects
```js
const user = { 
    'name': 'Alex',
    'address': '15th Park Avenue',
    'age': 43,
    'department':{
        'name': 'Sales',
        'Shift': 'Morning',
        'address': {
            'city': 'Bangalore',
            'street': '7th Residency Rd',
            'zip': 560001
        }
    }
}
const updated = {
    ...user, 
    department: {
        ...user.department, 
        'number': 7
    }
};

console.log(updated);

```
#### Combine two Objects
Using spread syntax two objects can be merged together. This way of merging performs a shallow merge, means, if there is a common peoperty between both the objects, the property value of obj2 will replace the property value of obj1. 
```js
const merged = {...obj1,obj2}
```
### Rest Operator 
The rest operator is used to gather elements into an object. The rest parameter is mostly used with destructuring syntax to consolidate the remaining properties in a new object you're working with. 
```js

const user = { 
    'name': 'Alex',
    'address': '15th Park Avenue',
    'age': 43
}
const {age, ...rest} = user;
console.log(age, rest);
```
## Array
In javascript array is a specialtype of object used to group, store and organize multiple values under a single variable name, facilitating the management and manipulation of data collection. In javascript array can contain elements of any type, and it's length is not fixed. 
### Destructive Array Method
Destructive array methods alter the original arrays and return a modified array. 
- **pop()** -> Removes the last element of array.
```js
//syntax
array.pop();
```
- **push()** -> Add new element to the end of the array
```js
//syntax
array.push(element);
```
- **shift()** -> Removes the first element of an array and returns to shifted element
```js
//syntax
array.shift();
```
- **unshift()** -> Add new array to the element at the beginning of array.
```js
//syntax
array.unshift(element);
```
- **splice()** -> Adds or removes specific elements from an array at a specific index. When removing elements, it returns removed elements.
```js
//syntax
array.splice(index, howMany, element1, element2, ...., elementN);
// index - where you want to add or remove elements
// howMany - (Optional) number of elements to be removed
// elements - Elements that you want to insert
```

### Non-Destructive Array Methods
Non-destructive array methods in JavaScript return a new array or value without modifying the original array. When you want to preserve the original array while assigning the new output to a new array, you can use these non destructive array method.
- **concat()** -> Join 2 array and return the array
- **slice()** -> It takes specified elements from one array into a new one without changing the original. It takes 2 parameters, start and end position. By default start is 0th element and end is last element. 
- **filter()** -> Creates a new array with all elements that pass the test implemented by the provided function.
- **join()** -> Return an array as string.
```js
array.join(separator);
//separtor -> (optional) It takes the preferred separator as parameter
```
### Iterating Over array elements
- **includes()** -> Checks the array if specific element is present or not. It returns true or false value.
```js
array.inlcudes(value, start);
```
- **every()** -> It executes a function for each element of an array in the form of an evaluation. It returns true if all the array elements pass the evaluation and returns false, if at least one element fails the evaluation. It doesn't execute function for empty elements.
```js
array.every(callback);
```
```js
//example
let age = [22, 5, 75, 33, 90, 22];
age.every((age) => age < 50);
//else
function checkAge(age) {
  return age < 50;
}
age.every(checkAge);
```
- **some()** -> Returns true and stops execution of it passes the evaluation for one of the array elements. It will return false if all the elements fail the evaluation. 
```js
array.some(callback);
```
- **forEach** -> The forEach method is a built-in array method in JavaScript used to execute a provided function once for each array element. Unlike loops, it does not return a new array and doesn’t work with break or continue statements.

- **for...in** -> The for...of loop is used to iterate over each element in the array without needing to reference the index.

## Objects
- In js object helps to group values with similar characteristic together to make code more readable, organized and operable.
- An object is a data type that can take in collections of tkey value pairs.
Objects can store different types of datat as its values.
- The key of object is a string, if any other datatype is used as key, then it is converted into string. 
- There are 2 ways to access properties of object. One is *dot operation (.)* another is *bracket notation []*.
- If you want to use the value of variable as peoperty name of an object, you have to use bracket notation, can not use dot notation. 
- With multiword property name you can't use dot notation. 
### for..in loop
The for...in loop iterates over the enumerable properties (keys) of an object. It allows you to access each key in an object, which can then be used to get the corresponding value.

### Copy Object
Assigning object to other variable doen't copy object, it reference to memory. Means both original object and subsequent objects created by assigning the roginal object as a value are refercing the same iteem in the memory. 
```js
let user1 = {
	name: "Swagatika",
	age: 21
	}
let user2 = user1;
console.log(user1 === user2); //true
user2.age = 23;
console.log(user1.age); //23
```
Thats why spread or object.assign() is used to do shallow copy of an object.
```js
// spread operator
let obj1 = {...obj2};
// object.assign()
let obj = Object.assign(target_object, sourc_Object)
/*
target_object -> which takes the properties copied
source_object -> properties you want to copy
*/
``` 

### JavaScript Type Conversion

| **Type**                    | **Description**                                                                                          |
|-----------------------------|----------------------------------------------------------------------------------------------------------|
| **String Conversion**       | Use `String()` to convert various data types to strings.                                                 |
| **Number Conversion**       | Use `Number()` to convert strings to numbers. `parseInt()` and `parseFloat()` are also used for numbers. |
| **Boolean Conversion**      | Use `Boolean()` to convert values to booleans. `0`, `null`, `undefined`, `NaN`, `""` are `false`; all other values are `true`. |

### Examples of JavaScript Type Conversion

| **Conversion**               | **Example**                   | **Result**                     |
|------------------------------|-------------------------------|--------------------------------|
| **String Conversion**        | `String(123)`                 | `"123"`                        |
|                              | `String(false)`               | `"false"`                      |
| **Number Conversion**        | `Number("123")`               | `123`                          |
|                              | `Number(" 10 ")`              | `10`                           |
|                              | `Number("10.33")`             | `10.33`                        |
|                              | `Number("10,33")`             | `NaN`                          |
|                              | `Number("John")`              | `NaN`                          |
| **parseInt()**               | `parseInt("10")`              | `10`                           |
|                              | `parseInt("10.33")`           | `10`                           |
| **parseFloat()**             | `parseFloat("10.33")`         | `10.33`                        |
| **Boolean Conversion**       | `Boolean(0)`                  | `false`                        |
|                              | `Boolean(1)`                  | `true`                         |
|                              | `Boolean("")`                 | `false`                        |
|                              | `Boolean("Hello")`            | `true`                         |

### JavaScript Date Conversion and Methods

| **Method**                   | **Description**                                                              | **Example**                              | **Result** (based on example)                    |
|------------------------------|------------------------------------------------------------------------------|------------------------------------------|--------------------------------------------------|
| **Date Conversion**          | `Date()` converts a date to a string or creates a new Date object.           | `Date("2024-11-06")`                     | `"Wed Nov 06 2024 00:00:00 GMT+0000 (UTC)"`      |
| **getTime()**                | Returns the number of milliseconds since January 1, 1970.                    | `new Date().getTime()`                   | `1699190400000`                                  |
| **getDate()**                | Returns the day of the month (1-31) for a specified date.                    | `new Date().getDate()`                   | `6` (if today is the 6th)                        |
| **getDay()**                 | Returns the day of the week (0-6) for a specified date.                      | `new Date().getDay()`                    | `3` (if today is Wednesday)                      |
| **getFullYear()**            | Returns the full year (4 digits) of a specified date.                        | `new Date().getFullYear()`               | `2024`                                           |
| **getHours()**               | Returns the hour (0-23) of a specified date.                                 | `new Date().getHours()`                  | `14` (if current time is 2:00 PM)                |
| **getMilliseconds()**        | Returns the milliseconds (0-999) of a specified date.                        | `new Date().getMilliseconds()`           | `250` (if current millisecond is 250)            |
| **getMinutes()**             | Returns the minutes (0-59) of a specified date.                              | `new Date().getMinutes()`                | `30` (if current minute is 30)                   |
| **getMonth()**               | Returns the month (0-11) of a specified date.                                | `new Date().getMonth()`                  | `10` (November, since months are zero-based)     |
| **getSeconds()**             | Returns the seconds (0-59) of a specified date.                              | `new Date().getSeconds()`                | `45` (if current second is 45)                   |
| **toDateString()**           | Converts the date portion of a Date object to a readable string.             | `new Date().toDateString()`              | `"Wed Nov 06 2024"`                              |
| **toTimeString()**           | Converts the time portion of a Date object to a readable string.             | `new Date().toTimeString()`              | `"14:30:00 GMT+0000 (UTC)"`                      |
| **toLocaleDateString()**     | Returns a date as a string, formatted according to local conventions.        | `new Date().toLocaleDateString()`        | `"11/6/2024"` (format varies by locale)          |
| **toLocaleTimeString()**     | Returns the time as a string, formatted according to local conventions.      | `new Date().toLocaleTimeString()`        | `"2:30:00 PM"` (format varies by locale)         |
| **toISOString()**            | Returns a date as a string in simplified extended ISO format (UTC time).     | `new Date().toISOString()`               | `"2024-11-06T14:30:00.000Z"`                     |

### Notes

- **Date Format in JavaScript**: Months are **zero-based** (`0` is January, `11` is December).
- **Milliseconds**: `getTime()` is helpful for timestamps or for calculating date differences.
- **Locale-Specific Formats**: `toLocaleDateString()` and `toLocaleTimeString()` can be customized for specific locales.

## Closure
A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function.

### How Closures Work
1. When a function is created inside another function, it has access to the variables in the outer function's scope due to **lexical scoping**.
2. **Scope Chain**: In closures, JavaScript looks through the nested scope for variable values:
   - The inner function first checks its own scope.
   - If not found, it looks in the outer scope, continuing outward until it either finds the variable or throws a reference error.
3. The **lexical scope** means variables are accessed based on where functions are declared, not where they are called.
