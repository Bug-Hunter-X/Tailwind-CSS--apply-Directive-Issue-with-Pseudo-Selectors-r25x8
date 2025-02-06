# Tailwind CSS @apply Directive Issue with Pseudo-Selectors

This repository demonstrates a bug where Tailwind's `@apply` directive fails to correctly apply styles when a class includes a pseudo-selector such as `&:hover` or `&:focus`.  The issue is that while `@apply` works as expected for regular classes, it doesn't seem to expand and correctly inject styles for pseudo-classes.

## Bug Description

The `@apply` directive, while efficient for applying multiple utility classes, falls short when dealing with styles defined for pseudo-selectors.  The resulting styles are not applied to the intended elements under the specified conditions (hover, focus, etc.).

## Solution

The solution involves using regular class application instead of the `@apply` directive for classes containing pseudo-selectors.   This ensures that styles are correctly applied based on their intended conditions.

## How to reproduce

1. Clone this repository.
2. Open `bug.html` in your browser.
3. Observe that hover and focus styles are not applied correctly.
4. Open `bugSolution.html` to see the corrected version.