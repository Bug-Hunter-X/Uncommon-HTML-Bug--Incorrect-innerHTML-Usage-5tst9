# Uncommon HTML Bug: Incorrect innerHTML Usage

This repository demonstrates a subtle bug that can occur when using innerHTML to modify the content of an HTML element.  The issue arises from the unexpected behavior when appending a complete HTML element using `innerHTML +=`. This can lead to unexpected behavior and, in more complex scenarios, potential XSS vulnerabilities.

## Bug Description
The bug involves incorrectly appending an entire `<div>` element using `innerHTML +=`. This will overwrite the content within the div that is already there.

## Solution
Instead of using `innerHTML`, use `insertAdjacentHTML` or DOM manipulation methods such as `appendChild` for a safer and more predictable outcome. This method allows us to selectively add and preserve parts of the original HTML.