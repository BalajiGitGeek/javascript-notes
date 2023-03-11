1. What is block or compound statement in javascript?
{} - block
Combining multiple statement to a group, so that we can use single statement where javascript expects one statement.

2. what is block scoped?
The variables and functions that can be accessed inside this block. let and const are block scoped. It folows the lexical scope. It is same for arrow functions.
{
    var a=10;// var will be in the global scope
    let b=10;//let and const will be in block scope
    const c=10;
}
//we cant access the b and c outside the block.

3. what is shadowing?
If we have same name variable outside the block then the shadowing occurs.It works the same way for arrow functions.
//Example
let/const b=100;
var a=100;
{
    var a=10;// it will shadow the value of a to 10 in global scope
    let/const b=10;
    const c=10;
    console.log(b); //10
}
console.log(a);// 10 will be print because of shadowing
console.log(b);// 100.

4. What is illegal shadowing?
we can't able to shadow the let assigned variable with var.This is called as illegal shadowing.
//Example 1
let a=20;
{
    var a =20;// illegal shadowing
    let a=100;// Able to shadow
}
//Example 2
var a =20;
{
    let a=100; //we can shadow
}