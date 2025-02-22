# React Router Nested Route Bug

This repository demonstrates a common issue encountered when using nested routes in `react-router-dom`.  The problem arises from incorrectly defining nested routes where a parent route's path is a prefix of its child's path. This can cause unexpected behavior where the nested route is never rendered.

## Problem Description

The provided `bug.js` file shows an example of such an issue. The route `/about` and `/about/*` will conflict. The `/about` route will always take precedence.

## Solution

The `bugSolution.js` file provides a corrected version. It uses more precise path matching to ensure that each route is handled correctly, thereby resolving the issue of incorrect path matching for nested routes.  This approach makes sure that `/about` and `/about/nested` routes are handled appropriately.