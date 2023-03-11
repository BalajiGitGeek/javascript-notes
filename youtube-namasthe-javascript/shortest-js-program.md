1. What is shortest javascript program?
Empty file.
Javascript engine will do lot of work behind the scenes.

2. What happens when empty file is run?
Global execution context is created and sets up the memory space.
Window object is created in global scope and it is created by the javascript engine. window object can be accessed by using this keyword.
At global level, this keyword will represents the window object.

3. Where javascipt code runs?
Javascript code runs in server,browser and various devices. WHerever it runs it need a javascript engine.
In chrome: V8 is the javascript engine and it is responsible to run the javascript code.

4. What is window?
It is a global object and it is created with global execution context.

5. what is global space?
Any variable assigned outside the function(At top level) will be in global space.

6. How can we access the variables in the global space?
we can access the variables in the global space without the window or this keyword.

// Example program
var a=10:
function b() {
    var x=10;
}
console.log(window.a);//all the below are same
console.log(a);
console.log(this.a);

console.log(x);//it will throw the error, since it is not in the global space.

