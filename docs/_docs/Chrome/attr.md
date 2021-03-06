---
title: .attr
category: Chrome
---

The `attr` method operates similarly to the [jQuery `attr` method](http://api.jquery.com/attr/), and return the value of an attribute of a DOM element. It's called with 2 parameters: the css-style selector of the element you wish to query, and the attribute you want to retrieve.

*JavaScript*
```js
const { Chrome } = require('navalia');
const chrome = new Chrome();

// Getting an attribute
chrome.goto('https://joelgriffith.github.io/navalia/')
.then(() => chrome.attr('.buy-now', 'href'))
.then((link) => console.log(link)) // Prints the 'href' link
.then(() => chrome.done());
```

*TypeScript*
```ts
import { Chrome } from 'navalia';
const chrome = new Chrome();

// Getting an attribute
async function getAll() {
  await chrome.goto('https://joelgriffith.github.io/navalia/');
  const link = await chrome.attr('.buy-now', 'href');
  console.log(link); // Prints the 'href' link
  chrome.done();
}

click();
```
