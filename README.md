# Uncommon DOM Manipulation Bug in HTML

This repository demonstrates a subtle bug related to DOM manipulation in HTML and JavaScript. The bug arises from attempting to access and modify a newly created element's properties before it's properly appended to the DOM. 

## Bug Description
The `bug.html` file contains a script that dynamically creates a `div` element, sets its `innerHTML`, and then immediately tries to access and style a child element (`h1`).  This will result in an error because the element is not yet part of the page's rendered structure.

## Solution
The `bugSolution.html` file presents a corrected version. The styling of the `h1` element is now performed *after* the new `div` is added to its parent in the DOM, ensuring that the element exists in the DOM before manipulation.