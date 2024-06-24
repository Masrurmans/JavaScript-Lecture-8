# Object in JavaScript
### What is Object in JavaScript ?
An object is a collection of properties, and a property is an association between a name (or key) and a value. A property's value can be a function, in which case the property is known as a method. Objects in JavaScript, just as in many other programming languages, can be compared to objects in real life.
### Create Object ↴
![image](https://github.com/Masrurmans/JavaScript-Lecture-8/assets/171729580/4d6a490d-2b07-4043-a7d0-d71885a121bb)
### Methods Obect
#### Method ```Object.entries()```
entries() method is used to return an array consisting of enumerable property [key, value] pairs of the object which are passed as the parameter. The ordering of the properties is the same as that given by looping over the property values of the object manually.
```````js
const obj = { a: 1, b: 2, c: 3 };

const entries = Object.entries(obj);
console.log(entries);
// Output: [ [ 'a', 1 ], [ 'b', 2 ], [ 'c', 3 ] ]

// Iterating over the entries
entries.forEach(([key, value]) => {
  console.log(`${key} -> ${value}`);
});
// Output:
// a -> 1
// b -> 2
// c -> 3
`````````
#### Method ```Object.keys()```
Object.keys() returns an array whose elements are strings corresponding to the enumerable string-keyed property names found directly upon object . This is the same as iterating with a for...in loop, except that a for...in loop enumerates properties in the prototype chain as well.
``````js
const obj = { a: 1, b: 2, c: 3 };

const keys = Object.keys(obj);
console.log(keys);
// Output: [ 'a', 'b', 'c' ]

// Iterating over the keys
keys.forEach(key => {
  console.log(`${key} -> ${obj[key]}`);
});
// Output:
// a -> 1
// b -> 2
// c -> 3
````````
#### Method ```Object.values()```
The Object.values() static method returns an array of a given object's own enumerable string-keyed property values.
````````js
const obj = { a: 1, b: 2, c: 3 };

const values = Object.values(obj);
console.log(values);
// Output: [ 1, 2, 3 ]

// Iterating over the values
values.forEach(value => {
  console.log(value);
});
// Output:
// 1
// 2
// 3
````````

# Destructuring & Spread in JavaScript (Object)
### What is Destructuring & Spread in JavaScript (Object) ?
Destructuring is used to create varibles from array items or object properties. Spread syntax is used to unpack iterables such as arrays, objects, and function calls.
#### Destructuring example:
````````js
// Destructuring an object
const person = {
  firstName: 'John',
  lastName: 'Doe',
  age: 30,
  city: 'New York'
};
const { firstName, lastName, ...details } = person;

console.log(firstName); // Output: John
console.log(lastName); // Output: Doe
console.log(details); // Output: { age: 30, city: 'New York' }
`````````
#### Spread example:
`````````js
// Spread in object
const obj1 = { foo: 'bar', x: 42 };
const obj2 = { ...obj1, y: 10 };

console.log(obj2); // Output: { foo: 'bar', x: 42, y: 10 }
`````````
# ```this``` keyword in JavaScript (Object)
### What is ```this``` keyword in JavaScript (Object) ?
The this keyword refers to the context where a piece of code, such as a function's body, is supposed to run. Most typically, it is used in object methods, where this refers to the object that the method is attached to, thus allowing the same method to be reused on different objects.
```````js
// Define an object
const person = {
  firstName: 'John',
  lastName: 'Doe',
  fullName() {
    // 'this' refers to the 'person' object
    return `${this.firstName} ${this.lastName}`;
  }
};

// Accessing object properties
console.log(person.fullName()); // Output: John Doe
````````

