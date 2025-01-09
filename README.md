# HTML DOM Element Access Before Load

This repository demonstrates a common yet subtle bug in HTML: attempting to access a DOM element before the browser has fully loaded it. This can result in unexpected errors and crashes, especially when dealing with asynchronous operations.

## Bug Description

The `bug.html` file contains code that attempts to access the `innerHTML` of a div element before the browser's DOM is fully ready.  This frequently leads to a `TypeError: Cannot read properties of null (reading 'innerHTML')` because `document.getElementById('myDiv')` will return `null`. 

## Solution

The `bugSolution.html` file demonstrates the correct approach using the DOMContentLoaded event listener or using a combination of load and DOMContentLoaded event listeners to resolve this issue.  This ensures that the script runs only after the element is fully available.