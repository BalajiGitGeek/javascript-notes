1. why undefined is assigned?
It is meant to know whether the memory is allocated or not.

2. what is undefined?
If the value is not present at that point of execution, it will be undefined.

3. What is ===?
Checks whether it is strictly equal.

4. Why javascript is loosely typed language?
It will not attach variable to the specific datatype. Datatype can be changed, hence it is loosely typed language.

//Example for loosely typed language
var a;
console.log(a);
a=10;
console.log(a);
a="hi balaji";
console.log(a);

//Example for undefined or not defined.
var a;
console.log(a);
if(a === undefined){
    console.log("a is undefined);
}
else{
    console.log("a is not defined);
}

