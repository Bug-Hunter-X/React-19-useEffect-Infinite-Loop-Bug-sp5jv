# React 19 useEffect Infinite Loop

This repository demonstrates a common error in React 19 involving infinite loops within `useEffect` hooks and provides a solution.

## Bug Description

The bug occurs when a state update inside a `useEffect` hook causes a re-render, which in turn triggers the `useEffect` again, resulting in an infinite loop. This often stems from incorrectly defining the dependencies array in `useEffect`.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console for continuous logging indicating the infinite loop. 

## Solution

The solution involves correctly specifying the dependencies array in the `useEffect` hook.  Only include the state variables that the effect directly depends on.