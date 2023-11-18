```
Program => allocates memory and parses and execute scripts (read/write commands)
Browser => JS engine => has memory heap and call stack

const a = 1;
const b = 2;

-> those variables are located within the memory heap;

Memory leak => unused memory present in memory heap that fills up storage;

call stack => reads and executes the script; reads a var, pops it, next var, etc.

const one = () => {
  const two = () => {
    console.log('4');
  }
  two();
}

Call Stack: FIFO
console.log('4')
two(); 
one();

remove top of stack by popping it after its read, then to next fxn and repeat

Synchronous => in order sequence; basically what the call stack is

stack overflow => call stack is bigger than its container

function foo() {
  foo()
}

foo()

recursion => keeps calling foo() without a base case to stop it; this is a example of stack overflow.

JS is single threaded!
```


