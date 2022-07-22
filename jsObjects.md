# Objects
### Objects
- An object is a built-in data type for storing key-value pairs. Data inside objects are unordered, and the values can be of any type.
### Creating Object Literals:
- Use curly braces, { }, to designate an object literal
- We fill an object with unordered data. This data is organized into key-value pairs
- write the key’s name, or identifier, followed by a colon and then the value. We separate each key-value pair in an object literal with a comma (,).
```
let objectName { = {
  'Property Name': 'Property Value',
  propName: 'Prop Value'};
```
### Restrictions in Naming Properties
- JavaScript object key names must adhere to some restrictions to be valid. Key names must either be strings or valid identifiers or variable names (i.e. special characters such as - are not allowed in key names that are not strings).

### Accessing Properties
#### Dot Notation
- Dot Notation for Accessing Object Properties
- Properties of a JavaScript object can be accessed using the dot notation in this manner: object.propertyName. Nested properties of an object can be accessed by chaining key names in the correct order.
- Create a variable with a value of the object’s property:
`const variableName = objectName.propertyName;`

#### Accessing non-existent JavaScript properties
- When trying to access a JavaScript object property that has not been defined yet, the value of undefined will be returned by default.

#### Bracket Notation 
- Bracket Notation for Accessing Object Properties 
- To use bracket notation to access an object’s property, we pass in the property name (key) as a string.
> Note: use bracket notation when accessing keys that have numbers, spaces, or special characters in them. Without bracket notation in these situations, our code would throw an error.
`let variableName = objectName['propertyName']`

### Property Assignment 
- If the property already exists on the object, whatever value it held before will be replaced with the newly assigned value.
- If there was no property with that name, a new property will be added to the object.

### JavaScript Objects are Mutable
- JavaScript objects are mutable, meaning their contents can be changed, even when they are declared as const. New properties can be added, and existing property values can be changed or deleted.
- It is the reference to the object, bound to the variable, that cannot be changed.

### Delete operator
- Once an object is created in JavaScript, it is possible to remove properties from the object using the delete operator. The delete keyword deletes both the value of the property and the property itself from the object. The delete operator only works on properties, not on variables or functions

### JavaScript Object Methods
- JavaScript objects may have property values that are functions. These are referred to as object methods.
- Methods may be defined using anonymous arrow function expressions, or with shorthand method syntax.
- Object methods are invoked with the syntax: 
`objectName.methodName(arguments)`
```
let objectName = {
             methodName() {
                        console.log('The methodName method was invoked!')
              }
      };
```

### JavaScript for...in loop
- The JavaScript for...in loop can be used to iterate over the keys of an object. In each iteration, one of the properties from the object is assigned to the variable of that loop.

### Properties and values of a JavaScript object
- A JavaScript object literal is enclosed with curly braces {}. Values are mapped to keys in the object with a colon (:), and the key-value pairs are separated by commas. All the keys are unique, but values are not.
- Key-value pairs of an object are also referred to as properties.

### javascript passing objects as arguments
- When JavaScript objects are passed as arguments to functions or methods, they are passed by reference, not by value. This means that the object itself (not a copy) is accessible and mutable (can be changed) inside that function.

### JavaScript destructuring assignment shorthand syntax
- The JavaScript destructuring assignment is a shorthand syntax that allows object properties to be extracted into specific variable values.
- It uses a pair of curly braces ({}) with property names on the left-hand side of an assignment to extract values from objects. The number of variables can be less than the total properties of an object.

### shorthand property name syntax for object creation
- The shorthand property name syntax in JavaScript allows creating objects without explicitly specifying the property names (ie. explicitly declaring the value after the key). In this process, an object is created where the property names of that object match variables which already exist in that context. Shorthand property names populate an object with a key matching the identifier and a value matching the identifier’s value.

### `this` Keyword
- The reserved keyword this refers to a method’s calling object, and it can be used to access properties belonging to that object.
- Here, using the this keyword inside the object function to refer to the cat object and access its name property.

### javascript function this
- Every JavaScript function or method has a this context. For a function defined inside of an object, this will refer to that object itself. For a function defined outside of an object, this will refer to the global object (window in a browser, global in Node.js).

### JavaScript Arrow Function this Scope
- JavaScript arrow functions do not have their own this context, but use the this of the surrounding lexical context. Thus, they are generally a poor choice for writing object methods.

### getters and setters intercept property access
- JavaScript getter and setter methods are helpful in part because they offer a way to intercept property access and assignment, and allow for additional actions to be performed before these changes go into effect.
javascript factory functions
- A JavaScript function that returns an object is known as a factory function. Factory functions often accept parameters in order to customize the returned object.

### javascript getters and setters restricted
- JavaScript object properties are not private or protected. Since JavaScript objects are passed by reference, there is no way to fully prevent incorrect interactions with object properties.
- One way to implement more restricted interactions with object properties is to use getter and setter methods.
- Typically, the internal value is stored as a property with an identifier that matches the getter and setter method names, but begins with an underscore (_).