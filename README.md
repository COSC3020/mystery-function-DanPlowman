[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/GDPVb20V)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```
This is a recursive function that recieves an array. 
The first if condition checks the length of the array, if it contains 2 indices, 0 and 1, it returns the value of the first index.
foo is assigned to the recursion part of the function, a.slice(1,a.length)) makes a second array, containing the elements of the first array starting from index 1 and going through the length of the array, then passes it into the recursive function. At the so called "bottom" of this recursive ladder, if the length of 'a' is 1, the value of a is assigned to foo. foo then is compared to the value indexed in the second to last value of the array, and the greater number is assigned to foo, this repeats until the full array has been compared, and results in searching the array for the largest number indexed.
