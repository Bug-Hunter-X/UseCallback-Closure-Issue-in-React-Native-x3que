# React Native useCallback Hook Closure Issue

This repository demonstrates a common issue when using the `useCallback` hook in React Native with state variables. The problem occurs because the closure created by `useCallback` captures the state variable's value at the time of `useCallback` invocation, not during the function's execution.  This results in stale closures and unexpected behavior.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the unexpected behavior as described in `bug.js`.
5. Refer to `bugSolution.js` for a solution to the issue.

## Solution
The `bugSolution.js` file provides a fix by using the current state value within the function. This ensures that the function always operates with the most up-to-date state.