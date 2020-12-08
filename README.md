# ReactJS_Interview_Questions
React Interview Questions

Q: Can we have multiple stores in redux?
Ans. It is possible to create multiple distinct Redux stores in a page, but the intended pattern is to have only a single store.
Isolating a Redux app as a component in a bigger application, in which case you might want to create a store per root component instance.

Q: How to check if the browser supports HTML5 and Javascript?
Ans. Use a <noscript> tag.This tag will always appear when Javascript is not supported and therefore you can put information within this tag to warn the user to enable Javascript on their browser (if they can).
For HTML5 support : https://www.geeksforgeeks.org/how-to-detect-html-5-is-supported-or-not-in-the-browser/#:~:text=createElement()%20method.,is%20supported%20by%20the%20browser.

Q: What is a mobile-first approach?
Ans: A “mobile-first” approach involves designing a desktop site starting with the mobile version, which is then adapted to larger screens (contrary to the traditional approach of starting with a desktop site and then adapting it to smaller screens).

Q: What happens when we call setState inside Render method?
Ans: render() Calling setState() here makes your component a contender for producing infinite loops. The render() function should be pure, meaning that it does not modify component state, it returns the same result each time it's invoked, and it does not directly interact with the browser.

Q: BrowserRouter VS HashRouter.
Ans: https://www.techblogsnews.com/post/browser-router-vs-hash-router-in-react-js
https://medium.com/@daniel.hramkov/browserrouter-vs-hashrouter-e8bf1c3824ce

Q: Event Bubbling and Capturing.
Ans. https://javascript.info/bubbling-and-capturing
Almost all events bubbles(except focus)

Q: Stop bubbling.
Ans. Any handler may decide that the event has been fully processed and stop the bubbling.
The method for it is event.stopPropagation().
Q: web workers and service workers.
Ans. https://bitsofco.de/web-workers-vs-service-workers-vs-worklets/

Q: What is useMemo?
Ans. React has a built-in hook called useMemo that allows you to memoize expensive functions so that you can avoid calling them on every render. You simple pass in a function and an array of inputs and useMemo will only recompute the memoized value when one of the inputs has changed.

Q: Build your own Redux from Scratch.
Ans. https://redvike.com/build-redux/
 https://codeburst.io/build-your-own-redux-from-scratch-1fb1c348b2f8

Q: Currying in JS.
Ans. Currying is the process of converting a function, that takes multiple arguments at once, to a function that takes these arguments step by step.

Q: Pinch zoom
Ans. A react component that lets you zooming and dragging on any DOM element using multi-touch gestures on mobile devices and mouse-events\wheel on desktop devices. React-quick-pinch-zoom

Q: Redux Principles.
Ans.
Single source of truth. The global state of your application is stored in an object tree within a single store. ...
State is read-only. The only way to change the state is to emit an action, an object describing what happened. ...
Changes are made with pure functions.


Q: Controlled Vs Uncontrolled Components.

Q: debouncing or throttling

Q: react middleware

Q: Promises chaining
Ans. https://javascript.info/promise-chaining
 
Q: Playing around var, let and const.
Ans. https://dandkim.com/js-var-let-const/

Q: why do we use async await?

Q: how is the 'this' keyword of javascript is different from 'this' keyword of java?
Ans. In JavaScript this always refers to the “owner” of the function we're executing, or rather, to the object that a function is a method of.
In Java, this refers to the current instance object on which the method is executed.

Q: Why do we need to bind event handlers in Class Components in React
Ans. While working on React, you must have come across controlled components and event handlers. We need to bind these methods to the component instance using .bind() in our custom component’s constructor.
In Class Components in React, when we pass the event handler function reference as a callback like this
<button type="button" onClick={this.handleClick}>Click Me</button>
the event handler method loses its implicitly bound context. When the event occurs and the handler is invoked, the this value falls back to default binding and is set to undefined , as class declarations and prototype methods run in strict mode.
When we bind the this of the event handler to the component instance in the constructor, we can pass it as a callback without worrying about it losing its context.
Arrow functions are exempt from this behavior because they use lexical this binding which automatically binds them to the scope they are defined in.

Q: Is Javascript Synchronous or Asynchronous?
Ans. JavaScript is synchronous, blocking, single-threaded language. That just means that only one operation can be in progress at a time.

