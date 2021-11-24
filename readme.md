2. Write a program to reverse a given integer number
The remainder of the number can be fetched and the number can be divided by 10 to remove the the digit in loop till number becomes 0
A simple approach to reverse a number could also be to convert it in to a string and then reverse it
```js
let num = 4587;
const arr = []
while(num > 0){
  // console.log( num % 10);
  const mod = num % 10;
  console.log(mod);
  num = Math.floor(num / 10);
  arr.push(''+mod)
}
arr.join('')
```
