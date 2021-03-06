##
 ⚡ <i><b>Explain what a callback function is and provide a simple example</b></i>
<details><summary><b>Answer</b></summary><br />
🌱 A callback function is a function that is passed to another function as an argument and is executed after some operation has been completed. Below is an example of a simple callback function that logs to the console after some operations have been completed. <br /> <br />

```go
const sum = (a, b, callback) => {
    const sum = a + b;
    callback();
}

const a = 5, b = 6;

sum(a, b, function () {
    console.log('summation done!')
})
```
</details>

##
 ⚡ <i><b>How to empty an array in JavaScript?</b></i>
<details><summary><b>Answer</b></summary><br />

```go
let array = [1,2,3,4,5];
1. array = [];
2. array.length = 0;
3. array.splice(0,array.length);
4. while(arrayList.length) {arrayList.pop();}
```
</details>

##
 ⚡ <i><b>Given a string, reverse each word in the sentence</b></i>
<details><summary><b>Answer</b></summary><br />
🌱 For example "Welcome to this Javascript Guide!" should become "emocleW ot siht tpircsavaJ !ediuG" <br /> <br />

```go
let string = "Welcome to this Javascript Guide!";
string = string.split('').reverse().join(''); //reverse full string
string = string.split(' ').reverse().join(' '); //reverse words
console.log(string); //print reversed string
```
</details>

##
 ⚡ <i><b>Write a simple function (less than 160 characters) that returns a boolean indicating whether or not a string is a palindrome</b></i>
<details><summary><b>Answer</b></summary><br />

```go
const isPalindrome = (string) => {
    string = string.toLowerCase();
    return (string === string.split('').reverse().join(''));
}

console.log(isPalindrome("MadAm")); //true
console.log(isPalindrome("MadAaaam")); //false

```
</details>

##
 ⚡ <i><b>In what order will the numbers 1-4 be logged to the console when the code below is executed?</b></i>

```go
(function() {
    console.log(1); 
    setTimeout(function(){console.log(2)}, 1000); 
    setTimeout(function(){console.log(3)}, 0); 
    console.log(4);
})();
```
<details><summary><b>Answer</b></summary><br />

```go
1
4
3
2
```
</details>

##
 ⚡ <i><b>Write a sum method which will work properly when invoked using either syntax below.</b></i>

 ```go
console.log(sum(2,3));   // Outputs 5
console.log(sum(2)(3));  // Outputs 5
```

<details><summary><b>Answer</b></summary><br />

```go
(function sum(x,y) {
    if(y !== undefined){
        return x+y;
    }
    else{
        return function(y){
            return x+y;
        }
    }
})();
```
</details>

##
 ⚡ <i><b>What will be the output of the following code?</b></i>

```go
(function timer() {
  for (var i=0; i<=5; i++) {
    setTimeout(function clog() {console.log(i)}, i*1000);
  }
})();
```
<details><summary><b>Answer</b></summary><br />

```go
6
6
6
6
6
6
```
<b>With var you have a function scope, and only one shared binding for all of your loop iterations - i.e. the i in every setTimeout callback means the same variable that finally is equal to 6 after the loop iteration ends.</b>
</details>

##
 ⚡ <i><b>What will be the output of the following code?</b></i>

```go
(function timer() {
  for (let i=0; i<=5; i++) {
    setTimeout(function clog() {console.log(i)}, i*1000);
  }
})();
```
<details><summary><b>Answer</b></summary><br />

```go
0
1
2
3
4
5
```
<b>With let you have a block scope and when used in the for loop you get a new binding for each iteration - i.e. the i in every setTimeout callback means a different variable, each of which has a different value: the first one is 0, the next one is 1 etc.</b>
</details>

##
 ⚡ <i><b>What will be the output of the following code?</b></i>

```go
let text = "Hello world!";
let result = text.slice(0, 5);
```
<details><summary><b>Answer</b></summary><br />

```go
Hello
```
<b>slice() extracts a part of a string and returns the extracted part.</b>
</details>

##
 ⚡ <i><b>Write a function that would allow you to do this?</b></i>

```go
let addSix = createBase(6);
addSix(10); // returns 16
addSix(21); // returns 27
```
<details><summary><b>Answer</b></summary><br />
<b>You can create a closure to keep the value passed to the function createBase even after the inner function is returned. The inner function that is being returned is created within an outer function, making it a closure, and it has access to the variables within the outer function, in this case the variable baseNumber.</b>
 
```go
function createBase(baseNumber) {
  return function(N) {
    return baseNumber + N;
  }
}

let addSix = createBase(6);
addSix(10);
addSix(21);
```
</details>

##
 ⚡ <i><b>Write a "mul" function which will properly when invoked as below syntax</b></i>

```go
console.log(mul(2)(3)(4)); // output : 24
console.log(mul(4)(3)(4)); // output : 48
```
<details><summary><b>Answer</b></summary><br />

```go
function mul (x) {
  return function (y) { // anonymous function
    return function (z) { // anonymous function
      return x * y * z;
    };
  };
}
```
<b>Here mul function accept the first argument and return anonymous function which take the second parameter and return anonymous function which take the third parameter and return multiplication of arguments which is being passed in successive</b>

</details>

##
 ⚡ <i><b>Given two strings, return true if they are anagrams of one another</b></i>

<details><summary><b>Answer</b></summary><br />

```go
const isAnagram = (str1, str2) => {
  return (
    str1.toLowerCase().split("").sort().join("") ===
    str2.toLowerCase().split("").sort().join("")
  );
};

console.log(isAnagram("Amar", "mraa"));     //true
console.log(isAnagram("Amar", "mraab"));    //false

```
</details>
