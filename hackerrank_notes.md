- use `readLine()` to get data from cmd line.
- Array(11).join("abc") use this to repeat join characters 11 - 1 times without using loops.

Converting to interger number
 - bitwise or i.e. (number | 0) or parseInt(3.00909, 10).
 - parseFloat for float numbers, x.toFixed(num_of_decimals)

#### Class vs Inheritance
![Checkout css tricks](https://css-tricks.com/understanding-javascript-constructors/)
and kyle ydkjs in guthub

#### Reverse Array
- this is essentially swapping values,
- array has inbuilt array.reverse(), kinda slow
- two types of swaps, temp swap and XOR swap.

use array. join to list elements.
Checkout http://stackoverflow.com/questions/5276953/what-is-the-most-efficient-way-to-reverse-an-array-in-javascript
*Temp swap*
- have 2 indices, left and right inside a loop
- left is the first element, right is length -1, loop till left < right
- in body, store left in temp var, and swap vars.

*XOR swap*
- Dont understand, check this.

#### Hastable or Hashmap/ Dicionaries
- Javascript by default does not have Hastable or hashmap,
- it uses arrays for all associative arrays http://stackoverflow.com/questions/1208222/how-do-i-implement-a-dictionary-or-hashtable-in-javascript
-
#### Recursion
Algorithm :
if N<= 1 then 1
else N * factorial (N - 1)

 return (n > 1) ? n * factorial(n-1) : 1;

if there is 1 if else, do ternary operator.

#### Binary conversion
**right logical shift**
 function dec2bin(num) {
     return (num >>> 0).toString(2);
 }

**count total repeats**
uniqueCount.forEach(function(element) {
  counts[element] = (counts[element] || 0) + 1;
});

simpler solution
var n = parseInt(readLine()).toString(2);
  var splits = n.split('0');
  console.log(splits.map(function(elem){return elem.length;}).reduce(function(a,b){
      if (a>b) return a; else return b;}));
