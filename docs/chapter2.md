### Chapter 2: Values, Types and Operators

Inside a computer's world, there is only data. You can read data, modify data, create new data.

All of this is stored as sequences of _bits_. Bits are usually described as zeros and ones(binary).

Everything can be expressed in terms of 1s and 0s.

## Values

Chunks that represent pieces of information are called _values_.

Every value has a type that determines what it does.

These types are called _Data Types_

## Data Types

## Numbers

These are numeric values. They are both integer type and floating point type numbers

```
13 56 7.5
```

JS(we will call it as such going forward) uses a fixed number of bits(64) to store single number value.

### Arithmetic

You can go arithmetic with JS numbers. All operations such as `* - / + %` are valid. It also understands BODMAS.

```js
((100 * 50 - 2) % 2) - 3;
```

The `%` is the modulo operator which gives us the remainder of the operation.

```js
4 % 2; // outputs 0
```

### Special Numbers

JS has special numbers `Infinity` and `-Infinity`. Infinity + 2 is Infinity.

It also has `NaN` => "not a number" even though it s a value of type number.

Dividing by zero will give you NaN. Generally operations that don't yield a meaningful result yield NaN.

## Strings

Strings are used to represent text. They are written by enclosing content in quotes.

```
`John is a brave man`
"Jack loves pizza"
"Run, Jack, run!"
```

You can put anything between quotes to make a string. We have special characters like `\n` which represents the newline character. `\` are used to escape a character meaning a character that comes after it makes it a special character. Some examples include: `\n` `\t` `\b`

```
"This is the first line\nAnd this is the second"
```

will be outputed as:

```
This is the first line
And this is the second line
```

Strings cannot be divided, multiplied, or subtracted but they can be added in an operation called _string concatenation_

```js
"Hello " + "World"; // produces Hello World
```

### Unary Operators

A unary operator has one operand. Some examples of unary operators include they `typeof` operator and `!` which will see a bit later.

Typeof returns the data type of a value.

```js
typeof 7.2; // produces number

typeof "Jack"; // produces string
```

## Boolean Values

These represent truthy and falsy values. These are represented using `true` or `false` keywords.

### Logical operators

These are operators used for comparisons.

Some of them include: `>` `<` `==` `!` `>=` `<=` `===`

```js
3 < 2; // outputs false

7 > 2; // outputs true

"Apples" > "Oranges"; // outputs false

5 == 5; // outputs true

5 == "5"; // outputs true

5 === "5"; // outputs false
```

The only value in JS not equal to itself is `NaN`, so

```js
NaN == NaN; // outputs false
```

### Logical Operators

These operators can be applied to Boolean values.

They are `and` `or` and `not`

```js
true && false => false

true && true => true

true || false => true

false || true => true
```

Generally `||` has the lowest precedence, then `&&` and then the comparison operators (>, ==, etc), and then the rest. This order helps in things like this:

```js
5 + 5 == 10 && 20 * 20 > 50; // ???
```

Another logical operator is the `ternary operator` which requires 3 operands.

It is written as such: `condition ? truthy value : falsy value`

```js
5 > 2 ? "5 is greater" : "5 is not greater than 2" => ??
```

### Empty values

JS has 2 special values called: `null` and `undefined`

They are values but carry no information. The difference between them is an accident in JS's design and it doesn't matter much most of the time.

### Automatic Type Conversion

```js
8 * null; // => 0

"5" - 1; // => 4

"5" + 1; // => 51

"five" * 2; // => NaN
```

JavaScript does type coercion when it percieves the "wrong" type of value has been used.

### Short circuiting of logical operators

```js
null || "user"; // user

"Agnes" || "user"; // Agnes
```
