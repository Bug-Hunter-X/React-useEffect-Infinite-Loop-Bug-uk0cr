# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by a missing dependency.

## Bug Description
The `useEffect` hook is used to set an interval that updates a counter every second. However, the dependency array is empty (`[]`), which means the effect runs only once after the initial render.  Because `count` is not included in the dependency array, the effect will continuously trigger and update the counter even when `count` changes, resulting in an infinite loop. 

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the rapidly updating counter in the browser.