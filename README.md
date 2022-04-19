# Javascript मध्ये हे 15 functions आलेच पाहीजेत.

## forEach()

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


## map()

<details><summary><b>Answer</b></summary>

map() creates a new array from calling a function for every array element.example:

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

  const NewPhonesArray = phones.map((phone) => {
      
     return phone.price - 10;
  
  });
  
  console.log(NewPhonesArray);
 
  
 ``` 
</details>


## filter()

<details><summary><b>Answer</b></summary>

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

  const NewPhonesArray = phones.filter((phone) => {
      
     return phone.price > 800;
  
  });
  
  console.log(NewPhonesArray);
  
  //output
  [ { brand: 'Apple', price: 1000 },
  { brand: 'LG', price: 1200 },
  { brand: 'Nokia', price: 1500 } ]
``` 
</details>

## some()

<details><summary><b>Answer</b></summary>
  
 The some() method executes the function once for each array element:
  
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

  const NewPhonesArray = phones.some((phone) => {
      
     return phone.price === 800;
  
  });
  
  console.log(NewPhonesArray);
  
  //output
   true
``` 
</details>

## every()

<details><summary><b>Answer</b></summary>
  
The every() method returns true if the function returns true for all elements.
  
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

  const NewPhonesArray = phones.every((phone) => {
      
     return phone.price > 500;
  
  });
  
  console.log(NewPhonesArray);
  
  //output
   false
``` 
</details>

## find()

<details><summary><b>Answer</b></summary>
  
The find() method returns the value of the first element that passes a test.
  
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

  const NewPhonesArray = phones.find((phone) => {
      
     return phone.price > 300;
  
  });
  
  console.log(NewPhonesArray);
  
  //output
   { brand: 'Apple', price: 1000 }
``` 
</details>

## includes()

<details><summary><b>Answer</b></summary>
  
The includes() method returns true if an array contains a specified value.
  
```javascript
  
const fruits = ["Banana", "Orange", "Apple", "Mango"];
  
console.log(fruits.includes("Mango"));
  
  //output
   true
``` 
</details>

## slice()

<details><summary><b>Answer</b></summary>
  
The slice() method returns selected elements in an array, as a new array.
  
```javascript
  
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
  
const sliceArray = fruits.slice(1, 3);

console.log(sliceArray)
  
  //output
   [ 'Orange', 'Lemon' ]
``` 
</details>

## splice()

<details><summary><b>Answer</b></summary>
  
The splice() method adds and/or removes array elements.

The splice() method overwrites the original array.
  
```javascript
  
const fruits = ["Banana", "Orange", "Apple", "Mango", "Kiwi"];
// At position 2, remove 2 items: 
const NewArr = fruits.splice(2, 2);

console.log(NewArr)
  //output
   [ 'Apple', 'Mango' ]
``` 
</details>

## reduce()

<details><summary><b>Answer</b></summary>
  
```javascript
  
let num = [5, 10, 15]

let sum = num.reduce(function (total, curValue) {

  return total + curValue

}, 0)

console.log(sum)
  //output
   30
``` 
</details>

## push()

<details><summary><b>Answer</b></summary>
  
```javascript
  
let arr = [5, 10, 15]

let size = arr.push(20)

console.log(size)
console.log(arr)
  //output
   4
  [ 5, 10, 15, 20 ]
``` 
</details>

## pop()

<details><summary><b>Answer</b></summary>
  
```javascript
  
let arr = [5, 10, 15]

let RemoveElement = arr.pop()

console.log(RemoveElement)
console.log(arr)
  //output
   15
  [ 5, 10]
``` 
</details>

## unshift()

<details><summary><b>Answer</b></summary>
  
```javascript
  
let arr = [10,20,30]

let size = arr.unshift(5)

console.log(size)
console.log(arr)
  //output
   4
  [ 5,10,20,30]
``` 
</details>

## shift()

<details><summary><b>Answer</b></summary>
  
```javascript
  
let arr = [10,20,30]

let size = arr.shift()

console.log(size)
console.log(arr)
  //output
   10
  [ 20,30]
``` 
</details>

## indexof()

<details><summary><b>Answer</b></summary>
  
```javascript
  
let arr = [10,20,30,40,50]

let index = arr.indexOf(40)

console.log(index)
  //output
   3
``` 
</details>

