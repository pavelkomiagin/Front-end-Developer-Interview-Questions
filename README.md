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

Mac OS X (or Ubuntu), Webstorm, zsh, Chrome, dev tools, git, node

**Which version control systems are you familiar with?**

Git, Mercurial, SVN

**Can you describe your workflow when you create a web page?**

1. study prototype
1. set structures(html tag)
1. render with style
1. add interactive by scripts

**If you have 5 different stylesheets, how would you best integrate them into the site?**

I'd combine them in one style file and minify.

**Can you describe the difference between progressive enhancement and graceful degradation?**

1. *Graceful degradation*. Providing an alternative version of your functionality or making the user aware of shortcomings of a product as a safety measure to ensure that the product is usable.

1. *Progressive enhancement*. Starting with a baseline of usable functionality, then increasing the richness of the user experience step by step by testing for support for enhancements before applying them.

I agree with progressive enhancement, and increasing user experience with feature detection. For example, once I detected that the browser support round-corner or shadow text, I will apply this features to pages.

**How would you optimize a website's assets/resources?**

1. File concatenation
1. File minification
1. CDN Hosted
1. Caching
Combine and minify all js files in one file. Do the same for styles. Combine images in sprites

**How many resources will a browser download from a given domain at a time?**
  * What are the exceptions?

Multiple domains could increase the number of parallel downloads that the browser can perform.

About 4 to 6 connections per domain

Not all browsers are restricted to just two parallel downloads per hostname. Opera 9+ and Safari 3+ do four downloads per hostname. Internet Explorer 8, Firefox 3, and Chrome 1+ do six downloads per hostname. Sharding across two domains is a good compromise that improves performance in all browsers.

The optimal number of domains to shard across is 2-4. After 4 domains, response time degrades.

**Lets say your google.com homepage is loading slowly how would you start addressing the problem?**

1. Optimize Image Size and Format
The images on your site can take up a lot of bandwidth, which affects the loading time of your page. It is not enough to downsize your website’s images in HTML because that only changes the appearance of the image and not its actual size. Use external picture editor tools to resize the images, such as Photoshop.
Additionally, use image optimization tools which further compress the image to reduce its size:

- JPEG & PNG Stripper
- Smush.it
- Online Image Optimizer
- SuperGIF

For optimized loading time of your page it is ideal to stick to standard image formats such as JPG, PNG and GIF.

2. Avoid Inline JS and CSS files
It is a good practice to place your website’s JS and CSS in external files. When the page loads the browser caches these files externally and reduces the page load time on subsequent requests. Moreover, having the JS and CSS files externally allows for easier site maintenance.

3. Optimize Caching
Every time a visitor loads a site, your web page’s image files, CSS and Javascript files load as well, taking up a lot of page load time. When caching is set up correctly, your browser can store these resources or files for subsequent requests. On repeated page loads these files can be retrieved from the cache rather than downloading them all over again from the network. This also reduces bandwidth and hosting costs.
You can use Expires headers for static components of the site and Cache-Control headers for dynamic ones. Using these headers makes the various components of a site, including images, stylesheets, scripts and flash, cacheable. This in turn minimizes HTTP requests and thus improves the page load time. With the use of Expires headers you can actually control the length of time that components of a web page can be cached, as shown in the example below:
     Expires: Wed, 20 Apr 2015 20:00:00 GMT
If your server is Apache you can set the time for cached content by using the ExpiresDefault directive. This sets the expiration date as a certain number of years from the current date:
     ExpiresDefault “access plus 15 years”

4. Avoid render blocking scripts
Place javascript files at the end of the body or use the 'async' attribute to load them asynchronously.

5. Avoid Redirects
Avoiding redirects increases serving speed. Some redirects are unavoidable and need to be in place but you must remember that this requires an additional HTTP which increases the page load time. Check for broken links and fix them immediately.

6. Set up G-Zip Encoding
Similar to files on your PC that are zipped and compressed to reduce the total size during online file transfers, heavy files on your website can be zipped with something called the G-Zip Compression. This saves bandwidth and download time and reduces your page loading speed. You should configure the server so that it returns zipped content.

7. Reduce HTTP Requests
Use CSS Sprites to reduce the number of image requests. Combine background images into a single image by using CSS background-image and background-position elements. Combine inline images into your cached stylesheets. Likewise, combine all your javascript files into a single file and all your CSS files as well.

