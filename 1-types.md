## Type Definitions

The @type tag is used to specify the type of a variable or property. It's helpful for documenting the expected type of values, especially in JavaScript where types are not explicitly declared.


### @type

* Primitive, like string or number.

```typescript
/**
 * @type {string}
 */
const name: string = "Vue.js"

```

* Declared in a TypeScript declaration, either global or imported.

```typescript
/**
 * @type {HelpCrunch}
 */

const helpCrunch = window.HelpCrunch
```

* Multiple types (type union)

```typescript
/**
 * @type {string|boolean}
 */

const value = response.data.title || response.data._id
```

* Nullable type

```typescript
/**
 * @type {?number}
 */
const value = response.data._id || null


/**
 * @type {?string}
 */
const title = response.data._id || null
```

### @typedef

* Defining a union type

```typescript
/**
 * A number, or a string containing a number.
 * @typedef {(number|string)} NumberLike
 */

/**
 * Set the magic number.
 * @param {NumberLike} x - The magic number.
 */
function setMagicNumber(x) {
}

```

* Defining a complex type

```typescript
/**
 * @typedef {Object} UserInformation - user information
 * @property {string} user.email - The user email
 * @property {string} user.password - The user password
 * @property {number} user.age - The user age
 * @property {boolean=} user.premium - optional user premium status
 * @property {boolean} [user.isSuperUser] - optional user isSuperUser status
 * @property {string} [user.city=istanbul] - optional user city with default
 */

/** @type {UserInformation} */
let user1;
```


[Back to Table of Contents](README.md)
