# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  An infinite loop occurs because a dependency is missing from the `useEffect` dependency array, causing the effect to run repeatedly.

## The Bug
The `bug.js` file contains a component with a `useEffect` hook that logs the current count. However, it's missing the `count` variable in its dependency array. This means the effect runs after *every* render, causing an infinite loop and potentially crashing the application or significantly impacting performance.

## The Solution
The `bugSolution.js` file shows the corrected code. By including `count` in the dependency array, the effect only runs when the `count` variable changes, resolving the infinite loop. 

## How to Reproduce
1. Clone this repository.
2. Open `bug.js` to see the buggy code.
3. Open `bugSolution.js` to see the corrected code.
4. Run the component and observe the difference in behavior. The buggy version will cause your console to fill rapidly.