##
 ⚡ <i><b>Explain what a callback function is and provide a simple example</b></i>
<details><summary><b>Answer</b></summary>
- A callback function is a function that is passed to another function as an argument and is executed after some operation has been completed. Below is an example of a simple callback function that logs to the console after some operations have been completed.


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
##
 ⚡ <i><b>How to empty an array in JavaScript?</b></i>
<details><summary><b>Answer</b></summary>
```go
let array = [1,2,3,4,5];
1. array = [];
2. array.length = 0;
3. array.splice(0,array.length);
4. while(arrayList.length) {arrayList.pop();}
```