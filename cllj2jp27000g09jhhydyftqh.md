---
title: "JavaScript Promises"
datePublished: Sun Aug 20 2023 06:30:10 GMT+0000 (Coordinated Universal Time)
cuid: cllj2jp27000g09jhhydyftqh
slug: javascript-promises
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1692512881855/b08c2516-f533-48cc-9a5d-ef10e1c1505c.png
tags: js, javascript, promises

---

JavaScript is **synchronous** means it executes the code line by line i.e. from top to bottom. The execution won't move to the next line until the first line is completed.

However, the web is dynamic, with various tasks happening simultaneously – like fetching data from a server. Being JavaScript synchronous programming, until the fetching is done, other parts of the code are blocked.

In such cases, **asynchronous** programming steps in. It allows JavaScript to handle multiple tasks without blocking the main thread. In simple words, it allows to work on multiple tasks parallelly.

We can achieve asynchronous programming via mechanisms like callbacks, Promises, and async/await. We will be discussing Promises today.

## Promises

A **Promise** can be understood as a simple promise you make to someone. For example, you promise your kid that you will buy an ice cream. It can have either of the three states: **pending**, **rejected** and **fulfilled.**

Let's take the earlier example of buying ice cream for your kid. As already mentioned **Promise** can have three states:

1. Until you buy ice cream, a Promise is in a pending state.
    
2. Now, if you buy ice cream for your kid, then the promise is resolved and hence fulfilled.
    
3. But if you do otherwise, then the promise is rejected and hence failed.
    

## Creating Promise

The Promise takes a function as an argument and that function accepts two functions: `resolve()` and `reject().`

If the Promise is successful, `resolve()` is executed and if otherwise, `reject()` is executed.

```javascript
let promise = new Promise(function(resolve, reject) {
    resolve(); // if successful
    reject(); // if failed
})

promise
.then(resolve => console.log(resolve))
.catch(reject => (console.log(reject))
```

Let us consider an example.

```javascript
let promise = new Promise(function(resolve, reject) {
  let x = 5;

  if (x === 5)
    resolve('You are right');
  else
    reject('You are wrong')
});

promise
  .then(resolve => console.log(resolve))
  .catch(reject => console.log(reject))
```

## Output

> `You are right`

I hope this helps. Thank you!