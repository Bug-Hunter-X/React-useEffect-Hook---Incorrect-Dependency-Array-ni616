# React useEffect Hook - Incorrect Dependency Array

This repository demonstrates a common bug in React's `useEffect` hook where the dependency array is incorrectly specified, leading to unexpected behavior.  The example shows a counter that should increment every second but fails to do so after the initial render.

## Bug Description
The provided `useEffect` hook has an empty dependency array `[]`. This means the effect runs only once after the component mounts.  The `setInterval` function is set up, but the interval is never cleared correctly. To solve this, add `count` to the dependency array.