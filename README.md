# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop within the `useEffect` hook.  The `useEffect` hook is incorrectly configured, leading to the `count` state being continuously updated, causing an infinite render loop.

## Bug Description
The bug occurs because the `count` state is included in the dependency array of the `useEffect` hook. Each time the `count` state changes (which happens when the `useEffect` hook runs), the hook runs again, triggering a new state update. This creates a feedback loop that never ends.

## Solution
The solution is to fix the dependency array in the `useEffect` hook. By removing `count` from the dependency array, the `useEffect` will only run once after the initial render.

## How to Reproduce
Clone this repository and run `npm install` to install the necessary dependencies. Then, run `npm start` to start the development server. You'll observe the counter incrementing indefinitely in the browser.