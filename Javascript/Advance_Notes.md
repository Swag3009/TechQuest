# Advance 
- JavaScript functions are executed in the sequence they are called. Not in the sequence they are defined. 
- JavaScript runs on a single threaded environment, by default instructions run synchronously, Meaning it can only execute one command at a time. 
## Callback Functions 
A callback function is a function that is passed as an argument to another functon and is exectued after the completion of some operations. 

### Callback hell
Callback hell refers to an ineffective way of writing code asynchronously. Callback hell refers to the situation in Javascript where multiple nested callbacks create complex, deeply indented code, often called the "pyramid of doom". This structure makes the code difficult to read, debug, and maintain, resulting in poor code quality and scalability issues. 

# OOP
Javascript is a **prototype-based procedural language** which follows both Object Oriented Programming and Functional Programming. Everything we define in Javascript is an object that extends the functionality from the prototype object. Hence, Javascript is a prototype-based language. 
Even though JavaScript doesn't have classes in it, it does have support for the **class** keyword. The **class** keyword is just a syntactic sugar over the prototype-based inheritence. 

OOP is a programming paradigm that believes in grouping data(properties) and methods(actions) together inside a box. It demonstates the pattern of real-world objects. 

## Object-Oriented Programming vs Prototype-based Programming
**OOP** -> The object-oriented paradigm keeps data and actions grouped together inside classes. In OOP, we create classes and create their instances called objects. 
**Prototype-based Programming** -> In this, we derive objects from other already existing objects. 

## Javascript OOP behaviours 
### Inheritence 
Objects inherit properties from parent objects or any other objects using the concept of prototypal inheritence. 
### Polymorphism 
Polymorphism is an concept in OOP that enables us to use the same function in different forms, which reduces repetition and makes the code snippet useful in many different cases. In JavaScript it is implemented by 
	1. Generic
	2. Overloading
	3. Structural sub-typing
#### Generic (Parametric Polymorphism)
Generic overloading allows the same function or method to handle different data types or different numbers of arguments. 

```js
const concatData = (x,y) => {
    return y.concat(x);
}
console.log(concatData([1,2],[3,4])); //[3, 4, 1, 2]
console.log(concatData("John","Smith")); //'SmithJohn'
```

#### Overloading (ad-hoc polymorphism)
Functions created using ad-hoc polymorphism exhibit different behaviors based on different types of input values. 

```js
//when used on integers and floats, exhibit the property of addition
console.log(4 + 5) //9

//when used with strings and array does concatenation.
console.log("My name is: "+"John Smith") //My name is John Smith.
```

#### Structural Subtyping (Structural Polymorphism / Duck Typing) 
Structural subtyping is a type system paradigm where type compatibility is determined based on the structure of the types (i.e., the properties and methods an object has) rather than explicit declarations or inheritance. It is also informally referred to as duck typing: "If it looks like a duck and quacks like a duck, it's treated as a duck."
In the context of programming, this means that if an object has the properties and methods expected by some piece of code, it can be used in that context, regardless of its actual type or inheritance.
JavaScript inherently supports structural subtyping because it is a dynamically typed language. Objects in JavaScript are defined by their properties and methods, not by their declared types or inheritance trees.

```js
function printDetails(entity) {
    if (entity.name && entity.age) {
        console.log(`Name: ${entity.name}, Age: ${entity.age}`);
    } else {
        console.log("Invalid structure");
    }
}

const person = { name: "Alice", age: 25 };
const dog = { name: "Buddy", age: 5, breed: "Golden Retriever" };

printDetails(person); // Output: Name: Alice, Age: 25
printDetails(dog); // Output: Name: Buddy, Age: 5

/*
The printDetails function only cares if the object has name and age properties. Any object with this structure is compatible.

The dog object works, even though it has additional properties like breed.
*/
```

### Relation Between Ojects 
JavaScript objects support Association, Aggregation and Composition
#### Association 
When two objects are unrelated and independent of each other, we define a relationship between them independent of any hierarchy. This means none of the objects is the child or parent of the other object, and the relation is called an association.

**For example:** In the case of a patient visiting a doctor, there is an independent relation. That doctor might be seeing multiple patients, and that patient can also be visiting multiple doctors simultaneously. None of them is a parent or a child. Hence, the relation is built through association.

#### Aggregation 
There is an ownership in this type of relationship. It holds a parent/child relation. An essential property of this type of relationship is that the parent can live without the child object and vice versa. The child can also exist independently.

**For example:** If an employee works for more than one department in a company, and anyone department gets deleted, the child, i.e., the employee, can still exist inside the company. Hence, this relationship exhibits aggregation.

#### Compostion 
Composition is a special type of aggregation. If the parent object dies, the child object also ceases to exist. To be more precise, the parent can exist without the child object, but vice versa is not true. The child cannot exist without its parent object.

# Prototype 
Prototypes are the mechanism by which JavaScript objects inherit features from one another. 
## Prototype Chain
Every object in JavaScript has a built-in property, which is called its prototype. The prototype is itself an object, so the prototype will have its own prototype, making what's called a prototype chain. The chain ends when we read a prototype that has null for its own prototype. 
