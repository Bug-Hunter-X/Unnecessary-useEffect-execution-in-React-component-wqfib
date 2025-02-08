# Unnecessary useEffect Execution in React

This example demonstrates an inefficient use of the `useEffect` hook in React. The effect function logs a message to the console after every render, even when the `count` value hasn't changed.  This can lead to performance issues in larger applications.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console logs after clicking the increment button repeatedly. You will see the message logged for each click, even when the count updates with the same value.

## Solution
The solution uses the optional dependency array in the `useEffect` hook to only trigger the effect when the `count` variable changes.