8. Minification of JavaScript and CSS
Minification is the process of compressing the code by renaming variables to shorter names which helps to reduce its size and the subsequent loading time. We recommend using uglify.js for this.

9. Reduce Cookie Size
Cookies are used to store data that needs to persist between requests. This data is sent on every request and adds to the load time when it’s big. Hence, by reducing the size of the cookies you reduce the size of the data that is transferred and decrease the page load time. Eliminate unnecessary cookies or reduce the size of the cookies.

**If you jumped on a project and they used tabs and you used spaces, what would you do?**

1. Suggest the project utilize something like EditorConfig (http://editorconfig.org)
1. Conform to the conventions (stay consistent)

I will setup my environment for using tabs because it's important to have the same settings for it in the team.

**Describe how you would create a simple slideshow page.**

I would create several blocks - left arrow, middle blocks for slides and right arrow. Then I would add click listeners on the arrows to decrease or increase the number of current slide and show html bolck with current slide number.

**If you could master one technology this year, what would it be?**

Ruby On Rails. For a good job.

**Explain the importance of standards and standards bodies.**

**What is Flash of Unstyled Content? How do you avoid FOUC?**

**Explain what ARIA and screenreaders are, and how to make a website accessible.**

We should add aria-attributes in out html to help screenreaders detect what part of site or what element is it.

**Explain some of the pros and cons for CSS animations versus JavaScript animations.**

CSS animations faster but less controled.

**What does CORS stand for and what issue does it address?**

**On which port HTTP runs?**

By default HTTP uses port 80 and HTTPS uses port 443

**SSL full form**

Secure Sockets Layer

#### HTML Questions:

**What does a `doctype` do?**

Instruct the browser to render the page.

**What's the difference between standards mode and quirks mode?**

Obviously,the css box model.

**What's the difference between HTML and XHTML?**

**Are there any problems with serving pages as `application/xhtml+xml`?**

**How do you serve a page with content in multiple languages?**

Use i18n framework.

**What kind of things must you be wary of when design or developing for multilingual sites?**

**What are `data-` attributes good for?**

The W3C specification for data-attributes states that:

Custom data attributes are intended to store custom data private to the page or application, for which there are no more appropriate attributes or elements.
Custom data- attributes are a great way to simplify the storage of application data in your web pages.

**Consider HTML5 as an open web platform. What are the building blocks of HTML5?**

1. more semantic text markup
1. new form elements
1. video and audio
1. new javascript API
1. canvas and SVG
1. new communication API
1. geolocation API
1. web worker API
1. new data storage

**Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.**

Now there are such way to keep data on front-end side.

1. HTML5 local Storage
1. HTML5 session storage
1. HTML5 web database
1. Cookies
2. 
localStorage - stores data with no expiration date sessionStorage - stores data for one session

HTML5 web storage = generic umbrella term for the new client-side data storage options:

1. Web Storage is more secure and faster. The data is not included with every server request, but used ONLY when asked for. It is also possible to store large amounts of data, without affecting the website's performance.
1. Local Storage = persistant and scoped to the domain(store data with no expiration date). At the moment two flavors are usually mentioned:
'default' = stores things in name/value pairs
Web SQL (aka Web Database) = uses a SQL database
1. Session Storage = non persistent and scoped only to the current window(stores data for one session)

Cookies = the old school way of doing all of the above. Stores name/value pairs per domain.

**Describe the difference between `<script>`, `<script async>` and `<script defer>`.**

**Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?**

It's a good idea because when we put our js script tag to the end of <body> tag, browser dont't wait while js file will be loaded. Browser can render page without it. But we should place <link> tag inside <head> because in this case browser will not be render page before styles will be full loaded.

**What is progressive rendering?**

**Have you used different HTML templating languages before?**

Slim, Skim, PHP templating.

#### CSS Questions:

**What is the difference between classes and ID's in CSS?**

**What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?**

1. *What Is A CSS Reset?*.
A CSS Reset (or “Reset CSS”) is a short, often compressed (minified) set of CSS rules that resets the styling of all HTML elements to a consistent baseline. In a word,reset.css is used to normalize browser's default styles.
Why USE A CSS Reset? 
Browser have different "built-in" styles which they apply to different html-elements. These styledefinitions may vary accross different browsers.
Which CSS Reset Should I Use?

1. *Normalize.css* is a customisable CSS file that makes browsers render all elements more consistently and in line with modern standards.
If you’re working with HTML5, use the HTML5 Doctor Reset CSS
If you’re doing some quick prototyping and testing, or building a non-HTML5 page, use Eric Meyer’s Reset CSS.
If you want a CSS Reset that acts more as a framework, un-resetting styles after the CSS Reset, use the Tripoli CSS Reset or the Vanilla CSS Un-Reset
If you want a full-featured CSS Framework, try using and abusing all the modules of the YUI 3 CSS Library
Generally speaking, don’t use the Universal Selector ‘*’ CSS Reset

**Describe Floats and how they work.**

A float element in page like a boat in water.

**Describe z-index and how stacking context is formed.**

**Describe BFC(Block Formatting Context) and how it works.**

**What are the various clearing techniques and which is appropriate for what context?**

1. *The Empty Div Method* is, quite literally, an empty div. <div style="clear: both;"></div>. Sometimes you'll see a <br /> element or some other random element used, but div is the most common because it has no brower default styling, doesn't have any special function, and is unlikely to be generically styled with CSS. This method is scorned by semantic purists since its presence has no contexual meaning at all to the page and is there purely for presentation. Of course in the strictest sense they are right, but it gets the job done right and doesn't hurt anybody.
1. *The Overflow Method* relies on setting the overflow CSS property on a parent element. If this property is set to auto or hidden on the parent element, the parent will expand to contain the floats, effectively clearing it for succeeding elements. This method can be beautifully semantic as it may not require an additional elements. However if you find yourself adding a new div just to apply this, it is equally as unsemantic as the empty div method and less adaptable. Also bear in mind that the overflow property isn't specifically for clearing floats. Be careful not to hide content or trigger unwanted scrollbars.
1. *The Easy Clearing Method* uses a clever CSS pseudo selector (:after) to clear floats. Rather than setting the overflow on the parent, you apply an additional class like "clearfix" to it. Then apply this CSS:

```css
    .clearfix:after {       
        content: ".";       
        visibility: hidden;       
        display: block;       
        height: 0;       
        clear: both;
    }
```

This will apply a small bit of content, hidden from view, after the parent element which clears the float. This isn't quite the [whole story](http://www.positioniseverything.net/easyclearing.html), as additional code needs to be used to accomodate for older browsers.

**Explain CSS sprites, and how you would implement them on a page or site.**

CSS sprites are a way to reduce the number of HTTP requests made for image resources referenced by your site. Images are combined into one larger image at defined X and Y coorindates. Having assigned this generated image to relevant page elements the background-position CSS property can then be used to shift the visible area to the required component image.(Css sprites is a technology to combin many image into one, and use css background-position to find which part you want)

CSS Sprites are the preferred method for reducing the number of image requests. Combine your background images into a single image and use the CSS background-image and background-position properties to display the desired image segment.

**What are your favourite image replacement techniques and which do you use when?**

**How would you approach fixing browser-specific styling issues?**

**How do you serve your pages for feature-constrained browsers?**
  * What techniques/processes do you use?

1. Progressive Enhancement
1. Graceful Degradation

**What are the different ways to visually hide content (and make it available only for screen readers)?**

css media types (http://www.w3.org/TR/CSS2/media.html)

**Have you ever used a grid system, and if so, what do you prefer?**

Of course yes.

1. Bootstrap Grid System
1. Grid960

**Have you used or implemented media queries or mobile specific layouts/CSS?**

**Are you familiar with styling SVG?**

http://www.w3.org/TR/SVG/styling.html

**How do you optimize your webpages for print?**

1. Create A Stylesheet For Print
1. Avoid Unnecessary HTML Tables
1. Hiding Needless Element For Print
1. Size Page For Print
1. Use Page Break

**What are some of the "gotchas" for writing efficient CSS?**

1. Use efficient CSS selectors
  1. Avoid a universal key selector.
  1. Allow elements to inherit from ancestors, or use a class to apply a style to multiple elements.
  1. Make your rules as specific as possible. 
  1. Prefer class and ID selectors over tag selectors.
  1. Remove redundant qualifiers. 
  1. These qualifiers are redundant:
    * ID selectors qualified by class and/or tag selectors
    * Class selectors qualified by tag selectors (when a class is only used for one tag, which is a good design practice anyway).
  1. Avoid using descendant selectors, especially those that specify redundant ancestors. For example, the rule body ul li a {...} specifies a redundant body selector, since all elements are descendants of the body tag.
  1. Use class selectors instead of descendant selectors.
1. Avoid CSS expressions
1. Put CSS in the document head

**What are the advantages/disadvantages of using CSS preprocessors?**
  * Describe what you like and dislike about the CSS preprocessors you have used.

**How would you implement a web design comp that uses non-standard fonts?**

Webfonts (font services like: Google Webfonts, Typekit etc.)  

**Explain how a browser determines what elements match a CSS selector.**

As the browser parses HTML, it constructs an internal document tree representing all the elements to be displayed. It then matches elements to styles specified in various stylesheets, according to the standard CSS cascade, inheritance, and ordering rules. In Mozilla's implementation (and probably others as well), for each element, the CSS engine searches through style rules to find a match. The engine evaluates each rule from right to left, starting from the rightmost selector (called the "key") and moving through each selector until it finds a match or discards the rule. (The "selector" is the document element to which the rule should apply.)

**Describe pseudo-elements and discuss what they are used for.**

**Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.**

All HTML elements can be considered as boxes. In CSS, the term "box model" is used to describe a rectangle params that wraps around HTML elements, and it consists of: margins, borders, padding, and the actual content.

Browsers differ on what should and should not get included in the “content” area. Up for debate is the content itself (words), the padding, the borders, and the margin. As far as I know, everyone agrees that the words should count towards the width, and that the margin should not. But when it comes to the padding and border things are uncertain.

Some browsers (such as Firefox) think the width should only include the the content itself, not the padding, border or margin. Other browsers (such as IE) think the width should include the content, padding, and border, but not the margin. (So far I haven’t found anyone who thinks the padding should be in and the boarder out - they seem to always go as a pair.)

*Important*: When you set the width and height properties of an element with CSS, you just set the width and height of the **content area**. To calculate the full size of an element, you must also add the padding, borders and margins.

The box-sizing CSS property is used to change the default CSS box model used to calculate widths and heights of elements. When we use { box-sizing: content-box; } then size calculates as a content size not including paddings, borders and margins. So when we use { box-sizing: border-box; } then size calculates as a content size including paddings, borders but not margins. And padding-box used for calculating size as content size with paddings but not including borders and margins.

**What does ```* { box-sizing: border-box; }``` do? What are its advantages?**

When we use this rule all html elements will calcultes their size as a content size including paddings, borders but not margins. So if we set width = 100px then it will include paddings and borders.

**List as many values for the display property that you can remember.**

block, inline-block, inline, none, flex, table, table-cell, table-caption.

**What's the difference between inline and inline-block?**

Elements with display: inline-block are elements like display: inline elements, but they can have a width and height. So you can use an inline-block element as a block while flowing it within text.

**What's the difference between a relative, fixed, absolute and statically positioned element?**

There are 4 different types of CSS positioning: Static, Relative, Absolute, and Fixed.

1. **Static position** is the default type of positioning. When elements don’t have a position specifically set, they default to static. There’s not much you can do with a statically positioned element. These elements will stack in a standard one-after-another order. So in your code, whatever comes first will be displayed first, then the next element will be below it, and so on.
1. **Relative Positioning** is more interesting because if you just give an element position:relative it will initially seem to do nothing. In order to see a relatively positioned element move you also need to tell it where to go using one of the following `top: XXX;` `bottom: XXX;` `left: XXX;` `right: XXX;`. When you begin to move around a relatively positioned element, two things happen. First, you will see the element move off from the side specified, so if you wrote `top:50px`; the element will move 50px off from the top, or basically down. When you do this though, it doesn’t effect any other static elements around it. So like above, if there’s a static element below your relative one, and you move the relative element down by 50px, the two will overlap, but there is essentially a placeholder where the relatively positioned div originally was. Again, this means that it does NOT effect any other static elements around it.
2. **An absolutely positioned** element is actually removed from the DOM and positioned based on its nearest relatively positioned parent element. What does this mean?… First off, unlike a relatively positioned element which doesn’t effect other static elements, when you give an element position:absolute its like it no longer exists. This means that other static elements will move up to fill in the space where the absolute element would have been. The position of the absolute element is determined by its parent elements. If all of the parent elements are either static, or there are none, then the element is positioned based on the <body>.
3. **Fixed elements** are completely independent of everything else on the web page. Regardless of any parents, a fixed position element will always be positioned based on the browser window. The interesting thing about fixed position elements is that when the page is scrolled, the element stays “fixed” and is always visible.

**The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?**

**What existing CSS frameworks have you used locally, or in production? How would you change/improve them?**

**Have you played around with the new CSS Flexbox or Grid specs?**

**How is responsive design different from adaptive design?**

**Have you ever worked with retina graphics? If so, when and what techniques did you use?**

**Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?**

#### JS Questions:

**Explain event delegation**

Event delegation is when you bind an event listener to a parent (or ancestor) element rather than the element(s) you are particularly interested in. When the event is triggered you can check the event target to make sure it was actually the triggered on the element of interest. In general this would be inefficient as you’re now listening to events on the parent, and have to filter out any that aren’t on the particular element of interest. However, event delegation is particularly useful when you have many siblings (or decedents of the ancestor) that you’re interested in.

For example we have list with three elements. While it would be possible to bind to the individual li elements it would require 3 listeners. Using event delegation it is possible to bind one event listener to the ul element and just check if the event’s target is an li element.

**Explain how `this` works in JavaScript**

`this` is the context the code is running in. However, the context seems to change a lot. So there are some cases:

1. when used inside global functions, `this` is equal to window in nostrict mode and undefined in strict mode.
2. When call an object method this refers to object
1. when use call or apply, this refers to giving object as parameter.
1. In dom event handler this refers to event object.

**Explain how prototypal inheritance works**

Whenever a function is created, its prototype property is also created according to a specific set of rules. 
When it comes to inheritance, JavaScript only has one construct: objects. Each object has an internal link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. null, by definition, has no prototype, and acts as the final link in this prototype chain.

**What do you think of AMD vs CommonJS?**

**Explain why the following doesn't work as an IIFE: `function foo(){ }();`.**
  * What needs to be changed to properly make it an IIFE?

The most widely accepted way to tell the parser to expect a function expression is just to wrap in in parens, because in JavaScript, parens can’t contain statements. At this point, when the parser encounters the function keyword, it knows to parse it as a function expression and not a function declaration.

**What's the difference between a variable that is: `null`, `undefined` or undeclared?**

1. Variables that are actually 'not defined', i.e. they don't exists as a given name isn't bound in the current lexical environment. Accessing such a variable will throw an error, but using `typeof` won't and will return 'undefined'. In contrast, accessing non-existing properties will not throw an error and return undefined instead (and you may use the `in` operator or the `hasOwnProperty()` method to check if properties actually do exist).

1. Existing variables which have not been assigned a value (which is common because of var hoisting) or which have been explicitly set to undefined. Accessing such a variable will return undefined, typeof will return 'undefined'.

1. Existing variables which have been explicitly set to null. Accessing such a variable will return null, typeof will return 'object'. Note that this is misleading: null is not an object, but a primitive value of type Null (which has the consequence that you can't return null from constructor functions - you have to throw an error instead to denote failure).

*Best practices:*

Use `typeof` to check for undefined, as it will cover the first two cases.

Don't assign `undefined` to properties: Use `delete` to get rid of them instead; note that you cannot delete variables (but also note that globals are actually properties of the global object and thus can be deleted).
Use `null` to mark the absence of a meaningful value (eg the forward reference of the last node of a linked list) or if you want to clear a variable as a hint to the garbage collector.
You could go with undefined for 3. as well and never use `null` at all.

**How would you go about checking for any of these states?**




The undefined variable is a declared but has a value of undefined. To use a undeclared variable will cause an error.

**What is a closure, and how/why would you use one?**

Closures are functions that have access to variables from anthor function's scope. This is often accomplished by creating a function inside a function.

**What's a typical use case for anonymous functions?**

Anonymous functions are typically used as callbacks or as IIFE.

**How do you organize your code? (module pattern, classical inheritance?)**

The module pattern use an anonymous function that returns a object. 
Inside of the anonymous function, the private variables and functions are defined first.
After that, an object literal is returned as the function value. That object literal contains only properties and methods that should be public. Since the object is defined inside the anonymous function, all of the public methods have access to the private variables and functions.

**What's the difference between host objects and native objects?**

1. Native objects are those objects supplied by JavaScript. Examples of these are String, Number, Array, Date, Math, etc.
2. Host objects - everything the environment gives you. For the browser, this includes objects like window. Host objects can differ by environment (or host), so that Node wouldn’t have access to window (which makes sense since there’s no DOM for Node), but could have its own host objects like NodeLists.

**Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?**

1. The first one function `Person(){}` defines a function. Since it’s got a capital letter at the beginning of the function name we expect that it’s a constructor. This is a JS convention.

1. Next `var person = new Person()` is one way to create new objects. Using this method person will have access to everything Person.prototype has access to, as well as any instance variables set in the Person constructor.
    
    `new` does three main things:
    1. new creates a new object. It’s just a plain old, bog standard, nothing-in-it object. It looks like {}. Boring, I know, but it’s very important. *This step (the plain old empty JS object) means that you get a unique “deep copy” (other languages would say “instance”) of the constructor each time it’s run. If new didn’t create a new object then you’d constantly be overwriting things in seemingly different objects.*
    1. The newly created object has it’s prototype set to whatever the Person’s prototype is right now. *This step (setting the prototype) means that you can set methods on the constructor’s prototype and they’ll be available on your new object. Something like this (If lucy’s prototype hadn’t been set to Person’s prototype then the introduce method wouldn’t have been available):*
    ```
    function Person(name) {
        this.name = name;
    }
    Person.prototype.introduce = function() {
        console.log("Hi, my name is " + this.name);
    }
    var lucy = new Person('Lucy');
    lucy.introduce(); // logs out: "Hi, my name is Lucy"
    ```
    1. Finally the constructor function is called (the body of Person) with any references to this replaced with the object created in step 1. *This step (constructor with this set) means that each object’s this points to the object, rather than the window or something else. Without the third step this from the Person constructor wouldn’t work correctly and lucy wouldn’t be able to introduce herself.*

1. Finally `var person = Person()` is a mistake. There are ways of dealing with mistakes like this (my preference is the "use strict" method), but ultimately this should be corrected. *Here we don’t actually have the Person constructor. Without the new keyword from above those three steps won’t happen. Let’s look at what that means step by step. We’re going to use the same example as above, but without the new keyword:*
    ```
    function Person(name) {
        this.name = name;
    }
    Person.prototype.introduce = function() {
        console.log("Hi, my name is " + this.name);
    }
    
    var lucy = Person('Lucy'); // <-- NO NEW KEYWORD
    ```
    **Step 1** (the plain old empty JS object) doesn’t happen. Now instead of getting a new object for lucy all we get is the return value of Person. Which is nothing (a.k.a undefined). Bummer.

    **Step 2** (setting the prototype) doesn't happen. Well that’s kind of a given. Since there’s no new object (see step 1 that didn’t happen) there can’t be a prototype set on it.

    **Step 3** (constructor with this set) tries to happen. It really does it’s very best. Since there’s no new object to set this to, JS does the next best thing and uses the default this, the window. So now there’s a brand new property on the window, and you can call it with window.name or this.name both of which are "Lucy".
    
    We can write logic for detect this situation:
    ```
    function Person(name) {
        if (this instanceof Person) {
            this.name = name;
          } else {
            return new Person(name);
          }
    }
    ```
    
    Or we can use strict mode and in this case error 'Cannot set property 'name' of undefined"' will appear bacause in strict mode this will not be equals `window` but will be equals `undefined`

**What's the difference between `.call` and `.apply`?**

These methods both call the function with a specific `this` value. The `apply()` method accepts two arguments: the value of this and an array of arguments. The `call()` method has the same behavior as `apply()`, but arguments must be separated by comma.

**Explain `Function.prototype.bind`.**

`bind` allows us to set up which object is treated as `this` within the function call. It can be useful when we want to change the context of some function calling.

**When would you use `document.write()`?**

First, what is `document.write()`? 
`document.write()` writes to the document (or web page). It takes the content you want to write as a parameter. An invocation could look like this:
`document.write("<h1>JS is awesome!</h1>");`

*Problems with document.write()*:

It replaced the entire content of the document with the parameter of this function. Obviously that’s a problem right there - `document.write()` shouldn’t be used after the page has loaded to change the content as it will overwrite the entire page (probably not what you wanted to happen...).

`document.write()` doesn’t work for XHTML pages.

*Possible situations to use `document.write()`*

It seems that the only “approved” time to use document.write() is for third party code to be included (such as ads or Google Analytics). Since document.write() is always available (mostly) it is a good choice for third party vendors to use it to add their scripts. They don’t know what environment you're using, if jQuery is or isn’t available, or what your onload events are. And with document.write() they don’t have to.

So don’t use it yourself, unless your working for the third party.

**What's the difference between feature detection, feature inference, and using the UA string?**

Feature Detection is to identify the browser's capabilities.
Feature Inference is guess whether browser has certain feature through others feature or UA string.
One inappropriate use of feature detection is called feature inference. Feature inference attempts to use multiple features after validating the presence of only one. The presence of one feature is inferred by the presence of another. The problem is, of course, that inference is an assumption rather than a fact, and that can lead to maintenance issues.
UA String is User-Agent Detection.

**Explain AJAX in as much detail as possible.**

Asynchronous JavaScript and XML. So how does it work?

After loading, the client uses JavaScript to fire off a request to the server and listens to the response asynchronously. The response that comes back can be XML, but is often other formats, most often JSON.

The bit that makes AJAX so powerful is that it can update the page after it has finished loading. Before AJAX any new content required an entire page refresh, even if it was only a small change. This meant that users had to redownload a page for very little updated content. Using AJAX meant that the front end could change without a full page refresh, thus giving a much faster response time.

Origially AJAX mostly returned HTML/XML snipits and the DOM would get updated with this new code when the AJAX returned. Now, however, it’s more common for AJAX to get data and update the DOM as needed rather than doing a swap.

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

Event bubbling occurs when a user interacts with a nested element and the event propagates up (“bubbles”) through all of the ancestor elements.

Let's imageine that we have button inside several div elements. When a user clicks the button the event first fires on the button itself, then bubbles up to the parent div, and then up to the ancestor div. The event would continue to bubble up through all the ancestors, until it finally reaches the document.

Often we only want the event to trigger on the element itself, without bubbling. For this we should call `event.stopPropagation();`

**What's the difference between an "attribute" and a "property"?**

Often an attribute is used to describe the mechanism or real-world thing.

A property is used to describe the model.

In HTML / Javascript the terms get confused because DOM Elements have attributes (per the HTML source) which are backed by properties when those elements are represented as Javascript objects.

To further confuse things, changes to the properties can sometimes update the attributes.

For example, changing the element.href property will update the href attribute on the element, and that'll be reflected in a call to element.getAttribute('href').

However if you subsequently read that property, it will have been normalised to an absolute URL, even though the attribute might be a relative URL!

**Why is extending built-in JavaScript objects not a good idea?**

We *extend an object* when we add functionality to an object using the `prototype` property. At first glance, this seems like such an awesome feature.

The main argument against doing this is: if, in future, a browser decides to implement its own version of your method, your method might get overridden (silently) and the browser’s implementation (which is probably different from yours) would take over. So not extending in the first place is future proofing your code.

On the another side, if you decide to overwrite the browsers definition, any future developer working on your code won’t know about the change. They'll have a harder time getting up to speed.

Generally it’s safer to move your particular changes into a library (as with underscore.js). That way your particular methods are clearly marked and there’s no chance of conflict.

But...

It might be a good idea to add an extension for functionality that became available in later versions, but isn’t guaranteed to be available in your particular browser. It is called a polyfill.

**Difference between document load event and document ready event?**

`$(document).ready()` fires when the HTML has finished loading. You can’t interact with the DOM before the HTML has finished loading, so we keep all our JS interactions wrapped up in the ready handler.

`window.onload` fires when all of the content (images, scripts, CSS) has finished loading. This can be really slow, so we try not to keep too much here. But it can be useful if you need to work with images of unknown size.

**What is the difference between `==` and `===`?**

The `double equals ==` operator will compare for equality after doing any necessary type conversions. The `triple equals ===` operator will not do the conversion, so if two values are not the same type `triple equals ===` will simply return false. It's this case where `triple equals ===` will be faster, and may return a different result than `double equals ==`. In all other cases performance will be the same.

If the two operands are not of the same type, JavaScript converts the operands then applies strict comparison. If either operand is a number or a boolean, the operands are converted to numbers if possible; else if either operand is a string, the other operand is converted to a string if possible. If both operands are objects, then JavaScript compares internal references which are equal when operands refer to the same object in memory.

The best practice is to use `triple equals ===` always.

**Explain the same-origin policy with regards to JavaScript.**

The same-origin policy helps prevent malicious attacks by stopping code from another site executing on your site. An attacks like this is known as a Cross Site Scripting attack.

How does JS decide if it’s a “same” site?

The “origin” is the same if three things are the same: the protocol (http vs. https), the domain (subdomain.yoursite.com vs. yoursite.com vs. google.com), and the port (:80 vs. :4567). If all three of these line up, then JS views the sites as the same, and code is executed. If any of them are different then the code is marked as potentially malicious and is not run.

Hmmm, if I own “subdomain.yoursite.com” and “yoursite.com” I might want to share resources. This same-origin policy could be really annoying!

It’s possible to work around the subdomain problem. You can change the domain of a page, so it can access it’s parent’s resources:

// in the code on subdomain.yoursite.com
document.domain = "yoursite.com";
There are a couple other pieces to remember about changing the domain (mostly about the port). You can read about them here.

**Make this work:**
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
function duplicate(collection) {
  return collection.concat(collection);
}
```

**Why is it called a Ternary expression, what does the word "Ternary" indicate?**

Let’s answer the second question first: what does the word “ternary” indicate? According to Wikipedia the word “ternary” comes from the n-ary word setup. Other examples of n-ary words are unary and binary. All of these (including ternary) are operands. The prefix section of their name lists how many inputs the operand accepts.

A unary operand accepts one parameter, e.g. -1, where - is the operand, and 1 is the parameter.

A binary operand accepts two parameters, e.g. 2 + 3, where + is the operand, and 2 and 3 are the parameters.

So a ternary operand accepts three parameters.

In programming the ternary operand we use is a rewrite of an if statement. Before we write an actual ternary, we'll just take a quick look at an if statement:

```
if(conditional) { // one
    truethy_block // two
} else {
    falsey_block // three
}
```
You can see there are three sections to an if statement. Let’s write them as a property ternary expression:

`conditional ? truethy_block : falsey_block`
All the same code is there, but it’s arranged slightly differently. The ternary’s operand looks like `?:`.

In JS ternarys are often used for assignment:

```
is_sunny = true;
var weather = is_sunny ? ’sunny' : 'Cloudy';
console.log(weather); // logs ’sunny'
```
They can also be used for very short conditional statements. But be wary of using them for long or complex logic as they are harder to read than traditional statements.

**What is `"use strict";`? what are the advantages and disadvantages to using it?**

If you put "use strict"; at the top of your code (or function), then the JS is evaluated in strict mode. Strict mode throws more errors and disables some features in an effort to make your code more robust, readable, and accurate.

*Advantages*. 
Strict mode helps out in a couple ways:

1. It catches some common coding bloopers, throwing exceptions.
1. It prevents, or throws errors, when relatively “unsafe” actions are taken (such as gaining access to the global object).
1. It disables features that are confusing or poorly thought out.

*Disadvantages*:

I had a harder time finding why people don’t like strict mode. The best explanation I found was when code mixed strict and “normal” modes. If a developer used a library that was in strict mode, but the developer was used to working in normal mode, they might call some actions on the library that wouldn’t work as expected. Worse, since the developer is in normal mode, they don’t have the advantages of extra errors being thrown, so the error might fail silently.

Also, strict mode stops you from doing certain things. People generally think that you shouldn’t use those things in the first place, but some developers don’t like the constraint and want to use all the features of the language.

**Create a for loop that iterates up to `100` while outputting "fizz" at multiples of `3`, "buzz" at multiples of `5` and "fizzbuzz" at multiples of `3` and `5`**

```
for(var i = 1, max = 100; i <= max; i++) {
    if (i % 15 === 0) {
        console.log('fizzbuzz');
        continue;
    }
    if (i % 3 === 0)
        console.log('fizz');
    else if (i % 5 === 0)
        console.log('buzz');
    else console.log(i);
}
```

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
