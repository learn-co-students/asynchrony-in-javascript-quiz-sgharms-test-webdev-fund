# Quiz: Variables and Scope in Ruby

## Introduction

Welcome to our quiz! Quizzes are designed for knowledge exploration and finding
weaknesses in your understanding. Use this to check up on your understanding.
Even if you see the "right" answer, consider what it would take to change the
given code to make it work. Think through the bugs that may arise in the given
code and consider multiple ways to fix the errors. Doing so will improve your
learning as there is always more than one solution and that solution may not be
immediately obvious. Incidentally, those are common tasks to assign in an
interview: explaining buggy code and then debugging it. Accordingly, these are
skills that we hope to help you grow over your course of study at Flatiron!

???

# Asynchronous JavaScript

?: What is the threading model of JavaScript

( ) Global Interpreter Lock
( ) Multicore
(*) Single-Threaded
( ) Multi-Threaded

?: Which of the following commands does not use asynchronous processing

( ) `fetch()`
( ) `setTimeout()`
(X) `console.log()`
( ) `jQuery.get()`

?: In JavaScript, execution can be reliably traced by following from top-down,
left to right.

( ) True
(X) False

?: A selling feature of libraries like jQuery and React is that they handle
asynchronous logic for you.

( ) True
(X) False

?: In a language without asynchronous processing (something not like
JavaScript), if a web request is made the code will not process until the
response is received and handled.

(X) True
( ) False

?: Given that `setTimeout` takes a function and a time (in milliseconds) as arguments (`setTimeout(fn, time)`), what is the expected output of this code (output lines have been collapsed):

```javascript
setTimeout(() => console.log("Hello"), 5);
console.log("World");
```

( ) Hello World
(X) World Hello
( ) Trick Question: `setTimeout` "steals" the output filehandle
( ) Hello Hello Hello Hello Hello World

?: Given that `setTimeout` takes a function and a time (in milliseconds) as arguments (`setTimeout(fn, time)`), what is the expected output of this code (output lines have been collapsed):

```javascript
setTimeout(() => console.log("Hello"), 0);
console.log("World");
```

( ) Hello World
( ) Trick Question: `setTimeout` "steals" the output filehandle
(X) World Hello
( ) World

?: What is the expected output of this command? Assume the server returns
`{"name": "Byron"}`:

```javascript
var babyName;

fetch("http://flatiron-baby-name.example.com")
  .then(response => response.json())
  .then(data => babyName = data.name);


console.log(`I've named my kid, ${babyName}`);

```

(X) I've named my kid, undefined
( ) I've named my kid, Byron
( ) This code will not work
( ) `babyName` will be updated in a parallel thread

?: What is the expected output of this command? Assume the server returns a
random Integer. On this particular run it will return `2` and `3`.

```javascript
var addends = [];

fetch("http://flatiron-random-integer.example.com")
  .then(response => parseInt(response.text()))
  .then(newInt => addends.push(newInt));

fetch("http://flatiron-random-integer.example.com")
  .then(response => parseInt(response.text()))
  .then(newInt => addends.push(newInt));

setTimeout(() => {
   var sum = addends[0] + addends[1];
   console.log(sum);
}, 500)
```

( ) 5
( ) 2 undefined
( ) undefined 3
(X) We have no way of being certain

???
