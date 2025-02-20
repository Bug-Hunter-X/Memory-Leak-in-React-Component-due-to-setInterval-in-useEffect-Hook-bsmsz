# React setInterval useEffect Memory Leak

This repository demonstrates a common mistake in React when using the `setInterval` function within the `useEffect` hook.  Forgetting to return a cleanup function leads to a memory leak.

## Problem
The `bug.js` file contains a React component that uses `setInterval` to increment a counter every second. However, it fails to provide a cleanup function within the `useEffect` hook. This means that when the component unmounts, the `setInterval` continues running, causing a memory leak.

## Solution
The `bugSolution.js` file provides a corrected version.  A cleanup function is returned from `useEffect`, which uses `clearInterval` to stop the interval when the component unmounts, thus preventing the memory leak.

## How to run
1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.