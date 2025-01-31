# Incorrect State Update in useEffect Hook

This repository demonstrates a common error in React when using the `useEffect` hook to update state.  The issue arises from the incorrect way of updating the state variable within the `useEffect`'s callback.

## The Bug

The `bug.js` file contains a component that attempts to increment a state variable (`count`) within a `useEffect` hook.  However, this approach fails because `setCount(count + 1)` uses the initial value of `count` (0) every time the component renders. The `useEffect` hook runs only once after the initial render and the state isn't updated in time.

## The Solution

The `bugSolution.js` file provides a corrected version. It uses a functional update for `setCount` to ensure that the correct value of `count` is used within the update logic.