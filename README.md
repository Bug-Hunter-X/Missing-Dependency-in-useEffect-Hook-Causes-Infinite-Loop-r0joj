# React useEffect Hook with Missing Dependency

This repository demonstrates a common error in React applications: forgetting to include necessary dependencies in the `useEffect` hook. This can lead to unexpected behavior, such as infinite re-renders and performance issues.

The `bug.js` file contains the buggy code.  The `bugSolution.js` file shows the corrected version.

## Problem

The original component uses the `useEffect` hook to log the current `count` value to the console.  However, `count` is not specified in the dependency array `[]`. This means that the effect runs after every render, regardless of whether `count` has changed.  The effect itself triggers a re-render by logging to the console, creating an infinite loop.

## Solution

The correct approach is to include `count` in the dependency array. This ensures that the effect runs only when the value of `count` changes.  