
var x = 1; // will be in the Global
a();
b();
console.log(x);
function a(){
    var x = 10; // Will be in the local
    console.log(x);
}
function b(){
    var x = 100;
    console.log(x);
}

Output:
10
100
1

what is Global and local inside the scope?
when the function is invoked a execution context is created, the value assigned inside that execution context is called local. the value in the global execution context will be named as global. 
