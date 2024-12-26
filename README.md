# React useEffect Cleanup Function Missing Return Statement

This repository demonstrates a common error in React's `useEffect` hook: omitting the return statement for the cleanup function.  This can lead to memory leaks and unexpected behavior when the component unmounts.

## Bug

The `bug.js` file shows an example where an event listener is added in `useEffect` without a corresponding cleanup function. When the component unmounts, the event listener remains active, potentially causing issues.

## Solution

The `bugSolution.js` file demonstrates the correct way to implement `useEffect` with a cleanup function.  The return statement of the `useEffect` callback provides a function that will remove the event listener when the component is unmounted, preventing memory leaks.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies (if necessary).
3. Run `npm start` to start the development server and open the bug and solution examples in separate tabs.
4. Note the behavior difference between the bug and solution examples.

## Learning points

* Always include a cleanup function in `useEffect` when adding event listeners, timers, or any other resources that need to be released.
* The cleanup function is crucial for preventing memory leaks and ensuring that your component behaves as expected when it unmounts.