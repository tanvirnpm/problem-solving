### 1. Function which returns a random number in the given range
- Create a function which returns a random number in the given range of values both inclusive

#### Test Case
- randomNumberGeneratorInRange(10, 50) should return a number between 10-50 (inclusive)
- randomNumberGeneratorInRange(100, 200) should return a number between 100-200 (inclusive)

##### Solution:::::
```js
function randomNumberGeneratorInRange(rangeStart, rangeEnd) {
	// write your solution here
	return Math.floor(Math.random() * (rangeEnd - rangeStart + 1) ) + rangeStart;
}

console.log(`My random number: ${randomNumberGeneratorInRange(5, 100)}`)
```

### 2. Write a program to reverse a given integer number
- The remainder of the number can be fetched and the number can be divided by 10 to remove the the digit in loop till number becomes 0
- A simple approach to reverse a number could also be to convert it in to a string and then reverse it

#### Test Case
- reverseAString("JavaScript is awesome") should return "emosewa si tpircSavaJ"
- reverseAString("Peter Parker is Spiderman") should return "namredipS si rekraP reteP"
- reverseAString("codedamn") should return "nmadedoc"
##### Solution:::::
```js
const str = "JavaScript is awesome"

function reverseAString(str) {
    // write your solution here

    return str.split('').reverse().join('')
}

console.log(`Reversed string is: ${reverseAString(str)}`)

```

### 3. Write a program to reverse a given integer number
- The remainder of the number can be fetched and the number can be divided by 10 to remove the the digit in loop till number becomes 0
- A simple approach to reverse a number could also be to convert it in to a string and then reverse it
#### Test Case
- reverseGivenInteger(3849) returns 9483
- reverseGivenInteger(2222) returns 2222
- reverseGivenInteger(1002) returns 2001
##### Solution:::::
```js
const num = 3849;

function reverseGivenInteger(num) {
    let rev_num = 0;
        while(num > 0)
        {
            rev_num = rev_num * 10 + num % 10;
            num = Math.floor(num / 10);
        }
        return rev_num;
}

console.log(`Reversed integer is: ${reverseGivenInteger(num)}`)

```
### 4. Write a function which can convert the time input given in 12 hours format to 24 hours format
- The check for 'AM' and 'PM' can be verified using endsWith String method
- An extra 0 would be needed if the hours have single digit
#### Test Case
- convertTo24HrsFormat("12:10AM") returns "00:10"
- convertTo24HrsFormat("5:00AM") returns "05:00"
- convertTo24HrsFormat("12:33PM") returns "12:33"
- convertTo24HrsFormat("01:59PM") returns "13:59"
- convertTo24HrsFormat("11:8PM") returns "23:08"
- convertTo24HrsFormat("10:02PM") returns "22:02"
##### Solution:::::
```js
const time = '12:10AM';

function convertTo24HrsFormat(time) {
    // write your solution here
    let [hour, minutes] = time.split(':');
    let finalMinutes = minutes.replace(/\D/g,'');
    if(hour === '12'){
        hour = '00';
    }
    if(time.endsWith('PM')){
        hour = parseInt(hour, 10) + 12;
    }
    if(hour.length == 1){
        hour = '0'+hour;
    }
    if(finalMinutes.length == 1){
        finalMinutes = '0'+finalMinutes;
    }
    const result = `${hour}:${finalMinutes}`;
    return result;
}

console.log(`Converted time: ${convertTo24HrsFormat(time)}`)

```
