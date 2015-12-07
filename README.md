#Front-end Job Interview Questions

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## Table of Contents

  1. [General Questions](#general-questions)
  1. [HTML Questions](#html-questions)
  1. [CSS Questions](#css-questions)
  1. [JS Questions](#js-questions)
  1. [Testing Questions](#testing-questions)
  1. [Performance Questions](#performance-questions)
  1. [Network Questions](#network-questions)
  1. [Coding Questions](#coding-questions)
  1. [Fun Questions](#fun-questions)

## Getting Involved

  1. [Contributors](#contributors)
  1. [How to Contribute](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/CONTRIBUTING.md)
  1. [License](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/LICENSE.md)

#### General Questions:

**What did you learn yesterday/this week?**

**What excites or interests you about coding?**

**What is a recent technical challenge you experienced and how did you solve it?**

**What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?**

**Talk about your preferred development environment.**

**Which version control systems are you familiar with?**

**Can you describe your workflow when you create a web page?**

**If you have 5 different stylesheets, how would you best integrate them into the site?**

**Can you describe the difference between progressive enhancement and graceful degradation?**

**How would you optimize a website's assets/resources?**

**How many resources will a browser download from a given domain at a time?**
  * What are the exceptions?

**Name 3 ways to decrease page load (perceived or actual load time).**

**If you jumped on a project and they used tabs and you used spaces, what would you do?**

**Describe how you would create a simple slideshow page.**

**If you could master one technology this year, what would it be?**

**Explain the importance of standards and standards bodies.**

**What is Flash of Unstyled Content? How do you avoid FOUC?**

**Explain what ARIA and screenreaders are, and how to make a website accessible.**

**Explain some of the pros and cons for CSS animations versus JavaScript animations.**

**What does CORS stand for and what issue does it address?**

#### HTML Questions:

**What does a `doctype` do?**

**What's the difference between standards mode and quirks mode?**

**What's the difference between HTML and XHTML?**

**Are there any problems with serving pages as `application/xhtml+xml`?**

**How do you serve a page with content in multiple languages?**

**What kind of things must you be wary of when design or developing for multilingual sites?**

**What are `data-` attributes good for?**

**Consider HTML5 as an open web platform. What are the building blocks of HTML5?**

**Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.**

**Describe the difference between `<script>`, `<script async>` and `<script defer>`.**

**Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?**

**What is progressive rendering?**

**Have you used different HTML templating languages before?**

#### CSS Questions:

**What is the difference between classes and ID's in CSS?**

**What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?**

**Describe Floats and how they work.**

**Describe z-index and how stacking context is formed.**

**Describe BFC(Block Formatting Context) and how it works.**

**What are the various clearing techniques and which is appropriate for what context?**

**Explain CSS sprites, and how you would implement them on a page or site.**

**What are your favourite image replacement techniques and which do you use when?**

**How would you approach fixing browser-specific styling issues?**

**How do you serve your pages for feature-constrained browsers?**
  * What techniques/processes do you use?

**What are the different ways to visually hide content (and make it available only for screen readers)?**

**Have you ever used a grid system, and if so, what do you prefer?**

**Have you used or implemented media queries or mobile specific layouts/CSS?**

**Are you familiar with styling SVG?**

**How do you optimize your webpages for print?**

**What are some of the "gotchas" for writing efficient CSS?**

**What are the advantages/disadvantages of using CSS preprocessors?**
  * Describe what you like and dislike about the CSS preprocessors you have used.

**How would you implement a web design comp that uses non-standard fonts?**

**Explain how a browser determines what elements match a CSS selector.**

**Describe pseudo-elements and discuss what they are used for.**

**Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.**

**What does ```* { box-sizing: border-box; }``` do? What are its advantages?**

**List as many values for the display property that you can remember.**

**What's the difference between inline and inline-block?**

**What's the difference between a relative, fixed, absolute and statically positioned element?**

**The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?**

**What existing CSS frameworks have you used locally, or in production? How would you change/improve them?**

**Have you played around with the new CSS Flexbox or Grid specs?**

**How is responsive design different from adaptive design?**

**Have you ever worked with retina graphics? If so, when and what techniques did you use?**

**Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?**

#### JS Questions:

**Explain event delegation**

Event delegation allows us to attach a single event listener, to a parent element, that will fire for all children matching a selector, whether those children exist now or are added in the future.the underlying cause is browser's event bubbling.

**Explain how `this` works in JavaScript**

The this object is bound at runtime based on the context in which a function is executed:

1. when used inside global functions,this is equal to window in nostrict mode and undefined in strict mode.
1. whereas this is equal to the object when called as an object method.
1. as a constructor
1. call and apply
1. bound functions
1. as dom event handler

**Explain how prototypal inheritance works**

Whenever a function is created, its prototype property is also created according to a specific set of rules. 
When it comes to inheritance, JavaScript only has one construct: objects. Each object has an internal link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. null, by definition, has no prototype, and acts as the final link in this prototype chain.

**What do you think of AMD vs CommonJS?**

**Explain why the following doesn't work as an IIFE: `function foo(){ }();`.**
  * What needs to be changed to properly make it an IIFE?

The most widely accepted way to tell the parser to expect a function expression is just to wrap in in parens, because in JavaScript, parens can’t contain statements. At this point, when the parser encounters the function keyword, it knows to parse it as a function expression and not a function declaration.

**What's the difference between a variable that is: `null`, `undefined` or undeclared?**
  * How would you go about checking for any of these states?

The undefined variable is a declared but has a value of undefined. To use a undeclared variable will cause an error.

**What is a closure, and how/why would you use one?**

Closures are functions that have access to variables from anthor function's scope. This is often accomplished by creating a function inside a function.

**What's a typical use case for anonymous functions?**

1. event handler
1. IIFE

**How do you organize your code? (module pattern, classical inheritance?)**

The module pattern use an anonymous function that returns a object. 
Inside of the anonymous function, the private variables and functions are defined first.
After that, an object literal is returned as the function value. That object literal contains only properties and methods that should be public. Since the object is defined inside the anonymous function, all of the public methods have access to the private variables and functions.

**What's the difference between host objects and native objects?**

1. Native objects are those objects supplied by JavaScript. Examples of these are String, Number, Array, Image, Date, Math, etc.
2. Host objects are objects that are supplied to JavaScript by the browser environment. Examples of these are window, document, forms, etc.

**Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?**

**What's the difference between `.call` and `.apply`?**

These methods both call the function with a specific this value. The *apply()* method accepts two arguments: the value of this and an array of arguments. The *call()* method has the same behavior as apply(), but arguments are passed to it differently. Using call() arguments must be enumerated specifically.

**Explain `Function.prototype.bind`.**

ECMAScript 5 defines an addition method called 'bind()'. The 'bind()' method create a new function instance whose this value is bound to the value to that was passed into 'bind()'.

**When would you use `document.write()`?**

**What's the difference between feature detection, feature inference, and using the UA string?**

Feature Detection is to identify the browser's capabilities.
Feature Inference is guess whether browser has certain feature through others feature or UA string.
One inappropriate use of feature detection is called feature inference. Feature inference attempts to use multiple features after validating the presence of only one. The presence of one feature is inferred by the presence of another. The problem is, of course, that inference is an assumption rather than a fact, and that can lead to maintenance issues.
UA String is User-Agent Detection.

**Explain AJAX in as much detail as possible.**

AJAX is short for Asynchronous Javascript + XML. The technique consisted of making server requests for additional data without reloading web page, as a result we have a better user experience.

**Explain how JSONP works (and how it's not really AJAX).**

**Have you ever used JavaScript templating?**
  * If so, what libraries have you used?

Handlebars, _.tmpl, $.tmpl, skim

**Explain "hoisting".**

There is a preproccess or precompile in javascript runtime. and 'Hoisting' occur in the preproccess.

Function declarations and variable declarations are always moved (“hoisted”) invisibly to the top of their containing scope by the JavaScript interpreter. This means that code like this:

```javascript
function foo() {
    bar();
    var x = 1;
}
```

is actually interpreted like this:

```javascript
function foo() {
    var x;
    bar();
    x = 1;
}
```

**Describe event bubbling.**

1. Event Flow describes the order in which events are received on the page. An event has three phases of its life cycle: capture, target, and bubbling.
2. Event Bubbling mean that an event start at the most specific element (the deepest possible point to the document tree) and then flow upward toward the least specific node (the document);

**What's the difference between an "attribute" and a "property"?**

Often an attribute is used to describe the mechanism or real-world thing.

A property is used to describe the model.

In HTML / Javascript the terms get confused because DOM Elements have attributes (per the HTML source) which are backed by properties when those elements are represented as Javascript objects.

To further confuse things, changes to the properties can sometimes update the attributes.

For example, changing the element.href property will update the href attribute on the element, and that'll be reflected in a call to element.getAttribute('href').

However if you subsequently read that property, it will have been normalised to an absolute URL, even though the attribute might be a relative URL!

**Why is extending built-in JavaScript objects not a good idea?**

Depend on the way of extending.

**Difference between document load event and document ready event?**

1. ready means DOM is ready.
1. load means the page fully loaded. Includes inner frames, images etc.

**What is the difference between `==` and `===`?**

The == operator will compare for equality after doing any necessary type conversions. The === operator will not do the conversion, so if two values are not the same type === will simply return false. It's this case where === will be faster, and may return a different result than ==. In all other cases performance will be the same.

**Explain the same-origin policy with regards to JavaScript.**

**Make this work:**
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
function duplicate(collection) {
  return collection.concat(collection);
}
```

**Why is it called a Ternary expression, what does the word "Ternary" indicate?**

**What is `"use strict";`? what are the advantages and disadvantages to using it?**

**Create a for loop that iterates up to `100` while outputting "fizz" at multiples of `3`, "buzz" at multiples of `5` and "fizzbuzz" at multiples of `3` and `5`**

**Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?**

**Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?**

**Explain what a single page app is and how to make one SEO-friendly.**

**What is the extent of your experience with Promises and/or their polyfills?**

**What are the pros and cons of using Promises instead of callbacks?**

**What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?**

**What tools and techniques do you use debugging JavaScript code?**

**What language constructions do you use for iterating over object properties and array items?**

**Explain the difference between mutable and immutable objects.**
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?

**Explain the difference between synchronous and asynchronous functions.**

**What is event loop?**
  * What is the difference between call stack and task queue?

#### Testing Questions:

**What are some advantages/disadvantages to testing your code?**

**What tools would you use to test your code's functionality?**

**What is the difference between a unit test and a functional/integration test?**

**What is the purpose of a code style linting tool?**

#### Performance Questions:

**What tools would you use to find a performance bug in your code?**

**What are some ways you may improve your website's scrolling performance?**

**Explain the difference between layout, painting and compositing.**

#### Network Questions:

**Traditionally, why has it been better to serve site assets from multiple domains?**

**Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.**

**What are the differences between Long-Polling, Websockets and Server-Sent Events?**

**Explain the following request and response headers:**
  * Diff. between Expires, Date, Age and If-Modified-...
  * Do Not Track
  * Cache-Control
  * Transfer-Encoding
  * ETag
  * X-Frame-Options

**What are HTTP actions? List all HTTP actions that you know, and explain them.**

#### Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
```

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

#### Fun Questions:

**What's a cool project that you've recently worked on?**

**What are some things you like about the developer tools you use?**

**Do you have any pet projects? What kind?**

**What's your favorite feature of Internet Explorer?**

**How do you like your coffee?**


#### Contributors:

This document started in 2009 as a collaboration of [@paul_irish](https://twitter.com/paul_irish) [@bentruyman](https://twitter.com/bentruyman) [@cowboy](https://twitter.com/cowboy) [@ajpiano](https://twitter.com/ajpiano)  [@SlexAxton](https://twitter.com/slexaxton) [@boazsender](https://twitter.com/boazsender) [@miketaylr](https://twitter.com/miketaylr) [@vladikoff](https://twitter.com/vladikoff) [@gf3](https://twitter.com/gf3) [@jon_neal](https://twitter.com/jon_neal) [@sambreed](https://twitter.com/sambreed) and [@iansym](https://twitter.com/iansym).

It has since received contributions from over [100 developers](https://github.com/h5bp/Front-end-Developer-Interview-Questions/graphs/contributors).
