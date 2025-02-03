# CSS Specificity Gotcha: Unexpected Inheritance Behavior

This repository demonstrates a subtle but important issue related to CSS specificity and inheritance that can lead to unexpected styling behavior.  The problem arises from the order of precedence that CSS uses when multiple selectors apply to the same element.  A seemingly more specific selector might be overridden by a less specific selector due to specificity rules.

## The Problem

The `bug.css` file contains a CSS rule where a selector targeting a `<p>` tag within a `<div>` tag is meant to override a rule targeting all `<p>` tags. However, because of specificity, the more general rule wins.  This demonstrates how specificity, rather than order in the stylesheet, determines which rule is applied.

## The Solution

The `bugSolution.css` file presents a corrected approach using the `!important` flag to properly override the existing style, which is generally discouraged, or by making the overriding style even more specific. 

This example highlights the importance of understanding CSS specificity when troubleshooting unexpected styling outcomes.