# Uncommon HTML DOM Access Error

This repository demonstrates an uncommon error that can occur in HTML when accessing DOM elements that may not exist.  The script attempts to modify the `display` style of an element before checking for its existence. This can lead to errors in certain browsers.

## Bug Description

The `bug.html` file contains a script that tries to access and modify the `style` property of the element with the ID `myDiv` without verifying that the element exists. If for some reason, `myDiv` isn't present in the DOM (maybe a dynamic loading issue), this results in an error.

## Solution

The `solution.html` file fixes this by first checking if `document.getElementById('myDiv')` returns a valid element before attempting to modify its style.  This simple check prevents the error from occurring.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in your browser. You should see a console error (depending on the browser).
3. Open `solution.html`. You should see the text but it will be hidden correctly, without any console error.