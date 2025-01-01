# Stale Closure Bug in React Functional Component
This repository demonstrates a common bug in React functional components involving stale closures when updating state.  The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the correct implementation.

## Problem
The problem lies in how the state update function `setCount` is used inside the `incrementCount` function.  Because `count` is captured by a closure, it references the initial state value. This leads to inconsistent and incorrect state updates.

## Solution
The solution utilizes the functional update pattern within the `setCount` function. This ensures that the update always uses the most current value of the state, resolving the stale closure issue.

## How to reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the application and observe the incorrect counting behavior in `bug.js`
4. Compare and observe the correct counting behavior in `bugSolution.js`