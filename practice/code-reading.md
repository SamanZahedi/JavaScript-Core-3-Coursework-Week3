# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.
The variable x defined in line is in the global scope and accessible throughout, whereas variable x defined in line 3 is in local scope and limited to the function.

## Question 2

Take a look at the following code:

```
let x = 10

function f1()
{
    console.log(x)
    let y = 20
}

console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less.
Line 32 will output 10 and line 33 will return undefined as variable y is not accessible outside the function and scoped to it.

## Question 3

Take a look at the following code:

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}

f1(x);
console.log(x);

const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y);
```

What will be the output of this code. Explain your answer in 50 words or less.
The variable x defined in line 43 will not change as any changes in the f1 function is scoped to it.
The variable y logged in line 62 will change to 10 as when we define an object and use it in a function, it changes the original defined value as it is passes as a reference to the function.
