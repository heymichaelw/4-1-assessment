## Scope, hoisting and compartmentalization

### Answer the following:
In you own words, explain the concepts of scope, hoisting, compartmentalization.

Scope is the idea of how "visible" an aspect of a program is to the rest of the program.  If something is on the global scope, it is available to the entire program.  If something is in the local scope, it is only available within that function or block of code.  Hoisting is the principle of JavaScript that will move all variable and function declarations to the top of their scope, either to the top of the document or the top of the function.  This insures that all declarations occur before the function or variable is called.  Compartmentalization is the principle of JavaScript in that you only change or work with functions or variables within the block of code they affect.  For instance, you would only want to set the properties of an object within that object or a function dealing with the object, not in a totally different part of code.  

### Provide examples for all three, below:

#### Scope:

function printName(){

  var name = 'Michael';
  console.log(name);
}

console.log(name);

In this example, the second console.log() will print undefined, because the 'name' variable is defined within the scope of the function printName().  It is not available outside of this scope.

#### Hoisting:



#### Compartmentalization:
