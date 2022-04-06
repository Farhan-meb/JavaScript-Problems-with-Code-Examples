**Question:** Explain what a callback function is and provide a simple example.

**Answer:** A callback function is a function that is passed to another function as an argument and is executed after some operation has been completed. Below is an example of a simple callback function that logs to the console after some operations have been completed.

<span style="color: green">
const sum = (a, b, callback) => {
    const sum = a + b;
    callback();
}

const a = 5, b = 6;

sum(a, b, function () {
    console.log('summation done!')
})</span>