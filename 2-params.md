
## @param

The @param tag is used to document the parameters of a function. It specifies the name, type, and description of the parameter.

* Name only

```typescript
/**
 * @param  name
 */
function sayHello(name: string) {
    alert('Hello ' + name);
}
```


* Name and type

```typescript
/**
 * @param {string} name
 */
function sayHello(name: string): void {
    alert('Hello ' + name);
}
```

* Name, type, and description

```typescript
/**
 * @param {string} name - this function will take the name and show alert.
 */
function sayHello(name: string): void {
    alert('Hello ' + name);
}
```

### Parameters with properties

* Documenting a parameter's properties

```typescript
/**
 * Print user details.
 * @param {object} user - The user informations.
 * @param {string} user.email - The user email
 * @param {string} user.password - The user password
 * @param {number} user.age - The user age
 */
function printUserDetails(user: User): void {
    console.log(user);
}
```

* Documenting a destructuring parameter

```typescript
/**
 * Print user details.
 * @param {User} user - The user informations.
 * @param {string} user.email - The user email
 */
function handleUserEmail({ email }: User): void {
    console.log(email)
}
```

* Documenting properties of values in an array

```typescript
/**
 * Print user details.
 * @param {User[]} users - users informations.
 * @param {string} user[].email - The user email
 */
function handleUsers(users: User[]): void {
    console.log(users)
}
```

### Optional parameters and default values

* An optional parameter

```typescript
/**
 * @param {string} [name] - The name of the user
 */
function sayHello(name: string): void {
    alert('Hello ' + name);
}
```

* An optional parameter and default value

```typescript
/**
 * @param {string} [city=istanbul] - The name of the city
 */
function sayHello(city: string = "istanbul"): void {
    alert('Hello ' + city);
}
```

### Multiple types and repeatable parameters

* Allows one type OR another type (type union)

```typescript
/**
 * @param {string|string[]} data - The data or data list
 */
function log(data: string | string[]): void {
    if (Array.isArray(data)) {
        data.forEach(row => console.log(row))
    } else {
        console.log(data);
    }
}


/**
 * @param {string|string[]} [data=[1,2,3]] - The data or data list
 */
function log(data: string | string[]): void {
    if (Array.isArray(data)) {
        data.forEach(row => console.log(row))
    } else {
        console.log(data);
    }
}
```

* Allows any type

```typescript
/**
 * @param {*} data - The data
 */
function log(data: any): void {
    console.log(data);
}
```

* Allows a parameter to be repeated

```typescript
/**
 * Returns the sum of all numbers passed to the function.
 * @param {...number} num - A number
 * @return {number} sum of all numbers passed
 */
function sum(): number {
    let sum = 0;
    var values = Array.prototype.slice.call(arguments, 0);
    return values.reduce((sum, item) => sum + item);
}


/**
 * Returns the sum of all numbers passed to the function.
 * @param {...number} num - A number
 * @return {number} sum of all numbers passed
 */
function sum(...numbers): number {
    let sum = 0;
    var values = Array.prototype.slice.call(arguments, 0);
    return values.reduce((sum, item) => sum + item);
}
```

### Callback functions

* Parameters that accept a callback

```typescript
/**
 * Returns the sum of  numbers.
 * @param {number} num1 - number 1
 * @param {number} num2 - number 2
 * @return {number} sum of all numbers passed
 */
function sum(num1: number, num2: number): number {
    return num1 + num2;
}

/**
 * The callback type for performing a math operation on two numbers.
 *
 * @callback mathOperationCallback
 * @param {number} num1 - The first number.
 * @param {number} num2 - The second number.
 * @returns {number} The result of the math operation.
 */


/**
 * Performs a math operation on two numbers and executes the callback with the result.
 * @param {number} num1 - The first number.
 * @param {number} num2 - The second number.
 * @param {mathOperationCallback} callback - The callback function that handles the result.
 */
function handleMathOperation(num1: number, num2: number, callback: mathOperationCallback): void {
    const result = callback(num1, num2);
    console.log("The result is:", result);
}
```

[Back to Table of Contents](README.md)
