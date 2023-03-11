**1. What is lexical environment?**
* It is the place where we can the access the values assigned in the parent when it is not present in local memory.
* Created whenever the execution context is created. It consists of both the local memory and the lexical environment of the parent.

**2. What is scope?**
* Where you can access a specific variables or functions. It is directly dependant on the lexical environment.

**3. What is lexical parent?**
* In the below example, function c() is lexically inside the function a() and a is lexically inside the global scope. 
* THE lexical parent of c is a. The lexical parent of function a() is global.

**4. What is scope chain?**
* Whole chain of lexical environment is scope chain.
```javascript
// Example for lexical environment, scope chain
function a(){
console.log(b); //checks whether b exists in the local memory, if it is not available it will search in the lexical environment of the parent(a) and even if it is not present, it will serach in the lexical environment of a(which is global)
function c(){
    console.log(b);
}
}
var b=10;
a();
c();
```
