# React Native: Cannot read properties of undefined (reading '...') before component mount

This repository demonstrates a common error in React Native where you attempt to access a component's state or props before the component has fully mounted. This often occurs due to asynchronous operations or race conditions between data fetching and rendering.

The `bug.js` file showcases the problematic code, while `bugSolution.js` provides the corrected implementation using the `useEffect` hook and conditional rendering to handle asynchronous data fetching. 

## How to reproduce the bug

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app. You should see the error in the console.

## Solution

The solution involves using the `useEffect` hook to fetch data after the component mounts and to only access the data after it has been fetched.  This prevents accessing undefined properties before data is available.