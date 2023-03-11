**1. What is closures?**
* It is a function bind together with the lexical scope.
```javascript
// Example
function x(){
    var a=7;
    function y(){
        console.log(a);
    }
    y();
}
x();
```
```bash
Output:
7
```

**2. What happens when we pass a function inside a function and when we return the function?**
* Closure happens.
```javascript
//Example
function x(){
    var a=10;
    function y(){
        console.log(a);
    }
    <!-- a=100 -->In this case output will be 100
    return y; // or it can be written as *return function y()* on line 
}
var z= x(); //closure will be returned, function along with the lexical scope, So a can be accessed.
z(); // Closure comes into existence, it will remember the a
```
```bash
Output:
10
```

```javascript
//example 2
function z(){
    var b=100;
    function x(){
    var a=10;
    return function y(){
        console.log(a,b);
    }
}
}
var c=z();
c();
```
```bash
Output:
10
100
```

**3. Uses of closures?**
* Module design pattern
* Currying in javascript
* function like once
* memoize
* maintaining state in async world
* setTimeOut() is a closure

**4. What happens in the setTimeOut function?**
```javascript
// Example
function x(){
    var i=1;
    setTimeOut(function(){ 
        console.log(i); //This function forms a closure with the reference(i)
    },3000);
    console.log("Javascript will not wait");
}
```
```bash
Output:
Javascript will not wait
1
```

**5. What will be output of the below code?**
```javascript
// Example with var
function x(){
    for(var i = 0; i <= 5;i++){
        setTimeOut(function(){ 
        console.log(i); //This function forms a closure with the reference(i)
        },i*1000);
    }
    console.log("closures");
}
x();
```
```bash
Output:
closures
6
6
6
6
6
6
```

**6. Output of below code?**
```javascript
// Example with let
Since it is block scoped
function x(){
    for(let i = 0; i <= 5;i++){
        setTimeOut(function(){ 
        console.log(i); //This function forms a closure with the reference(i)
        },i*1000);
    }
    console.log("closures");
}
x();
```
```bash
Output:
closures
1
2
3
4
5
```

**7. Output of below code?**
```javascript
//Only using var
function x(){
    for(var i = 1; i <= 5;i++){
        function closure(x){
            setTimeOut(function(){ 
            console.log(x); //This function forms a closure with the reference(i)
            },i*1000);
        }        
        closure(i);
    }
}
x();
```
```bash
Output:
1
2
3
4
5
```
