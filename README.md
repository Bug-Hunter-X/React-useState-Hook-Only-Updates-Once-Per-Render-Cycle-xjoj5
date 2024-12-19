# React useState Hook - Unexpected Single Update

This repository demonstrates a common issue with React's `useState` hook:  multiple calls to `setCount` within a single event handler only result in a single state update. This example shows how calling `setCount` twice only increments the count by one, not two, due to batching optimizations in React.

## Problem
The `bug.js` file contains a simple counter component.  Clicking the button is supposed to increment the counter by two. However, only a single increment occurs due to the way React batches updates.

## Solution
The solution (`bugSolution.js`) uses `useReducer` to manage the state. `useReducer` is more robust when complex state updates or multiple state changes are necessary.