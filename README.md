# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop due to incorrect usage of the dependency array.

## Bug Description

The `useEffect` hook is used to perform side effects after a component renders.  However, if the effect modifies a state variable that is also included in its dependency array, an infinite loop can occur.  The component will continuously re-render, triggering the effect again and again.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the console and the rapidly incrementing counter on the page.

## Solution

The solution involves properly managing the dependencies array in the `useEffect` hook.  This ensures that the effect only runs under specific conditions, thus preventing the infinite loop.
