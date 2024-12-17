# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite render loop. The bug is caused by missing a dependency array in the useEffect, resulting in the effect running after every render.

## Bug Description
The `MyComponent` component uses `useState` to track a count. The `useEffect` hook logs the current count to the console.  Without a dependency array, the effect runs on every render, leading to an infinite loop of console logs and potentially performance issues.

## Solution
The solution is to add a dependency array to the `useEffect` hook, specifically including the `count` variable.  This ensures that the effect only runs when the `count` variable changes.

## How to reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite console logs in your browser's developer console.
5. Examine the corrected code in `bugSolution.js` to see how to fix the issue.
