### 6. Answer the following questions clearly:

1. What is the difference between **getElementById, getElementsByClassName, and querySelector / querySelectorAll**?

<!-- Answer to question no.1 -->

**getElementById** selects only one element with the given id. So it returns a single DOM element.
**getElementsByClassName** selects all elements with the given class name. So it returns an HTMLCollection, which means the collection automatically updates as elements are added, removed, or have their class names changed in the document.
***querySelector** selects the first element within a document that matches a specified CSS selector or a group of selectors. It is part of the Document Object Model (DOM), providing a modern and efficient way to interact with HTML elements in web pages.
**querySelectorAll** Selects all elements that match a CSS selector. It utilizes standard CSS selectors to identify elements, allowing for selection based on tag names, class names, IDs, attributes, pseudo-classes, and more complex combinations.



2. How do you **create and insert a new element into the DOM**?

<!-- Answer to question no.2 -->

**Steps:** (1) Use **document.createElement("tag")** to create a new element. (2) Add content with **.textContent, .innerHTML,** or set attributes. (3) Insert into the DOM using: .appendChild(), .append(), .prepend(), .insertBefore()



3. What is **Event Bubbling** and how does it work?

<!-- Answer to question no.3 -->

Event Bubbling is the process where an event starts from the innermost (child) element and then bubbles up to its parent, grandparent, etc. until it reaches the root (document).
**How Event Bubbling Works:**
1. Target Element - When a user interacts with an element (e.g., clicks a button), an event is initially triggered and handled by that target element.
2. Propagation - The event then moves up the Document Object Model (DOM) tree, to its parent, then its grandparent, and so on, like bubbles rising in water.
3. Ancestor Handlers - If there are event listeners attached to these ancestor elements, they are also triggered.
4. Reaching the Root - This process continues until the event reaches the top of the DOM tree, typically the document or <html> element. 



4. What is **Event Delegation** in JavaScript? Why is it useful?

<!-- Answer to question no.4 -->

Event Delegation is a technique where you attach an event listener to a parent element, instead of adding listeners to multiple child elements. When an event happens on a child, the event bubbles up, and the parent can detect which child triggered it (using event.target).
**Why useful?** Because it Saves memory (one listener instead of many). It also works for dynamically added elements which makes it Cleaner and easier to manage.



5. What is the difference between **preventDefault() and stopPropagation()** methods?

<!-- Answer to question no.4 -->

**preventDefault()**
Stops the default action of an element.
Example: Prevents a link from opening or a form from submitting.
**stopPropagation()**
Stops the event from bubbling up to parent elements.
Example: Prevents a click event on a child from triggering parent’s click handler.