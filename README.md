# Understanding Hoisting in JavaScript with Regular Expressions

## Introduction:

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution. This can often lead to confusion and unexpected results, especially for beginners.

In this tutorial, we'll use regular expressions to understand hoisting in JavaScript. We'll start by defining a regular expression that matches hoisted function declarations and then move on to variables.

## Summary:

The regular expression we'll be using to match hoisted function declarations is:


This regex matches any line of code that starts with the word "function", followed by one or more whitespace characters, followed by the name of the function (a word character), followed by optional whitespace characters, followed by an opening parenthesis and any number of characters that are not a closing parenthesis, followed by a closing parenthesis, optional whitespace characters, and an opening curly brace.

## Table of Contents:

- [Matching Hoisted Function Declarations](#matching-hoisted-function-declarations)
- [Matching Hoisted Variables](#matching-hoisting-variables)
- [Conclusion](#conclusion)
- [About the Author](#about-the-author)

## Section 1: Matching Hoisted Function Declarations

To understand hoisted function declarations, let's take a look at the following code snippet:
```
foo();

function foo() {
  console.log('hello');
}
```

This code will execute without any errors, even though the function foo is called before it's declared. This is because function declarations are hoisted to the top of their scope.

To match hoisted function declarations with regular expressions, we can use the following pattern:

```
/^function\s+\w+\s*\([^)]*\)\s*\{/
```
This pattern matches the function keyword followed by one or more whitespace characters, followed by the name of the function (a word character), followed by optional whitespace characters, followed by an opening parenthesis and any number of characters that are not a closing parenthesis, followed by a closing parenthesis, optional whitespace characters, and an opening curly brace.

## Section 2: Matching Hoisted Variables

Now let's take a look at how hoisted variables work. Consider the following code snippet:

```
console.log(x);
var x = 5;
```

This code will log undefined to the console, not an error, even though x is accessed before it's declared. This is because variable declarations are also hoisted to the top of their scope, but the initialization is not.

To match hoisted variables with regular expressions, we can use the following pattern:

```
/^(var|let|const)\s+\w+/
```

This pattern matches the variable keyword followed by one or more whitespace characters, followed by the name of the variable (a word character).

## Section 3: Conclusion

In this tutorial, we used regular expressions to understand hoisting in JavaScript. We defined regular expressions that match hoisted function declarations and variables. By understanding hoisting and how it works, we can avoid common mistakes and write more maintainable code.

## Section 4: About the Author

Myles Nichols is a web developer who is getting his foot in the door programming. He is an asapiring web developer who specializes on front end development. You can find more of Myles's work on their GitHub profile: [https://github.com/MylesNichols](https://github.com/MylesNichols). 
