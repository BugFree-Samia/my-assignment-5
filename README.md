### Question NO 1 : What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
### Answer :
- `getElementById` is used to select a single HTML element by its ID. It only works for one element because ID should be unique.

- `getElementsByClassName` selects all elements with the same class name we used . It returns a collection of elements, not just one because we can use same class name many times.

- `querySelector` lets us use CSS selectors to get the first matching element (like `.class`, `#id`, or `div p`).

- `querySelectorAll` is like `querySelector`, but it returns all matching elements as a list, not just the first one.Returns a NodeList (which is like an array, but not exactly the same).\



### Question NO 2 : How do you create and insert a new element into the DOM?

### Answer :
To create and insert a new element in the DOM, I use JavaScript.

- First, I use `document.createElement()` to make a new element.
- Then I set its content or attributes (like innerText, className).
- After that, I insert it using `appendChild()`, `prepend()`, or `append()` into a parent element.

**Example:**

```javascript
const newDiv = document.createElement("div");
newDiv.innerText = "Hello, this is a new div!";
document.body.appendChild(newDiv);
```
### Question NO 3. What is Event Bubbling and how does it work?

### Answer :
Event Bubbling is a behavior in JavaScript where an event starts from the element that was actually clicked (called the target) and then moves upward through its parent elements in the DOM tree.

**How it works:**
1. Suppose there is a `<button>` inside a `<div>`.
2. If I click the button, the event will first trigger on the button itself.
3. Then it will bubble up to the `<div>`.
4. After that, it goes to `<body>`, then `<html>`, and so on.

This is useful when we want to handle events at a higher level instead of adding event listeners to every small element.
###  Question NO 4. What is Event Delegation in JavaScript? Why is it useful?
### Answer:
Event Delegation is a JavaScript technique where instead of adding event listeners to multiple child elements, you add a single event listener to a parent element and handle events for the children using `event.target`. 
**It's useful because:**

-  Better performance.
-  Works with dynamically added elements.
-  Cleaner and more maintainable code.

### Question NO 5. What is the difference between preventDefault() and stopPropagation() methods?
### Answer :

The difference between `preventDefault()` and `stopPropagation()` methods are given below:

**preventDefault()**
- Prevents the browser's default behavior for an event.
- Stops actions like submitting a form, following a link, etc.

**stopPropagation()**
- Stops the event from bubbling up to parent elements.
- The event stays on the current element only and does not affect its ancestors.

