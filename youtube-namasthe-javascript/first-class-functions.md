1. What is an anonymous funtion?
 Functions without name are called anonymous functions. It does not have their own identity.
// Anonymous function
function(){ // no name
    //throws error syntax error
}

2. What is the use of anonymous function?
It is used when the function are used as values. Anonymous function cannot be written in funtional statement but it can be written in functional expression.
// anonymous function used in the functional expression
let a = function (){
    //it works when a is called
}

3. What is named function expression?
let b= function a(){
    console.log(a); //can be used here
}
a(); // It will give a reference error that a is not defined
b(); // we can call

4. What are arguments and parameters?
function a(parameter){
    console.log(parameter);
}
a(arguments);

5. What is the difference b/w functional statement and functional expression?
Major difference is hoisting. when a function is called before the definition
For Functional statement - executes
For Functional expression - typeerror: It is not a function

//functional statement or function declaration
function x(){
    console.log("functional statement);
}
// Functional expression
let expression = function(){
    console.log("Functional Expression");
}

6. What are first class functions or first class citizens?
It is ability to use function as arguments and can be returned out of another funtions is called as first class functions.

function b(x){
    x();
}
function a(){
    return function xyz(){
        // this function will be returned
    }
}
b(a);

7. what are arrow function?
It is introduced in ES6.