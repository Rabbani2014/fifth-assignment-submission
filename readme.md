1. What is the difference between **getElementById, getElementsByClassName, and querySelector / querySelectorAll**?
Answer:Difference between **getElementById, getElementsByClassName and querySelector / querySelectorAll**:
Answer: The getElementById() method is used to select a single element based on its unique id attribute. Since an id is meant to be unique within an HTML document, this method always returns a single element object or null if no element with the specified id is found.
Syntax: document.getElementById('my-id');

The getElementsByClassName() method is used to select all elements that have a specific class name. Unlike IDs, multiple elements can share the same class name, so this method returns a collection of elements, specifically a HTMLCollection. This collection is "live," meaning it automatically updates if new elements with the same class are added or removed from the DOM.
Syntax: document.getElementsByClassName('my-class');
querySelector() specificity selects the first element that matches a specified CSS selector and returns a single Element object or null.
Syntax: document.querySelector('selector');

On the other hand,querySelectorAll() selects all elements that match a specified CSS selector.Returns a static NodeList. This collection is a snapshot of the elements at the time of selection and does not update automatically if the DOM changes.
Syntax: document.querySelectorAll('selector');

2.How do you **create and insert a new element into the DOM**? 
Answer:To create and insert a new element into the DOM, we first create the element in memory, then we append it as a child of an existing element in the DOM tree.
We can create a new HTML element using the document.createElement() method. This method takes one argument: a string representing the tag name of the element we want to create (e.g., 'div', 'p', 'span').
After creating and configuring the element, we need to insert it into the DOM tree. This is done by selecting a parent element and then using an append method.
The appendChild() method inserts a new element at the end of the parent element's list of children.The append() method is a more modern alternative that allows us to insert multiple nodes and strings at the end of the parent.

3. What is **Event Bubbling** and how does it work?
Answer:**Event Bubbling** is a concept in the DOM (Document Object Model) event model where an event starts from the target element and then bubbles up through its ancestors (parent, grandparent, etc.) all the way up to the document.
**How does it works**
When an event occurs (like a click):
The event is first triggered on the target element.

Then it "bubbles" up through the parent elements, in order, until it reaches the <html> and document.

4. What is **Event Delegation** in JavaScript? Why is it useful?
Answer:**Event delegation** is a design pattern in JavaScript where a single event handler is placed on a parent element to manage events for its child elements. Instead of attaching a separate event listener to each child, the parent listens for events that bubble up from its children.

**Event delegation is useful for several reasons:**
Improved Performance: Attaching a single event listener to a parent element is more efficient than attaching multiple listeners to numerous child elements. This conserves memory and processing power, especially in applications with a large number of interactive elements.

Simplified Code: It reduces the amount of code needed to manage events. 

Handles Dynamically Added Elements: One of the biggest advantages is that it automatically works for elements added to the DOM after the page has loaded.This is especially useful for dynamic lists or tables.

5. What is the difference between **preventDefault() and stopPropagation()** methods?
Answer: The preventDefault() and stopPropagation() methods in JavaScript event handling serve distinct purposes related to event behavior in the Document Object Model (DOM).
**event.preventDefault():**
This method prevents the default action associated with an event from occurring.
The default action is the browser's built-in behavior for a specific event on an element.
It does not stop the event from bubbling or propagating through the DOM.
**event.stopPropagation():**
This method prevents the event from propagating further up or down the DOM tree .
It stops the event from reaching parent or child elements that might also have event listeners for the same event type.
It does not prevent the default action of the element itself.
