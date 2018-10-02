# Event Loop

How JavaScript execures asynchronous functions

call stack: a stack onto which calls are pushed when made and popped when executed

blowing the stack: infinite loop of stack placement

blocking: code that is slow, and thus blocks things from happening, like requests. not good in js cuz browsers b slow

webapi: hold onto timed tasks, shoves them into task queue when they're done. getput onto stack when stack is empty. where the nonjs code lives

set timeout for 0 will delayed something until the stack is clear

callback queue: where async tasks wait for the stack to clear before being executed when they come back from the webapi

setimetoutt not guarenteed, is a minimum. gets placed in queue when done.

rerendering has higher priority than callbacks

render queue: browser queue that gets blocked by the call stack. settimeout 0 allows rerendering to happen by making code wait

check out sprema



## Prototype

All objects have a protoype, determines what manner of object they are and what functionality they have.

object.prototype = other objects sets prototype

prototype is a regular property, while [[Prototype]] indicateds inhertience

object.contstructor = prototype

can add to prototype with object.prototype.x = stuff || object.prototype = {new stuff} to overwrite

f.prototype = { constructor: f }

obj2 = new obj.constructor() creates object from instance of object without knowing it's constructor, if constructor hasn't been modified.


## Closure

allows a function to access variables from an eclosing scope even after it leaves the scope where it was declared

lets a function act a lot more like a class without class syntax. returned functions can be called with object.function notation

function SpringfieldSchool() {
  let staff = ['Seymour Skinner', 'Edna Krabappel'];
  return {
    getStaff: function() { console.log(staff) },
    addStaff: function(name) { staff.push(name) }
  }
}

let elementary = SpringfieldSchool()
console.log(elementary)        // { getStaff: ƒ, addStaff: ƒ }
console.log(staff)             // ReferenceError: staff is not defined
/* Closure allows access to the staff variable */
elementary.getStaff()          // ["Seymour Skinner", "Edna Krabappel"]
elementary.addStaff('Otto Mann')
elementary.getStaff()  

doesn't work:

const arr = [10, 12, 15, 21];
for (var i = 0; i < arr.length; i++) {
  setTimeout(function() {
    console.log(`The value ${arr[i]} is at index: ${i}`);
  }, (i+1) * 1000);
}

works:

const arr = [10, 12, 15, 21];
for (let i = 0; i < arr.length; i++) {
  setTimeout(function() {
    console.log(`The value ${arr[i]} is at index: ${i}`);
  }, (i) * 1000);
}

### IIFE: immediately invoked functional expression

function called as it is defined.

//doesn't work
var result = [];
for (var i=0; i < 5; i++) {
  result.push( function() { return i } );
}
console.log( result[1]() ); // 5
console.log( result[3]() ); // 5

//works
result = [];
for (var i=0; i < 5; i++) {
  (function () {
    var j = i; // copy current value of i
    result.push( function() { return j } );
  })();
}


## Context

what this is

## Scope

what variables can be accessed
console.log( result[1]() ); // 1
console.log( result[3]() ); // 3
