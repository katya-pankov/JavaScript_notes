# Converting Functions to Arrow Functions
1. Named functions with two parameters
2. Named functions with one parameter
3. Named functions with no parameters
4. Anonymous functions with no name

**Arrow** function is a newer way to write traditional function
## Named functions with two parameters 
```javascript
function sum(a, b) {
    return a + b;
}
```
First thing we need to do is to remove the function keyword.
Then create a variable to store the function and use const to declare it.
Lastly, after the parameter list and before the { place an =>
```javascript
const sum2 = (a, b) => {
    return a + b;
}
// Alternative syntax (works only if you only have one line of code within curly braces)
const sum2 = (a, b) => a + b;
```

## Named functions with one parameter
```javascript
function isPositive(number) {
    return number >= 0;
}
```
To convert this function to an arrow function, we need to:
- Remove the **function** keyword
- Create a variable to store the function and use **const** to declare it
- After the parameter list and before the { place an =>
- If there is only one statement which is a return, you can drop the {}'s
```javascript
const isPositive2 = (number) => {
    return number >= 0;
}

// or
const isPositive2 = (number) => number >= 0;

// since we only have one parameter, we can remove the ()'s around the parameter
const isPositive2 = number => number >= 0;
```

## Named functions with no parameters
```javascript
function randomNumber() {
    return Math.random();
}
```

To convert to an arrow function, you need to:
- Remove the **function** keyword
- Create a variable to store the function and use **const** to declare it
- Leave the ()  and before the { place an =>
```javascript
const randomNumber = () => {
    return Math.random();
}
// or
const randomNumber = () => Math.random();
```
## Anonymous functions 

**Anonymous functions** are functions without a name. It is also known as a function expression.  An anonymous function is not accessible after its initial creation. Therefore, you often need to assign it to a variable.

```javascript
document.addEventListener('click', function () {
    console.log('Clicked!');
});
```
Converted result 
```javascript
document.addEventListener('click', () => {console.log('Clicked!');
});
// Alternative syntax (only if you have on statement)
document.addEventListener('click', () => console.log('Clicked!')) ;
```

