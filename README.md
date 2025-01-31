# Unnecessary Re-renders in React 19 useEffect Hook

This repository demonstrates a common performance issue in React 19 applications involving the `useEffect` hook. The issue arises when an effect runs after every render, leading to unnecessary re-renders and potential performance degradation.

## Problem Description

The provided `bug.js` file shows a simple counter component where the `useEffect` hook logs the count to the console after each render. While this is a simple example, in real-world applications, such an effect could be performing expensive operations, significantly impacting performance.

## Solution

The `bugSolution.js` file demonstrates the solution by using the optional dependency array in `useEffect`. By specifying the dependency array as `[count]`, the effect only runs when the value of `count` changes.