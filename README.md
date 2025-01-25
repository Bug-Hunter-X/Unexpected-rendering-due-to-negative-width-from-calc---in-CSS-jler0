# Unexpected Rendering Due to Negative Width from `calc()` in CSS

This repository demonstrates a common CSS error where the `calc()` function, when used with percentages and fixed values, can lead to negative widths, causing unexpected rendering behavior.  The `bug.css` file shows the erroneous code, and the `bugSolution.css` demonstrates the correction.

## Bug Description

The CSS rule attempts to set the width of an element to `calc(100% - 10px)`. If the parent element's width is smaller than 10px, this will evaluate to a negative value, resulting in the element being hidden or behaving unexpectedly.

## Solution

The solution involves adding a `max-width` to the element to prevent the width from becoming negative.