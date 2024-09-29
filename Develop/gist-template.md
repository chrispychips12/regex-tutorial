# Understanding the Email Regex

A short tutorial to understand how the regular expression for matching an email address works.

## Summary

The regex `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` is used to validate email addresses. 

This will ensure that the email has proper formatting with a local part, an "@" symbol, a domain, and a top-level domain.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors are used to make sure that the regex matches the start all the way to end of the of a string.

- `^` asserts the position at the start of the string.
- `$` asserts the position at the end of the string.

### Anchors

Anchors are used to ensure that the regex matches from the start to the end of the string. 
The `^` symbol asserts the position at the start of the string, ensuring that the match must begin right at the start. 
THe `$` symbol asserts the position at the end of the string, ensuring that the match must end right at the end. 
This way, the entire string must conform to the pattern defined by the regex.

Real-life example: When you sign up for a new account on a website:
the form often checks if your email address is valid. 
The regex ensures that the email address starts and ends correctly.

Example:
```javascript
const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
console.log(regex.test("example@example.com")); // true
console.log(regex.test("example.com")); // false
````

### Quantifiers

Quantifiers specify how many instances of a character, group, or character class
must be present in the input for a match to be found.

- `+` matches one or more of the preceding token.

Real-life example: When entering a username or password, the system might require at least one character to be present. 
The `+` quantifier ensures that the input is not empty.

Example:
```javascript
const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
console.log(regex.test("e@example.com")); // true
console.log(regex.test("@example.com")); // false
```

### OR Operator

The OR operator `|` is not used in this regex.

### Character Classes

Character classes match any one of a set of characters.
In this regex, `[a-z0-9_\.-]` matches any lowercase letter, digit, underscore, dot, or hyphen. 
This allows for a wide range of characters in the local part and domain of the email address-
making the regex flexible and robust.

- `[a-z0-9_\.-]` matches any lowercase letter, digit, underscore, dot, or hyphen.

Real-life example: When creating a username, you might be allowed to use letters, numbers, 
and certain special characters. 
The character class ensures that only valid characters are used.

Example:
```javascript
const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
console.log(regex.test("user_name@example.com")); // true
console.log(regex.test("user!name@example.com")); // false
```

### Flags

Flags are not applicable in this regex.

### Grouping and Capturing

Grouping and capturing are used to group parts of the regex and capture the matched text.

In this regex:

- `([a-z0-9_\.-]+)` captures the local part of the email
- `([\da-z\.-]+)` captures the domain
- `([a-z\.]{2,6})` captures the top-level domain

These groups can be used to extract specific parts of the email address for further processing.

Real-life example: When processing an email address, you might want to extract the username, 
domain, and top-level domain separately. 
Grouping and capturing allow you to do this easily.

Example:
```javascript
const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
const match = "user@example.com".match(regex);
console.log(match[1]); // "user"
console.log(match[2]); // "example"
console.log(match[3]); // "com"
```

### Bracket Expressions

Bracket expressions are used to match any one of the enclosed characters. 
In this regex, `[a-z0-9_\.-]` matches any lowercase letter, digit, underscore, dot, or hyphen. 
This allows for a wide range of characters in the local part and domain of the email address.

Real-life example: When validating a password, you might allow a set of special characters. 
Bracket expressions ensure that only the allowed characters are used.

Example:
```javascript
const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
console.log(regex.test("user.name@example.com")); // true
console.log(regex.test("user@name@example.com")); // false
```

### Greedy and Lazy Match

Greedy and lazy matches are not explicitly used in this regex.

### Boundaries

Boundaries are not explicitly used in this regex.

### Back-references

Back-references are not used in this regex.

### Look-ahead and Look-behind

Look-ahead and look-behind are not used in this regex.

## Author

This tutorial was written By Christopher Concepcion (https://github.com/chrispychips12)