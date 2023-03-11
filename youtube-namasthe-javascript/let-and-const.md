**1. Is let and const are hoisted?**
* Yes.But it will be in temporal dead zone for time being. It will be hoisted but not in the same way as var keyword.

**2. What is temporal dead zone?(only for let and const)**
* It is the timeperiod of the undefined variable and the initialization of that variable. when we access a varible which is in temporal dead zone, it gives the reference error(cannot access a before the initialization).
* But Incase of var, gives undefined as value.

**3. What is reference error?**
* When there is no reference of the variable.
```javascript
// Example 1
console.log(a);//cannot access a before the initialization(not for var)
let a=100;
```
```javascript
// Example 2
console.log(y); //not defined
```

**4. What is syntax error?** (will not run one single line also)
* when let a=10; is assigned again, syntax error throws.
* In var: It is possible to assign again.
* In const: redeclaration cant be done(missing initializer in const declaration)
```javascript
// Example 1
const a;// missing initializer in const declaration
```
```javascript
// Example 2
let a=100;
let a=1000;// already been declared
```

**5. what is type error error?**
```javascript
// Example
const a=100; 
a=1000; // Type Error: Assignment to constant variable.
```

**6. Diff b/w const vs let vs var?**
* const>let>var (strict)
* let - temporal dead zone, redeclaration is not possible.
* const - Only able to intialize at the first time.

**7. What is script?**
* Hoisting of let and const happens in this place.
```javascript
//Example (a will be not attached to the window object.But b will be attached to the window object)
console.log(a); //throws error:cannot access a before the initialization- it will be in the script memory space
console.log(b);// undefined
let a=10; 
var b=100;
```



