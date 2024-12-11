# React Router Dom v6 Catch All Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in React Router Dom v6.  The problem is that the catch-all route always triggers, even when other routes should match, effectively overriding any other route defined.

The `App.js` file shows the buggy implementation.  The solution is provided in `AppSolution.js`. The core problem and solution are explained below:

## Problem

The order of routes matters. If a catch-all route (`/*`) is placed before other routes, it will always match first, regardless of whether other routes match, thus preventing other routes from being used.

## Solution

Place the catch-all route at the end of your route definitions in the `Routes` component.  This ensures other routes get a chance to match before the catch-all route takes over.