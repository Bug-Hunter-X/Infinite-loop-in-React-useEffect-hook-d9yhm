# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from an infinite loop caused by a missing or incomplete dependency array. 

## Problem
The `useEffect` hook in the provided `MyComponent` runs after every render because the dependency array `[count]` is missing. This leads to an infinite render loop, as updating the `count` triggers the effect, which updates the `count` again.  This results in very high CPU usage and can crash the browser.

## Solution
The solution is to correctly specify the dependency array to include all variables from the component's scope that the effect depends on.  In this case, only `count` is needed, ensuring the effect runs only when `count` changes.

## How to run
1. Clone this repo
2. Navigate to the project directory
3. Run `npm install`
4. Run `npm start`
