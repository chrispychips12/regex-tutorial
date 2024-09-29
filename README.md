# Email Regex Tutorial

This repository contains a detailed tutorial on understanding and using a regular expression (regex) for validating email addresses. The tutorial breaks down each component of the regex and explains its functionality with examples.

You can find the full tutorial on GitHub Gist [here](https://gist.github.com/chrispychips12/bce8ceecaa4fb3567c511a80af17b4f8#file-gistfile1-txt-L1).

<img width="977" alt="Screenshot 2024-09-29 at 10 17 41 AM" src="https://github.com/user-attachments/assets/88b860ed-f3bc-4a83-a882-e8ea7b7705c8">

## Summary

The regex `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` is used to validate email addresses. It ensures that the email has a proper format with a local part, an "@" symbol, a domain, and a top-level domain.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors

Anchors are used to ensure that the regex matches from the start to the end of the string. The `^` symbol asserts the position at the start of the string, ensuring that the match must begin right at the start. Similarly, the `$` symbol asserts the position at the end of the string, ensuring that the match must end right at the end. This way, the entire string must conform to the pattern defined by the regex.

Real-life example: When you sign up for a new account on a website, the form often checks if your email address is valid. The regex ensures that the email address starts and ends correctly.

Example:
```javascript
const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
console.log(regex.test("example@example.com")); // true
console.log(regex.test("example.com")); // false
```

### Quantifiers<img width="977" alt="Screenshot 2024-09-29 at 10 17 41 AM" src="https://github.com/user-attachments/assets/54b4e462-1444-4eab-a75b-004c3c0b8411">


Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

- `+` matches one or more of the preceding token.

Real-life example: When entering a username or password, the system might require at least one character to be present. The `+` quantifier ensures that the input is not empty.

Example:
```javascript
const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
console.log(regex.test("e@example.com")); // true
console.log(regex.test("@example.com")); // false
```

### Character Classes

Character classes are used to match any one of a set of characters.

- `\d` matches any digit (0-9).
- `\w` matches any word character (alphanumeric and underscore).
- `\s` matches any whitespace character (space, tab, newline, etc.).

Real-life example: When filling out a form, you might need to enter your name. The regex ensures that the name contains only letters, numbers, and underscores.

Example:
```javascript
const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
console.log(regex.test("example@example.com")); // true
console.log(regex.test("example.com")); // false
```

### Grouping and Capturing

Grouping and capturing is used to group parts of the regex together and capture them as a single unit.

Real-life example: When you sign up for a new account on a website, the form often checks if your email address is valid. The regex ensures that the email address starts and ends correctly.

Example:
```javascript
const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
console.log(regex.test("example@example.com")); // true
console.log(regex.test("example.com")); // false
```                 

### Bracket Expressions

Bracket expressions are used to match any one of a set of characters.

Real-life example: When you sign up for a new account on a website, the form often checks if your email address is valid. The regex ensures that the email address starts and ends correctly.

Example:
```javascript
const regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
console.log(regex.test("example@example.com")); // true
console.log(regex.test("example.com")); // false
``` 
## Author

This tutorial was written by [Christopher Concepcion](https://github.com/chrispychips12).

## Link to the Gist

You can find the full tutorial on GitHub Gist [here](https://gist.github.com/chrispychips12/bce8ceecaa4fb3567c511a80af17b4f8#file-gistfile1-txt-L1).
