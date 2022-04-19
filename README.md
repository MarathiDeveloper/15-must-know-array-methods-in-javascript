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


## JavaScript Array map()

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


## JavaScript Array filter()

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

## JavaScript Array some()

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

  const NewPhonesArray = phones.some((phone) => {
      
     return phone.price === 800;
  
  });
  
  console.log(NewPhonesArray);
  
  //output
   true
``` 
</details>

## JavaScript Array every()

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

  const NewPhonesArray = phones.every((phone) => {
      
     return phone.price > 500;
  
  });
  
  console.log(NewPhonesArray);
  
  //output
   false
``` 
</details>
