# React useEffect Hook Memory Leak

This repository demonstrates a common error in React: forgetting the cleanup function within the `useEffect` hook.  This can lead to memory leaks and unexpected behavior.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected version.

## Problem
The `useEffect` hook in `bug.js` logs a message to the console when the component mounts. However, it's missing a return statement that would normally contain a cleanup function. This means that the component doesn't properly clean up after itself, potentially leading to memory leaks if it is unmounted and re-mounted frequently. 