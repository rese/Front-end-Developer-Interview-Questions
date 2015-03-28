#Front-end Job Interview Questions

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## Table of Contents

  1. [General Questions](#general-questions)
  1. [HTML Questions](#html-questions)
  1. [CSS Questions](#css-questions)
  1. [JS Questions](#js-questions)
  1. [Network Questions](#network-questions)
  1. [Coding Questions](#coding-questions)
  1. [Fun Questions](#fun-questions)

## Getting Involved

  1. [Contributors](#contributors)
  1. [How to Contribute](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/CONTRIBUTING.md)
  1. [License](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/LICENSE.md)

#### General Questions:

* What did you learn yesterday/this week?
* What excites or interests you about coding?
* What is a recent technical challenge you experienced and how did you solve it?
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* Talk about your preferred development environment.
* Which version control systems are you familiar with?
* Can you describe your workflow when you create a web page?
* If you have 5 different stylesheets, how would you best integrate them into the site?
* Can you describe the difference between progressive enhancement and graceful degradation?
* How would you optimize a website's assets/resources?
* How many resources will a browser download from a given domain at a time?
  * What are the exceptions?
* Name 3 ways to decrease page load (perceived or actual load time).
* If you jumped on a project and they used tabs and you used spaces, what would you do?
* Describe how you would create a simple slideshow page.
* What tools do you use to test your code's performance?
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.

#### HTML Questions:

* What does a `doctype` do?
   
      It tells the client how to interpret and render the document
* What's the difference between standards mode and quirks mode?
  
      Quirks mode emulates non-standard behavior to provide support for old browsers so that exisiting content doesn't break. Standards mode emulates what's described in the specifications. Most obvious difference behavior can be seen in the box model.
* What's the difference between HTML and XHTML?

      XHTML is much more strict than HTML (e.g. elements must be properly nested and closed)
* Are there any problems with serving pages as `application/xhtml+xml`?
* How do you serve a page with content in multiple languages?
* What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?

      They can be used to semantically add additional application-specific on the markup.
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.

      All three are client storage solutions. `cookie` is the old school way but the more recent `sessionStorage` and `localStorage` should be used if it's supported. Data in `sessionStorage` is good only for the duration of the session while `localStorage` stores data without an expiration date.
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
   
      The difference lies in when the script is downloaded and executed.
       - `<script>`: Client parses the document. When a script is encountered, parsing is paused to download the file and execute it. Parsing resumes only after execution.
       - `<script async>`: Document is parsed and script is downloaded asynchronously when encountered. Parsing is paused to execute the script when it has been fully downloaded.
       - `<script defer>`: Same as async for the parsing and download portion. Only when parsing has finished will the script be executed even if downloaded finishes before parsing.

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?

      - Script tags are better just before `</body>` because downloading them is a blocking operation and having them near the end of the document prevents flashing the user with a 'white screen'.
      - CSS are better at the `<head>` area so that content is rendered with styling right away.
      
* What is progressive rendering?
    
    A rendering technique to enhance perceived if not actual load time by rendering important parts of the page first and rendering less important ones when they are ready.


#### CSS Questions:

* What is the difference between classes and ID's in CSS?
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* Describe Floats and how they work.
* Describe z-index and how stacking context is formed.
* What are the various clearing techniques and which is appropriate for what context?
* Explain CSS sprites, and how you would implement them on a page or site.
* What are your favourite image replacement techniques and which do you use when?
* How would you approach fixing browser-specific styling issues?
* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
* What are the different ways to visually hide content (and make it available only for screen readers)?
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Any familiarity with styling SVG?
* How do you optimize your webpages for print?
* What are some of the "gotchas" for writing efficient CSS?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* How is responsive design different from adaptive design?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?

#### JS Questions:

* Explain event delegation

    Attaching an event listener to the parent instead of individual nodes (e.g. to the `<ul>` instead of every `<li>`). 
* Explain how `this` works in JavaScript

    `this` is a keyword whose value depends on its context. In the global context for example, `this` refers to the global object. In a function context, the value of `this` depends on how the function was called. In an object context `this` usually refers to the instance of that object.
* Explain how prototypal inheritance works
    
    A prototype acts like a blueprint of an object. In prototypal inheritance, each object has a prototype chain that links it to other objects. Aside from an object's own properties and methods, it also inherits the properties and methods of objects in its prototype chain. When an objects' property or method is referenced, it checks first if it `hasOwnProperty` and uses it if it exisits. If it doesn't the object goes up the prototype chain until one is found or until the chain points to null.
* How do you go about testing your JavaScript?
* What do you think of AMD vs CommonJS?
* Explain why the following doesn't work as an IIFE: `function foo(){ }();`.
    
      It doesn't work because the parser sees it as a function declaration.
  * What needs to be changed to properly make it an IIFE?
      
        Change it to `(function foo(){ })();`
* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?

    - `null` is a value for non-value
    - `undefined` means the variable has been declared but not assigned a value
    - `undeclared` means the variable has not been declared at all and will cause an error
  * How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?

    A function that has access to the scope of another function, usually one declared within another function. Use it to save state for example.
* What's a typical use case for anonymous functions?

    Callbacks, handlers, IIFE
* How do you organize your code? (module pattern, classical inheritance?)
* What's the difference between host objects and native objects?

    Native objects are objects that come with Javascript itself (e.g. String, Number, etc.) while host objects are provided by the browser (e.g. window, form, document)
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* What's the difference between `.call` and `.apply`?

    Both are use to specify the context of `this` but they differ in how arguments are passed. `.apply` arguments are passed as an array while `.call` is comma separated.
* Explain `Function.prototype.bind`.
* When would you use `document.write()`?
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain AJAX in as much detail as possible.

    AJAX is a collection of technologies (HTML, CSS, DOM, JS, etc) that allow you to obtain resources from a server without fully reloading the page.
* Explain how JSONP works (and how it's not really AJAX).
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".

    In javascript, variables and functions are 'hoisted' to the top of the scope by the interpreter. This means that you can use or invoke a variable or function before they have been declared.
* Describe event bubbling.

    When elements are nested and an event is 'triggered', the event moves outward of the nest and executes any handlers for it.
* What's the difference between an "attribute" and a "property"?
* Why is extending built in JavaScript objects not a good idea?
* Difference between document load event and document ready event?

    Document ready means that the document has been parsed and DOM is ready. Document load is triggered when the document is ready and all of its resources downloaded.
* What is the difference between `==` and `===`?

    The latter is more strict in the sense that it also checks for type equality.
* Explain the same-origin policy with regards to JavaScript.

    Mostly for security reasons, it dictates how a resource can interact with another resource depending on their origin.
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What is `"use strict";`? what are the advantages and disadvantages to using it?
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, `"buzz"` at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?

#### Network Questions:

* Traditionally, why has it been better to serve site assets from multiple domains?
* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
* What are the differences between Long-Polling, Websockets and Server-Sent Events?
* Explain the following request and response headers:
  * Diff. between Expires, Date, Age and If-Modified-...
  * Do Not Track
  * Cache-Control
  * Transfer-Encoding
  * ETag
  * X-Frame-Options
* What are HTTP actions? List all HTTP actions that you know, and explain them. 

#### Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```
```javascript
==> '1020'
```

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

```javascript
function add(a, b) {
  if(typeof(b) === 'undefined') {
    return function(n) {
        return a + n;
    }
  }
  
  return a + b;
}
```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

```javascript
===> It's reverse: "goh angasal a m'i"
```

*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
```
```javascript
===> "bar"
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
```javascript
===> "Hello World"
===> Uncaught reference error
```


*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
```javascript
===> 2
```


#### Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Do you have any pet projects? What kind?
* What's your favorite feature of Internet Explorer?
* How do you like your coffee?


#### Contributors:

This document started in 2009 as a collaboration of [@paul_irish](https://twitter.com/paul_irish) [@bentruyman](https://twitter.com/bentruyman) [@cowboy](https://twitter.com/cowboy) [@ajpiano](https://twitter.com/ajpiano)  [@SlexAxton](https://twitter.com/slexaxton) [@boazsender](https://twitter.com/boazsender) [@miketaylr](https://twitter.com/miketaylr) [@vladikoff](https://twitter.com/vladikoff) [@gf3](https://twitter.com/gf3) [@jon_neal](https://twitter.com/jon_neal) [@sambreed](https://twitter.com/sambreed) and [@iansym](https://twitter.com/iansym).

It has since received contributions from over [100 developers](https://github.com/h5bp/Front-end-Developer-Interview-Questions/graphs/contributors).
