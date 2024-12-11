# CSS `calc()` Pitfalls

This repository demonstrates two uncommon issues that can arise when using the `calc()` function in CSS: problems related to percentage calculations and operator precedence. The `bug.css` file shows code exhibiting these issues, while `bugSolution.css` presents corrected versions.

## Issue 1: Percentage and Fixed Unit Calculation Errors

When using percentages alongside fixed units (like `px` or `em`) in `calc()`, the context in which the percentage is resolved is crucial. If the containing element's width is indeterminate, percentage calculations can become unreliable and lead to unpredictable results.  This is addressed by ensuring proper context is set within the hierarchy.

## Issue 2: Operator Precedence Problems in `calc()`

The `calc()` function adheres to standard mathematical operator precedence (multiplication before addition). Overlooking this can lead to incorrect calculations. Using parentheses to force the desired order of operations is vital to preventing unexpected results.

## Solutions

The `bugSolution.css` file illustrates how to correct these issues.  Issue 1 is tackled by setting appropriate widths to allow percentage-based calculations to work correctly. Issue 2 is solved by using parentheses for explicit operator precedence control. 

This example highlights the importance of understanding the nuances of `calc()` to avoid hidden bugs in your CSS.