
**1. What is a garbage collector?**
* It is a program in the browser/javascript engine free up and utilize the memory. whenever there is unused variables, it will be garbage collected.
```javascript 
funtion a(){
    var a=0,z=1; // a will not garbage collected but z will be garbage collected by browser/javascript engine smartly.
    return function b(){
        console.log(a);
    }
}
a();
```

**2. Disadvantages of closure?**
* Overconsumption of memory
* The variable are not garbage collected.

**3. How are garbage collector and closures are related to each other?**
```javascript
funtion a(){
    var a=0; // this will not garbage collected.
    return function b(){
        console.log(a);
    }
}
a();
```

**4. What is double paranthesis?**
```javascript
function outer(b){
    function inner(){
        console.log(a,b);
    }
    var a=10; 
    retun inner;
}
outer("hello closure")();
```
```bash
Output:
10
hello closure
```

**5. What will be output when the above function is nested inside other funtion?**
* Behaves the same way as the closure
```javascript
function outest(){
    function outer(b){
        function inner(){
            console.log(a,b);
        }
        var a=10; 
        retun inner;
    }
    return outer;
}
let a=100; // if the a does not exists in the block scope, then it will print
outest()("hello closure")();
```
```bash
Output:
10 hello closure
```
**6. Advantages of closures?**
* function currying
* data hiding

**7. what is data hiding?**
* Hiding of data, so that other functions can't access it.
```javascript
//example
function counter(){
    var count=0;
    return function incrementCounter(){
    count++;
    }
}
var counter1= counter();
counter1();
counter1();
var counter2= counter();// it gives a new counter.
counter2();
```
**8. Is the above code scalable?**
* It is not a good way. We can use *constructor* function.
* // Example of a constructor function
```javascript
function Counter(){
    var count=0;
    this.incrementCounter = function incrementCounter(){
        count++;
        console.log(count);
    }
    this.decrementCounter = function decrementCounter(){
        count--;
        console.log(count);
    }
}
var count = new Counter();//*new* keyword is used for constructor and naming convention is *Pascal*
count.incrementCounter();
count.decrementCounter();
```
```bash
Output:
1
0
```




