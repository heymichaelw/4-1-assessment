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

printName();

function printName(){

  var name = 'Michael';
  console.log(name);
}

In this example, the function printName() can be called at the top of the page because JavaScript hoists the declaration to the top of the page.  Because of this, once the program reaches "printName()", it is already defined.


#### Compartmentalization:

var firstnumber = 6;
var secondnumber = 4;

somePreviouslyDefinedFunction();
someOtherFunction();

function doMath(){
  var sum = firstnumber + secondnumber
  return sum;
}

This example does not follow compartmentalization, because the two variables are defined at the top of the program, before they're even used.  It would be better to declare the variables within the function, to reduce the likelihood they would be changed elsewhere.
