# React useEffect Dependency Issue

This repository demonstrates a common mistake when using the `useEffect` hook in React: incorrectly specifying dependencies, leading to unexpected behavior.

The `bug.js` file contains the erroneous code.  The `useEffect` hook's dependency array includes `count`, but the conditional logic inside the effect (`if (count)`) doesn't correctly handle the initial render where `count` is 0. This causes the `console.log` to run even when the count hasn't actually changed.

The `bugSolution.js` file shows the corrected code.  The issue is resolved by removing the unnecessary condition or handling the initial render case appropriately.