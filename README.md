# JavaScript ES6 Cheatsheet

- You should avoid using arrow functions in class as they won't be the part of prototype and thus not shared by every instance.

### [for/for-in/for-if/forEach](https://thecodebarbarian.com/for-vs-for-each-vs-for-in-vs-for-of-in-javascript)

- The for and for/in looping constructs give you access to the index in the array, not the actual element:
for (let i = 0; i < arr.length; ++i) {
  console.log(arr[i]);
}

for (let i in arr) {
  console.log(arr[i]);
}

- With the other two constructs, forEach() and for/of, you get access to the array element itself.
arr.forEach((v, i) => console.log(v));

for (const v of arr) {
  console.log(v);
}

- Iterating through an array using for/in is generally bad practice because it does not ignore the non-numeric property.
- Empty elements in an array: for/in and for/each skip the empty element, for and for/of do not.
- Use arrow functions with forEach()
- Another edge case with forEach() is that it doesn't quite work right with async/await or generators. You can't use yield either. 

_Generally, for/of is the most robust way to iterate over an array in JavaScript. It is more concise than a conventional for loop and doesn't have as many edge cases as for/in and forEach(). The major downsides of for/of is that you need to do extra work to access the index (1), and you can't chain like you can with forEach(). forEach() comes with several caveats and should be used sparingly, but there are numerous cases where it makes code more concise._


- Rest parameters:
const myFunc = (...args) => {
  sum = 0
  for
}
