# Javascript मध्ये हे 15 functions आलेच पाहीजेत.

## JavaScript Array forEach()

<details><summary><b>Answer</b></summary>

The forEach() method calls a function for each element in an array.example:

```javascript
const phones = [
  {brand : 'Apple' , price : 1000},
  {brand : 'Samsung' , price : 800},
  {brand : 'OnePlus' , price : 400},
  {brand : 'LG' , price : 1200},
  {brand : 'Xiami' , price : 300},
  {brand : 'Realme' , price : 600},
  {brand : 'Nokia' , price : 1500}
 ];

  const phonesArray = phones.forEach((phone) => {
      
     console.log(`phone.brand phone.price `)
  
  });
console.log(phonesArray)

 // style 2
 phones.forEach((element, index) => { console.log(element) })
 ``` 
</details>

## Question 4. What is “closure” in javascript? Can you provide an example?

<details><summary><b>Answer</b></summary>

A closure is a function defined inside another function (called parent function) and as such it has access to the variables declared and defined within its parent function's scope.

The closure has access to the variables in three scopes:

- Variable declared in its own scope
- Variable declared in its parent function's scope
- Variable declared in the global namespace

```javascript
var globalVar = "abc"; //Global variable

// Parent self-invoking function
(function outerFunction (outerArg) { // start of outerFunction's scope

  var outerFuncVar = 'x'; // Variable declared in outerFunction's function scope   
  
  // Closure self-invoking function
  (function innerFunction (innerArg) { // start of innerFunction's scope

    var innerFuncVar = "y"; // variable declared in innerFunction's function scope
    console.log(         
      "outerArg = " + outerArg + "\n" +
      "outerFuncVar = " + outerFuncVar + "\n" +
      "innerArg = " + innerArg + "\n" +
      "innerFuncVar = " + innerFuncVar + "\n" +
      "globalVar = " + globalVar);
  	
  // end of innerFunction's scope
  
  })(5); // Pass 5 as parameter to our Closure

// end of outerFunction's scope

})(7); // Pass 7 as parameter to the Parent function
```

`innerFunction` is a closure which is defined inside `outerFunction` and consequently has access to all the variables which have been declared and defined within `outerFunction`'s scope as well as any variables residing in the program's global scope.

The output of the code above would be:

```javascript
outerArg = 7
outerFuncVar = x
innerArg = 5
innerFuncVar = y
globalVar = abc
```

</details>

## Question 5. Write a mul function which will work properly when invoked with following syntax.

```javascript
console.log(mul(2)(3)(4)); // output : 24
console.log(mul(4)(3)(4)); // output : 48
```
<details><summary><b>Answer</b></summary>

```javascript
function mul (x) {
  return function (y) { // anonymous function
    return function (z) { // anonymous function
      return x * y * z;
    };
  };
}
```

Here the `mul` function accepts the first argument and returns an anonymous function which then takes the second parameter and returns one last anonymous function which finally takes the third and final parameter; the last function then multiplies `x`, `y` and `z`, and returns the result of the operation.

In Javascript, a function defined inside another function has access to the outer function's scope and can consequently return, interact with or pass on to other functions, the variables belonging to the scopes that incapsulate it.

- A function is an instance of the Object type
- A function can have properties and has a link to its constructor method
- A function can be stored as a variable
- A function can be passed as a parameter to another function
- A function can be returned by another function

</details>
