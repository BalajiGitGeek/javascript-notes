1. What happens in the javascript engine when the javascript code runs?
    Initially a Global execution context is created.


2. What is global execution context?
It consists of two components (Memory component and code component)
Execution context is Created in two phases
    1. Memory creation phase or creation phase
        Javscript skims through the whole program and allocate memory to every variables and functions. It stores a special value known as undefined in this phase for a variable but incase of functions it stores the whole code in the Memory component during the first phase. 
    2. Code execution phase
        Javascript runs through the whole program and executes the code again. In this phase, value is assigned to the variables.

3. Why is call stack?
For the control of the execution context.It will get empty after the whole javascript code is executed.
Global execution context will be in the bottom of call stack.

4. What is undefined?
Special keyword in javascript.

5. what happens to execution context when function is invoked?
whenever a function is invoked, a new execution context is created. Similarly, two phases happens(Memory creation phase and code execution phase)
Memory is allocated even to the parameters in the memory allocation phase. Calculations will be taken place inside the code component in the code execution phase.

6. What is arguments?
Values inside the paranthesis in the function call.

7. What is parameters?
Values inside the paranthesis in the function definition.

8. what happens when encouters the return keyword?
It return the value of the local memory of the execution context and the execution context will be deleted which was created during function invokation.

9. Various names for call stack?
program stack
machine stack
execution context stack
run time stack
Control stack.