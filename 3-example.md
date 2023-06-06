### @example

The @example tag is used to provide an example of how to use the documented item

* Basic usage of @example:
```typescript
/**
 * @param {string} name
 * @example 
 * // Hello Vue.js
 * sayHello("Vue.js");
 */
function sayHello(name: string) {
    alert('Hello ' + name);
}
```

* You can include multiple examples:
```typescript
/**
 * @param name
 * @example 
 * // Hello Vue.js
 * sayHello("Vue.js");
 * @example
 * // Hello World
 * sayHello("World");
 */
function sayHello(name: string) {
    alert('Hello ' + name);
}
```


* For complex or multiline examples, you can use HTML <caption> to provide a description:
```typescript
/**
 * Returns the sum of an array of numbers.
 * @param {number[]} arr - The array of numbers
 * @returns {number} The sum of the numbers in the array
 * @example
 * <caption>Example usage of sum.</caption>
 * // returns 6
 * sum([1, 2, 3]);
 * // returns 10
 * sum([1, 2, 3, 4]);
 */
function sum(arr) {
  return arr.reduce((a, b) => a + b, 0);
}
```


[Back to Table of Contents](README.md)
