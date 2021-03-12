# TypeScript Intro

- Static types (set during developement)
```js
function funcName (<arg1>: <type>, <arg2>:<type>) {}

num1: number
name: string
isString: boolean
```
- Object:
```js
// optional object type declaration
const person: {
    name: string;
    age: number;
} = {
    name: "John",
    age: 25
}
```
- Adding (+) sign to a variable converts the variable into number:
```js
let result = +var1 + +var2
```
- Literal type
```js
type combinable = number | string; // type alias
function combine(
    input1: combinable, //number | string,
    input2: combinable //number | string,
    resultCobersion: 'as-number' | 'as-text' // literal type
 ) : combinable {
     if (typeof input1 === 'number' && typeof input2 === 'number' || resultConversion === 'as-number') {
         return +input1 + +input2;
     } else {
         return input1 + " " + input2;
     }
 }
```
- Function type
```js
function add(n1: number, n2: number): number {
    return +n1 + +n2;
}

function print(result: number): void {
    console.log('Result: ' + result);
}

let func: (a: number, b: number) => number //Function;
func = add;
//func = print //valid if func: Function

print(print(func(10,20)));
```
- tsc --int
    - Initialize the typescript configuration (tsconfig.json file will be created)
- include:
    - Include files which should be compiled from tsc to javascript
- exclude:
    - Exclude files which should not be compiled from tsc to javascript

# References
- https://www.youtube.com/watch?v=BwuLxPH8IDs