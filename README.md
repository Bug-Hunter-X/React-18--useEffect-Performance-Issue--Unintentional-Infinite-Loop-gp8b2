# React 18+ useEffect Performance Issue

This repository demonstrates a common performance issue in React 18 and later versions related to the `useEffect` hook.  The example shows how an `useEffect` hook without a dependency array can cause unexpected behavior and performance problems by running after every render, potentially leading to an infinite loop of updates.

## Problem

The provided `bug.js` demonstrates an `useEffect` hook that's missing an explicit dependency array. This means that React will run this effect after every render. In some cases, this might trigger unnecessary re-renders, leading to performance degradation or unexpected side-effects.

## Solution

The `bugSolution.js` file shows the correct way to fix the issue. The dependency array `[count]` ensures that the effect only runs when the `count` variable changes.